# Channel Setup

This file is maintained by the memory subsystem.

## Setup Entries

### registry

```json
[
  {
    "RegistrationId": "whatsapp:default",
    "ChannelType": "whatsapp",
    "ChannelId": "default",
    "DisplayName": "WhatsApp (default)",
    "Enabled": true,
    "RegisteredAtUtc": "2026-04-29T03:25:25.2208234+00:00",
    "SettingsJson": "{\n  \u0022ConnectionMode\u0022: \u0022baileys\u0022,\n  \u0022AccountId\u0022: \u0022default\u0022,\n  \u0022CredentialsDirectory\u0022: \u0022whatsapp\u0022,\n  \u0022DefaultRecipientNumber\u0022: \u0022\\u002B13362572629\u0022\n}"
  }
]
```

### whatsapp

# WhatsApp Channel Setup

- Channel: whatsapp
- Status: configured
- ConnectionMode: baileys
- AccountId: default
- DefaultRecipientNumber: +13362572629
- LegacyPairingPage: /api/whatsapp/pairing
- LegacyPairingUrl: http://localhost:5121/api/whatsapp/pairing?accountId=default

## Setup Flow
1. The runtime hosts the Baileys linked-device session in-process.
2. The coordinator starts login directly and returns a QR or pairing code in the active conversation.
3. Inbound WhatsApp messages are forwarded directly into the coordinator without a separate WebhookReceiver hop.
4. Replies for the active conversation flow back through the same in-process WhatsApp session.

### whatsapp.config

{
  "channel": "whatsapp",
  "connectionMode": "baileys",
  "accountId": "default",
  "configuredAtUtc": "2026-04-29T03:25:25.2208234+00:00",
  "defaultRecipientNumber": "\u002B13362572629"
}

### whatsapp.state

