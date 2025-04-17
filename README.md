# n8n Chat Widget 

The **n8n Chat Widget** is a lightweight, customizable chat widget designed to integrate seamlessly with n8n workflows. It allows users to embed a chat interface into their websites or web applications, enabling real-time communication with visitors or customers. The widget sends messages to an n8n webhook, which can then be processed and routed to various services.

## Features

- **Customizable Branding**: Add your company logo, name, and welcome message to personalise the chat experience.
- **Styling Options**: Configure colours, positions, and fonts to match your website's design.
- **n8n Integration**: Easily connect the widget to your n8n workflows using a webhook URL.
- **Lightweight and Fast**: Minimal impact on your website's performance.
- **Responsive Design**: Works seamlessly across devices and screen sizes.

---

## Installation

### 1. Add the Script to Your Website

Include the following script in your HTML file to initialise the widget:

```html
<!-- Widget Configuration -->
<script>
    window.ChatWidgetConfig = {
        webhook: {
            url: '<your n8n webhook URL>',
            route: 'general' // Optional: Specify the route for n8n webhook processing
        },
        branding: {
            logo: '<your company logo URL>',
            name: 'Your Company Name', // Your company name
            welcomeText: 'Hi 👋, how can we help?', // Welcome message
            responseTimeText: 'We typically respond right away' // Response time message
        },
        style: {
            primaryColor: '#854fff', // Primary color
            secondaryColor: '#6b3fd4', // Secondary color
            position: 'right', // Position of the widget (left or right)
            backgroundColor: '#ffffff', // Background color of the chat widget
            fontColor: '#000000' // Text colour for messages and interface
        }
    };
</script>
<script src="https://cdn.jsdelivr.net/gh/prathameshshirole/n8n-chat-widget@latest/n8n-chat-widget.js"></script>
<!-- Widget Script -->

```

## Replace Placeholder Values

Update the following placeholders in the ChatWidgetConfig object:

1. `<your n8n webhook URL>:` Your n8n webhook endpoint URL.
2. `<your company logo URL>:` Direct link to your logo (e.g., hosted on AWS S3 or GitHub).
3. Customise branding and styling options as needed

## How It Works
- **User Interaction:** When a user interacts with the chat widget, their message is sent to the specified n8n webhook URL.
- **Webhook Processing:** The n8n workflow processes the incoming message and performs actions such as sending emails, triggering notifications, or integrating with third-party services.
- **Response Handling:** Responses from the n8n workflow can be configured to display back in the chat widget (requires additional setup).

## Example Use Cases
1. Customer Support
Embed the widget on your website to provide real-time customer support. Route messages to your support team via email or messaging platforms.

2. Lead Generation
Collect leads by capturing user queries and forwarding them to your CRM or marketing automation tools.

3. Feedback Collection
Use the widget to gather feedback from users and store it in a database for analysis.
