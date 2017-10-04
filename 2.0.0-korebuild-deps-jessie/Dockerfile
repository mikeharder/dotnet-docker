FROM microsoft/dotnet:2.0.0-runtime-deps-jessie

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        git \
# KoreBuild dependencies
        unzip \
        curl \
    && rm -rf /var/lib/apt/lists/*

ENV DOTNET_SKIP_FIRST_TIME_EXPERIENCE true
