#Ejemplo -> .Net core 7 api rest + swagger

	-Scaffold Up API 
	- Build Docker Image 
	- Run Our Inage (without HTTPS) 
	- Some Container housekeeping
	- Generate Dev Certifcate for Container - Configuring User Secrets 
	- Rebuild our image (with User Secrets) 
	- Overview of Docker Run parameters 
	- Run our Container with HTTPS (Docker CLI) Migrate and Run in Docker Compose 
	- Certificate file name case sensitivity

Generate DockerFile like this -> 
````DockerFile
FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base
WORKDIR /app
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY ["UserDemostration/UserDemostration.csproj", "UserDemostration/"]
RUN dotnet restore "UserDemostration/UserDemostration.csproj"
COPY . .
WORKDIR "/src/UserDemostration"
RUN dotnet build "UserDemostration.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "UserDemostration.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "UserDemostration.dll"]
````

Run this command to build an image
````bash
foo@bar:~$ Docker build -t <name image> .
````

