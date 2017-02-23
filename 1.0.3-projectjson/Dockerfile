FROM microsoft/dotnet:1.0.3-sdk-projectjson

WORKDIR /dotnetapp

# copy project.json and restore as distinct layers
COPY 1.0.3-projectjson/project.json .
RUN dotnet restore

# copy and build everything else
COPY . .
RUN dotnet publish -c Release -o out
ENTRYPOINT ["dotnet", "out/dotnetapp.dll"]
