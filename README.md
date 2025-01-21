# keepsrv00-alive
Optimized Workflow



Explanation of Changes

1. Store ACCOUNTS_JSON in GitHub Secrets
	•	Add ACCOUNTS_JSON to your repository’s secrets:
	•	Go to Settings → Secrets and variables → Actions → New repository secret.
	•	Add your ACCOUNTS_JSON with the following JSON structure:

[
  {"RES":"n", "SSH_USER":"CR", "SSH_PASS":"Y N jVPF", "REALITY":"www.speedtest.net", "SUUID":"f6e8f9e4-abbc-4f85-a0f0-", "TCP1_PORT":"13580", "TCP2_PORT":"13759", "UDP_PORT":"38866", "HOST":"scom", "ARGO_DOMAIN":"s7cr.us.kg", "ARGO_AUTH":"dfhj k"},
  {"RES":"n", "SSH_USER":"LZ", "SSH_PASS":"k.qKZZ", "REALITY":"www.icloud.com", "SUUID":"02e0ae79-94cd-42d8-f102b29", "TCP1_PORT":"18181", "TCP2_PORT":"22041", "UDP_PORT":"37778", "HOST":"sd.com", "ARGO_DOMAIN":"lzi8.xinkg", "ARGO_AUTH":"dfhj k"}
]



2. Sending Results to Telegram
	•	Secrets Needed:
	•	TELEGRAM_BOT_TOKEN: Telegram bot token.
	•	TELEGRAM_CHAT_ID: Chat ID where the message will be sent.
	•	Setup Telegram Bot:
	1.	Create a Telegram bot using BotFather and get the bot token.
	2.	Get your chat ID by messaging your bot and visiting https://api.telegram.org/bot<your_bot_token>/getUpdates.
	•	Send Message:
	•	The results are written to results.txt.
	•	The curl command sends the content of results.txt to the specified Telegram chat.

Benefits of This Workflow
	1.	Secure: Sensitive data like SSH credentials and JSON configurations are stored securely in GitHub Secrets.
	2.	Automated Notifications: Results are sent to Telegram, providing real-time updates.
	3.	Customizable: You can easily adjust the script to include additional functionality or logging.

Let me know if you have further questions!
