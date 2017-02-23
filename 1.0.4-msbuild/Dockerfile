FROM microsoft/dotnet-nightly:1.0.4-sdk-rc4

WORKDIR /dotnetapp

# copy csproj and Nuget.config, and restore as distinct layers
COPY 1.0.4-msbuild/*.csproj .
COPY 1.0.4-msbuild/NuGet.config .
RUN dotnet restore

# copy and build everything else
COPY . .
RUN dotnet publish -c Release -o out
ENTRYPOINT ["dotnet", "out/dotnetapp.dll"]