```json
{
  "channel.activity.whatsapp.default": "{\u0022ChannelType\u0022:\u0022whatsapp\u0022,\u0022ChannelId\u0022:\u0022default\u0022,\u0022LastStartedUtc\u0022:\u00222026-05-02T04:13:13.064873\u002B00:00\u0022,\u0022LastShutdownUtc\u0022:\u00222026-05-02T04:35:41.250422\u002B00:00\u0022,\u0022LastActiveUtc\u0022:\u00222026-05-02T04:35:41.250422\u002B00:00\u0022,\u0022LastInboundMessageUtc\u0022:\u00222026-05-01T23:03:37.640083\u002B00:00\u0022,\u0022LastInboundSenderId\u0022:\u002213366930850\u0022,\u0022LastInboundSenderDisplayName\u0022:\u0022AddledDev\u0022,\u0022LastOutboundMessageUtc\u0022:\u00222026-05-02T04:11:46.324933\u002B00:00\u0022,\u0022LastStartupSignalSentUtc\u0022:\u00222026-05-02T04:11:46.324933\u002B00:00\u0022,\u0022LastStartupSignalText\u0022:\u0022SkippyBot v0.0.31 is online on WhatsApp as 13362572629:48@s.whatsapp.net. Reply here to verify inbound delivery into the runtime.\u0022}",
  "conversation.context.05455AFF2AF564F91A858875DB219E47B52EF622BFC1C35084A4F031A46DE7B9": "{\u0022OriginKey\u0022:\u0022whatsapp|default|13366930850\u0022,\u0022ChannelType\u0022:\u0022whatsapp\u0022,\u0022ChannelId\u0022:\u0022default\u0022,\u0022SenderId\u0022:\u002213366930850\u0022,\u0022LastConversationStartedUtc\u0022:\u00222026-05-01T23:01:43\u002B00:00\u0022,\u0022LastConversationBoundaryReason\u0022:\u0022channel startup signal was sent after the previous exchange\u0022,\u0022LastUserMessageUtc\u0022:\u00222026-05-01T23:03:37\u002B00:00\u0022,\u0022LastUserMessage\u0022:\u0022the link doesn\\u2019t work\u0022,\u0022LastAssistantMessageUtc\u0022:\u00222026-05-01T23:24:21.099383\u002B00:00\u0022,\u0022LastAssistantMessage\u0022:\u0022I apologize for that. It looks like I provided a placeholder or an incorrect link in the previous message.\\n\\nTo properly authenticate and connect your Microsoft account, please try the following:\\n\\nIf you are using a specific integration or app, please let me know which one. Otherwise, the most reliable way to trigger the authentication process is to **reply with the phrase \\u0060reauth-microsoft\\u0060** or run the command **/setup-microsoft**.\\n\\nThis should trigger the official authentication flow and provide you with a valid, secure link to sign in.\u0022,\u0022AwaitingIdentity\u0022:false,\u0022AwaitingFollowUp\u0022:false}",
  "graph.auth.configured_username": "",
  "graph.auth.status": "failed: An error occurred while sending the request.",
  "graph.auth.password_configured": "false",
  "last-user-message": "the link doesn\u2019t work",
  "channel.setup.whatsapp.config": "{\r\n  \u0022channel\u0022: \u0022whatsapp\u0022,\r\n  \u0022connectionMode\u0022: \u0022baileys\u0022,\r\n  \u0022accountId\u0022: \u0022default\u0022,\r\n  \u0022configuredAtUtc\u0022: \u00222026-04-29T03:25:25.2208234\u002B00:00\u0022,\r\n  \u0022defaultRecipientNumber\u0022: \u0022\\u002B13362572629\u0022\r\n}",
  "graph.auth.configured_password": "",
  "graph.auth.mode": "device-code",
  "whatsapp.processed-inbound.default": "[\u002287201358569541:8@lid\\n3EB0C7FF69AD862A829EB6\u0022,\u002287201358569541:10@lid\\n3B873ABC8C4D8B2996FE\u0022,\u002287201358569541:10@lid\\n3BB943544B3A02C1A887\u0022,\u002287201358569541:10@lid\\n3BA5A08E1AC7A205213E\u0022,\u002287201358569541:10@lid\\n3B29F7FC4E4018250DE0\u0022,\u002287201358569541:10@lid\\n3B9BE6830497DD703207\u0022]",
  "graph.auth.user": "pjslauta@outlook.com",
  "channel.registry": "[\n  {\n    \u0022RegistrationId\u0022: \u0022whatsapp:default\u0022,\n    \u0022ChannelType\u0022: \u0022whatsapp\u0022,\n    \u0022ChannelId\u0022: \u0022default\u0022,\n    \u0022DisplayName\u0022: \u0022WhatsApp (default)\u0022,\n    \u0022Enabled\u0022: true,\n    \u0022RegisteredAtUtc\u0022: \u00222026-04-29T03:25:25.2208234\u002B00:00\u0022,\n    \u0022SettingsJson\u0022: \u0022{\\n  \\u0022ConnectionMode\\u0022: \\u0022baileys\\u0022,\\n  \\u0022AccountId\\u0022: \\u0022default\\u0022,\\n  \\u0022CredentialsDirectory\\u0022: \\u0022whatsapp\\u0022,\\n  \\u0022DefaultRecipientNumber\\u0022: \\u0022\\\\u002B13362572629\\u0022\\n}\u0022\n  }\n]",
  "graph.auth.tenant_id": "consumers",
  "channel.setup.whatsapp.state": "",
  "graph.auth.account_id": "00000000-0000-0000-c044-f4f57ce46eac.9188040d-6c67-4c5b-b112-36a304b66dad",
  "channel.setup.whatsapp": "# WhatsApp Channel Setup\r\n\r\n- Channel: whatsapp\r\n- Status: configured\r\n- ConnectionMode: baileys\r\n- AccountId: default\r\n- DefaultRecipientNumber: \u002B13362572629\r\n- LegacyPairingPage: /api/whatsapp/pairing\r\n- LegacyPairingUrl: http://localhost:5121/api/whatsapp/pairing?accountId=default\r\n\r\n## Setup Flow\r\n1. The runtime hosts the Baileys linked-device session in-process.\r\n2. The coordinator starts login directly and returns a QR or pairing code in the active conversation.\r\n3. Inbound WhatsApp messages are forwarded directly into the coordinator without a separate WebhookReceiver hop.\r\n4. Replies for the active conversation flow back through the same in-process WhatsApp session.",
  "coordinator.model.preferred": "ollama",
  "runtime.lifecycle": "{\u0022LastStartedUtc\u0022:\u00222026-05-02T04:11:41.933282\u002B00:00\u0022,\u0022LastShutdownUtc\u0022:\u00222026-05-02T04:35:41.234146\u002B00:00\u0022}",
  "graph.auth.client_id": "a5493629-9dd9-40f8-b526-09b1f401f5bb"
}
```