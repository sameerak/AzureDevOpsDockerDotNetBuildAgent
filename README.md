# AzureDevOpsDockerDotNetBuildAgent

### How to build the docker build agent and run it.

1. Execute "docker build -t dockeragent:latest ." in powershell with in this directory to create the docker container.
2. Execute "docker run -e AZP_URL=\<Azure DevOps instance\> -e AZP_TOKEN=\<PAT token\> -e AZP_AGENT_NAME=mydockeragent -e AZP_POOL=<(optional) pool to register the agent under> dockeragent:latest" to start and listen for build tasks.

This Dockerfile is created, combining the Dockerfiles from [VS build tools container](https://docs.microsoft.com/en-us/visualstudio/install/build-tools-container?view=vs-2019) and [Azure pipeline agent](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops).\
Powershell file start.ps1 can be found in [Azure pipeline agent](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops) and [start.ps1](https://github.com/PacktPublishing/Learning-Azure-DevOps---B16392/blob/master/Chapter-6/start.ps1).
