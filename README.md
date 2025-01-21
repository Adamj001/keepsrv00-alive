# keepsrv00-alive
Optimized Workflow from https://github.com/yonggekkk/sing-box-yg

Explanation of Changes

1. Store ACCOUNTS_JSON in GitHub Secrets
	•	Add ACCOUNTS_JSON to your repository’s secrets:
	•	Go to Settings → Secrets and variables → Actions → New repository secret.
	•	Add your ACCOUNTS_JSON with the following JSON structure:

 # serv00变量添加规则：
    # RES：n表示每次不重置部署，y表示每次重置部署。SSH_USER表示用户名。SSH_PASS表示密码。REALITY表示reality域名(用户名.serv00.net)。SUUID表示uuid。TCP1_PORT表示vless的tcp端口。TCP2_PORT表示vmess的tcp端口。UDP_PORT表示hy2的udp端口。HOST表示登录服务器域名。ARGO_DOMAIN表示argo固定域名，临时域名留空。ARGO_AUTH表示argo固定域名token，临时域名留空
    # 每行一个{serv00服务器}，末尾用,间隔
    [
 {"RES":"y", "SSH_USER":"ygkkk2", "SSH_PASS":"ygkkk456", "REALITY":"time.is", "SUUID":"2f68aba2-b460-43ca-b9c3-1ac843bd2c70", "TCP1_PORT":"55254", "TCP2_PORT":"55255", "UDP_PORT":"55256", "HOST":"s16.serv00.com", "ARGO_DOMAIN":"abcd.ygkkk.eu.org", "ARGO_AUTH":"eyJhIjoiOTM3YzFjYWI88552NTFiYTM4ZTY0ZDQzMWRhOTgyNzkiLCJ0IjoiYjI1MDc5MDktMWQzMS00MWNmLWI1N2QtYTkxNGIxOTAzOTExIiwicyI6Ik9XTmxNR1F6WkRRdE56a3dNaTAwWlRaakxXRmlNelF0TkRBd1pUQTRNVEJqTUdVeCJ9"} 
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
