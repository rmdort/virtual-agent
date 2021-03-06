---

copyright:
  years: 2015, 2017
lastupdated: "2017-08-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Integrating the agent
{: #integrate}

To publish the agent for production use, you must take additional steps to support the functions performed by the agent, and make it available to users in a secure manner.
{: shortdesc}

## Choose an integration method

You can integrate the agent in one of the following ways:

- Add the {{site.data.keyword.IBM_notm}}-provided chat interface as-is to your customer-facing website. 
  See [Adding the provided chat widget to your UI](integrate_add-chat.html).

- Extend the provided chat window to customize it for your needs. 
  See [Adding the provided chat widget to your UI](integrate_add-chat.html).

- Build your own chat interface using the provided Client SDK. 
  See [Building a custom chat interface](integrate_custom-chat.html).

- Add the agent to an existing support channel and use the API to interact with the agent programmatically. 
  See [Adding the agent to a support channel](integrate_backend.html).

### Before you begin

Regardless of the method you use to publish the agent for production use, consider making a clone of the agent beforehand. Having a non-integrated copy of the agent enables you to test changes or additions to functionality on the test copy before you make them to the agent that is being used in a production environment. See [Cloning the agent](agent-create.html#clone) for more information.