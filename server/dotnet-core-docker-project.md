# DotNet Core Docker Project

## Required Steps

- [New GitHub Repository](/server/new-github-repository.md)

## Setup

Navigate to your project directory and do the following

```bash
$ vi .gitignore
bin/
obj/
```

```bash
$ vi Dockerfile
```

```dockerfile
FROM microsoft/dotnet:2.0-sdk
RUN mkdir /code
WORKDIR /code
```

```bash
$ vi docker-compose.yml
```

```YAML
version: "3"
services:
  server:
    build: .
    command: dotnet run --project api
    ports:
      - "5000:5000"
    volumes:
      - .:/code
  database:
    image: postgres:10.1-alpine
    restart: always
    ports:
      - 5432:5432
    environment:
      POSTGRES_PASSWORD: password
    volumes:
      - pgdata:/var/lib/postgresql/data
 
volumes:
  pgdata:
```

```bash
$ sudo docker-compose run server dotnet new sln
$ sudo docker-compose run server dotnet new webapi --output api
$ sudo docker-compose run server dotnet sln add api/api.csproj
$ sudo docker-compose run server dotnet new xunit --output tests
$ sudo docker-compose run server dotnet sln add tests/tests.csproj
$ sudo chown -R username:username .
```

```bash
$ vi api/Program.cs
```

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.AspNetCore;
using Microsoft.AspNetCore.Hosting;
using Microsoft.Extensions.Configuration;
using Microsoft.Extensions.Logging;

namespace code
{
    public class Program
    {
        public static void Main(string[] args)
        {
            BuildWebHost(args).Run();
        }

        public static IWebHost BuildWebHost(string[] args) =>
            WebHost.CreateDefaultBuilder(args)
                .UseUrls("http://0.0.0.0:5000")
                .UseStartup<Startup>()
                .Build();
    }
}
```

## Next Steps

- [DotNet New WebAPI](/server/dotnet-new-webapi.md)

## Back To The Beginning

- [Start Over](/README.md)

