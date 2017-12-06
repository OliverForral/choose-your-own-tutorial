# DotNet Core Docker Project

## Required Steps

- [New GitHub Repository](/server/new-github-repository.md)

## Setup

Navigate to your project directory and do the following

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
        command: dotnet run
        ports:
            - "5000:5000"
        volumes:
            - .:/code
```

```bash
$ sudo docker-compose run server bash
# dotnet new sln
# mkdir api
# cd api
# dotnet new webapi
# cd ..
# dotnet sln add api/api.csproj
# mkdir tests
# cd tests
# dotnet new xunit
# cd ..
# dotnet sln add tests/tests.csproj
# exit
$ sudo chown -R username:username .
```

```bash
$ vi Program.cs
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

```bash
$ vi .gitignore
/bin/
/obj/
```

## Next Steps

- [DotNet New WebAPI](/server/dotnet-new-webapi.md)

## Back To The Beginning

- [Start Over](/README.md)

