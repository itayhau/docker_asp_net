FROM mcr.microsoft.com/dotnet/sdk:3.1
COPY . /tmp/.
WORKDIR /tmp/WebApplication2
RUN dotnet build
WORKDIR /tmp/WebApplication2/WebApplication2
ARG BUILD_CONFIGURATION=Debug
ENV ASPNETCORE_ENVIRONMENT=Development
ENV DOTNET_USE_POLLING_FILE_WATCHER=true  
ENV ASPNETCORE_URLS=http://+:80  
EXPOSE 80
ENTRYPOINT ["dotnet", "/tmp/WebApplication2/WebApplication2/bin/Debug/netcoreapp3.1/WebApplication2.dll"]

