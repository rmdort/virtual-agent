---

copyright:
  years: 2015, 2017
lastupdated: "2017-08-01"

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

# Publishing the agent for demo use
{: #publish}

In less than 10 minutes, you can publish the agent to a test site to share it with colleagues and assess together whether it meets the needs of your organization.
{: shortdesc}

To publish the agent to a test site, complete the following steps:

1.  Determine where on the page you want the bot's chat window to be displayed. On the `<div>` HTML element that defines the target area, add an ID attribute if one is not defined. You will use the ID attribute to refer to the element later. For example, `<div id="ibm-chat-root"></div>`.

1.  Follow the instructions in [Getting API keys](publish.html#api-keys) to retrieve the following keys:
    - Client ID
    - Client secret token

1.  From the main menu ![Icon with three horizontal lines](images/hamburger.png) , click **Documentation**, and then scroll down to the **Publish** section.

1.  If you have multiple agents, click the down-arrow to get the bot ID for the agent you want to publish.

    This botID is the ID that was generated by the service and assigned to your bot.

    A script block is generated and displayed on the page. This script can be copied and placed into a HTML page to render the agent on the page. You must replace some of the values in the script with appropriate values for your instance.

1.  Copy the script block, and paste it into a text or HTML editor.

    ``` Javascript
    <script src='https://unpkg.com/@watson-virtual-agent/chat-widget@1.6.0/dist/chat.min.js'>
    </script>
    <script>
      IBMChat.init({
        el: 'ibm_chat_root',
        baseURL: 'https://api.ibm.com/virtualagent/run/api/v1',
        botID: 'YOUR_BOT_ID',
        XIBMClientID: 'YOUR_IBM_CLIENT_ID',
        XIBMClientSecret: 'YOUR_IBM_CLIENT_SECRET'
      });
    </script>
    ```

1.  Replace the following attribute values:
    - **el**: Specify the ID of the element that you chose to use in Step 1.
    - **XIBMClientID**: Add the client ID value that you copied earlier.
    - **XIBMClientSecret**: Add the client secret token value that you copied earlier.

   Use the baseURL and botID values that are specified in the script; they are generated by the service.

   **Important:** Keep the values of the XIBMClientID and XIBMClientSecret as private as possible.

1.  Embed and initialize the Watson Virtual Agent chat widget by pasting the revised script into your web page.

   Add the script as close to the closing `</body>` tag as possible to prevent the script from blocking the rest of the page from rendering. This placement also ensures that whichever element you associated with the script will be fully rendered by the time the script is executed.

1.  Refresh the web page and give the agent a try!

   The chat widget is associated with and rendered to the HTML element that you designated in Step 1. You can hide or show and position that element. The widget extends to the full height and width of the element. The maximum width is 768 pixels, and the minimum hight is 300 pixels.

When you are ready to put the agent to work helping your customers directly, you must perform some additional steps. See [Integrating the agent](integrate.html) for more details.

# Getting API keys
{: #api-keys}

To prove that you have permission to use the Watson Virtual Agent API services, the following  keys must be associated with any API calls that are made to the service:

- Client ID
- Client secret token

{: shortdesc}

Follow these steps to retrieve the credentials.

1.  Go to the [IBM developerWorks API Explorer ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/api/){: new_window} web site, and sign in with the same IBM ID that was used to sign up for the service subscription. Create a user name if necessary. Click the **My APIs** link in the page header.

1.  Look for the {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}} tile, and then click the key icon associated with it.

1.  If not selected, select the key you want to use. Two credentials are generated for the key, and are shown with their values obfuscated in two fields. Hover over the fields.

1.  Click the **SHOW** button to remove the obfuscation from the field values.

1.  You will need to provide these values later, so copy them into a text file.
    - The first field contains the client ID key.
    - The second field contains the client secret token.

  ![Add node](images/api-explorer.jpg)