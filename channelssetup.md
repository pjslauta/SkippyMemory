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
    "SettingsJson": "{\r\n  \u0022ConnectionMode\u0022: \u0022baileys\u0022,\r\n  \u0022AccountId\u0022: \u0022default\u0022,\r\n  \u0022CredentialsDirectory\u0022: \u0022whatsapp\u0022,\r\n  \u0022DefaultRecipientNumber\u0022: \u0022\\u002B13362572629\u0022\r\n}"
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
  "channel.activity.whatsapp.default": "{\u0022ChannelType\u0022:\u0022whatsapp\u0022,\u0022ChannelId\u0022:\u0022default\u0022,\u0022LastStartedUtc\u0022:\u00222026-05-01T19:28:21.9128847\u002B00:00\u0022,\u0022LastShutdownUtc\u0022:\u00222026-05-01T19:31:09.4615138\u002B00:00\u0022,\u0022LastActiveUtc\u0022:\u00222026-05-01T19:31:09.4615138\u002B00:00\u0022,\u0022LastInboundMessageUtc\u0022:\u00222026-05-01T19:31:07.8910022\u002B00:00\u0022,\u0022LastInboundSenderId\u0022:\u002213366930850\u0022,\u0022LastInboundSenderDisplayName\u0022:\u0022AddledDev\u0022,\u0022LastOutboundMessageUtc\u0022:\u00222026-05-01T19:31:07.9090022\u002B00:00\u0022,\u0022LastStartupSignalSentUtc\u0022:null,\u0022LastStartupSignalText\u0022:null}",
  "conversation.context.05455AFF2AF564F91A858875DB219E47B52EF622BFC1C35084A4F031A46DE7B9": "{\u0022OriginKey\u0022:\u0022whatsapp|default|13366930850\u0022,\u0022ChannelType\u0022:\u0022whatsapp\u0022,\u0022ChannelId\u0022:\u0022default\u0022,\u0022SenderId\u0022:\u002213366930850\u0022,\u0022LastConversationStartedUtc\u0022:\u00222026-05-01T19:27:21\u002B00:00\u0022,\u0022LastConversationBoundaryReason\u0022:\u0022follow-up window expired\u0022,\u0022LastUserMessageUtc\u0022:\u00222026-05-01T19:27:21\u002B00:00\u0022,\u0022LastUserMessage\u0022:\u0022mark all email in my inbox as read\u0022,\u0022LastAssistantMessageUtc\u0022:\u00222026-05-01T19:29:15.0610291\u002B00:00\u0022,\u0022LastAssistantMessage\u0022:\u0022Based on the provided context, it seems you are interested in reading a specific email from the list of recent inbox messages. Let\\u0027s start by selecting one of the emails from the recently fetched inbox messages.\\n\\nHere are some options from the list:\\n- Michele: Peter, have you seen this offer?! \\uD83D\\uDC40 Take $4272.66 off your account!\\n- Belk: This is a good day to shop 60%Off\\uD83D\\uDECD\\uFE0F\\n- LinkedIn: Backend Python Software Engineer role at Nvidia: Actively recruiting\\n- Apple Card Support: Your Apple Card statement is ready\\n\\nCould you please indicate which email you would like to read more details from, or provide another choice if you prefer? If you want to read all of them, just let me know, and I can proceed with reading those emails for you.\u0022,\u0022AwaitingIdentity\u0022:false,\u0022AwaitingFollowUp\u0022:true}",
  "graph.auth.configured_username": "",
  "graph.auth.status": "authenticated",
  "graph.auth.password_configured": "false",
  "last-user-message": "mark all email in my inbox as read",
  "channel.setup.whatsapp.config": "{\r\n  \u0022channel\u0022: \u0022whatsapp\u0022,\r\n  \u0022connectionMode\u0022: \u0022baileys\u0022,\r\n  \u0022accountId\u0022: \u0022default\u0022,\r\n  \u0022configuredAtUtc\u0022: \u00222026-04-29T03:25:25.2208234\u002B00:00\u0022,\r\n  \u0022defaultRecipientNumber\u0022: \u0022\\u002B13362572629\u0022\r\n}",
  "graph.auth.configured_password": "",
  "graph.auth.mode": "device-code",
  "whatsapp.processed-inbound.default": "[\u002287201358569541:8@lid\\n3EB0C7FF69AD862A829EB6\u0022]",
  "graph.auth.user": "pjslauta@outlook.com",
  "channel.registry": "[\r\n  {\r\n    \u0022RegistrationId\u0022: \u0022whatsapp:default\u0022,\r\n    \u0022ChannelType\u0022: \u0022whatsapp\u0022,\r\n    \u0022ChannelId\u0022: \u0022default\u0022,\r\n    \u0022DisplayName\u0022: \u0022WhatsApp (default)\u0022,\r\n    \u0022Enabled\u0022: true,\r\n    \u0022RegisteredAtUtc\u0022: \u00222026-04-29T03:25:25.2208234\u002B00:00\u0022,\r\n    \u0022SettingsJson\u0022: \u0022{\\r\\n  \\u0022ConnectionMode\\u0022: \\u0022baileys\\u0022,\\r\\n  \\u0022AccountId\\u0022: \\u0022default\\u0022,\\r\\n  \\u0022CredentialsDirectory\\u0022: \\u0022whatsapp\\u0022,\\r\\n  \\u0022DefaultRecipientNumber\\u0022: \\u0022\\\\u002B13362572629\\u0022\\r\\n}\u0022\r\n  }\r\n]",
  "graph.auth.tenant_id": "consumers",
  "channel.setup.whatsapp.state": "",
  "graph.auth.account_id": "00000000-0000-0000-c044-f4f57ce46eac.9188040d-6c67-4c5b-b112-36a304b66dad",
  "channel.setup.whatsapp": "# WhatsApp Channel Setup\r\n\r\n- Channel: whatsapp\r\n- Status: configured\r\n- ConnectionMode: baileys\r\n- AccountId: default\r\n- DefaultRecipientNumber: \u002B13362572629\r\n- LegacyPairingPage: /api/whatsapp/pairing\r\n- LegacyPairingUrl: http://localhost:5121/api/whatsapp/pairing?accountId=default\r\n\r\n## Setup Flow\r\n1. The runtime hosts the Baileys linked-device session in-process.\r\n2. The coordinator starts login directly and returns a QR or pairing code in the active conversation.\r\n3. Inbound WhatsApp messages are forwarded directly into the coordinator without a separate WebhookReceiver hop.\r\n4. Replies for the active conversation flow back through the same in-process WhatsApp session.",
  "runtime.lifecycle": "{\u0022LastStartedUtc\u0022:\u00222026-05-01T18:11:47.889265\u002B00:00\u0022,\u0022LastShutdownUtc\u0022:\u00222026-05-01T19:31:09.4282538\u002B00:00\u0022}",
  "graph.auth.client_id": "a5493629-9dd9-40f8-b526-09b1f401f5bb"
}
```