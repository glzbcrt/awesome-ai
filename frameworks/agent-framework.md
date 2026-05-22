# Microsoft Agent Framework

## My Notes

### Packages

#### agent-framework-foundry

This package contains the Microsoft Foundry **integrations** for Microsoft Agent Framework. Provides the following:

- Foundry memory context provider.
- Toolbox integration.

- FoundryAgent class that connect to existing PromptAgents or HostedAgents in Foundry.

            agent = FoundryAgent(
                project_endpoint="https://your-project.services.ai.azure.com",
                agent_name="my-prompt-agent",
                agent_version="1.0",
                credential=AzureCliCredential(),
                tools=[my_function_tool],
            )
            result = await agent.run("Hello!")

#### agent-framework-foundry-hosting

This package provides the integration of Agent Framework agents and workflows with the Foundry Agent Server, which can be hosted on Foundry infrastructure.

#### agent-framework-foundry-local

Foundry Local integration for Microsoft Agent Framework.

#### agent-framework-hyperlight

Hyperlight CodeAct integrations for Microsoft Agent Framework.

### AI Python SDK

#### Foundry Local

#### foundry-local-sdk

Foundry Local Manager Python SDK: Control-plane SDK for Foundry Local.
