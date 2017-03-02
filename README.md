# Dockers
List of my docker images

 - [dind-deploy.net.rc2](dind-deploy.net.rc2/Dockerfile) - DIND runner image with AWS ECS deploy and .NET Core SDK RC2.3131
 - [dind-deploy.net.rc4](dind-deploy.net.rc4/Dockerfile) - DIND runner image with AWS ECS deploy and .NET Core SDK RC4.4771
 - [alpine.php7](alpine.php7/Dockerfile) - Runtime container on Apline linux with PHP7
 - [alpine.npm.python](alpine.npm.python/Dockerfile) - Building container for Node (and Python)
 - [firefly-core](firefly-core/Dockerfile) - Runtime container with .NET Core SDK RC2 for the Firefly.net project. Includes Node.js, npm and a 
 firefly-pdf-render cli tool.
 - [firefly-core-runtime](firefly-core-runtime/Dockerfile) - Same as firefly-core but based on runtime image without sdk (lighter)