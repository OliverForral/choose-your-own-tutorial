# DotNet Core Docker Project

## Required Steps

- [New GitHub Repository](/server/new-github-repository.md)

## Setup

Navigate to your project directory and do the following

```bash
$ vi Dockerfile
```

```dockerfile
FROM microsoft/aspnetcore-build:2.0 AS build-env
WORKDIR /app

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY . ./
RUN dotnet publish -c Release -o out

# Build runtime image
FROM microsoft/aspnetcore:2.0
WORKDIR /app
COPY --from=build-env /app/out .
ENTRYPOINT ["dotnet", "aspnetapp.dll"]
```

```bash
$ vi .dockerignore
bin\
obj\
$ cp .dockerignore .gitignore
```

## Next Steps

- [DotNet New WebAPI](/server/dotnet-new-webapi.md)

## Back To The Beginning

- [Start Over](/README.md)

