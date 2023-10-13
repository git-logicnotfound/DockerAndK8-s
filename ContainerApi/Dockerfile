FROM mcr.microsoft.com/dotnet/sdk:6.0 as build-env
WORKDIR /src
COPY ContainerApi.csproj ./
RUN dotnet restore
COPY . ./
RUN dotnet publish -c release -o /publish

FROM mcr.microsoft.com/dotnet/aspnet:6.0 as runtime
WORKDIR /publish
COPY --from=build-env /publish .
EXPOSE 80
ENTRYPOINT [ "dotnet","ContainerApi.dll" ]