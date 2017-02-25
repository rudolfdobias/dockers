FROM gitlab/dind

WORKDIR var

RUN sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ trusty main" > /etc/apt/sources.list.d/dotnetdev.list' && \
    apt-key adv --keyserver apt-mo.trafficmanager.net --recv-keys 417A0893 && \
    apt-get update -q && \
    apt-get install -qy \
      curl \
      libuv-dev \
      dotnet-dev-1.0.0-rc4-004771 \
      python-setuptools \
      jq \
      build-essential \
      python-pip \
      libuv0.10 &&\
    pip install awscli && \
    apt-get clean apt-get purge && \
    rm -rf /var/lib/apt/lists/*

# ECS deploy
RUN curl -L https://github.com/silinternational/ecs-deploy/archive/2.5.0.tar.gz | tar xvz && cp ecs-deploy-2.5.0/ecs-deploy /usr/local/bin/ecs-deploy
RUN chmod a+x /usr/local/bin/ecs-deploy

# Trigger the population of the local nuget package cache
ENV NUGET_XMLDOC_MODE skip
RUN mkdir warmup \
    && cd warmup \
    && dotnet new \
    && cd .. \
    && rm -rf warmup \
    && rm -rf /tmp/NuGetScratch

