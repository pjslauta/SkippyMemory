# Channel Setup

This file is maintained by the memory subsystem.

## Setup Entries

_No channel setup entries yet._

```json
{
  "graph.auth.mode": "device-code",
  "graph.auth.tenant_id": "consumers",
  "graph.auth.password_configured": "false",
  "graph.auth.account_id": "00000000-0000-0000-c044-f4f57ce46eac.9188040d-6c67-4c5b-b112-36a304b66dad",
  "graph.auth.client_id": "a5493629-9dd9-40f8-b526-09b1f401f5bb",
  "channel.setup.whatsapp": "# WhatsApp Channel Setup\r\n\r\n- Channel: whatsapp\r\n- Status: configured\r\n- ConnectionMode: baileys\r\n- AccountId: default\r\n- DefaultRecipientNumber: \u002B13362572629\r\n- LegacyPairingPage: /api/whatsapp/pairing\r\n- LegacyPairingUrl: http://localhost:5121/api/whatsapp/pairing?accountId=default\r\n\r\n## Setup Flow\r\n1. The runtime hosts the Baileys linked-device session in-process.\r\n2. The coordinator starts login directly and returns a QR or pairing code in the active conversation.\r\n3. Inbound WhatsApp messages are forwarded directly into the coordinator without a separate WebhookReceiver hop.\r\n4. Replies for the active conversation flow back through the same in-process WhatsApp session.",
  "channel.setup.whatsapp.config": "{\r\n  \u0022channel\u0022: \u0022whatsapp\u0022,\r\n  \u0022connectionMode\u0022: \u0022baileys\u0022,\r\n  \u0022accountId\u0022: \u0022default\u0022,\r\n  \u0022configuredAtUtc\u0022: \u00222026-04-29T03:25:25.2208234\u002B00:00\u0022,\r\n  \u0022defaultRecipientNumber\u0022: \u0022\\u002B13362572629\u0022\r\n}",
  "channel.setup.whatsapp.state": "",
  "channel.registry": "[\r\n  {\r\n    \u0022RegistrationId\u0022: \u0022whatsapp:default\u0022,\r\n    \u0022ChannelType\u0022: \u0022whatsapp\u0022,\r\n    \u0022ChannelId\u0022: \u0022default\u0022,\r\n    \u0022DisplayName\u0022: \u0022WhatsApp (default)\u0022,\r\n    \u0022Enabled\u0022: true,\r\n    \u0022RegisteredAtUtc\u0022: \u00222026-04-29T03:25:25.2208234\u002B00:00\u0022,\r\n    \u0022SettingsJson\u0022: \u0022{\\r\\n  \\u0022ConnectionMode\\u0022: \\u0022baileys\\u0022,\\r\\n  \\u0022AccountId\\u0022: \\u0022default\\u0022,\\r\\n  \\u0022CredentialsDirectory\\u0022: \\u0022whatsapp\\u0022,\\r\\n  \\u0022DefaultRecipientNumber\\u0022: \\u0022\\\\u002B13362572629\\u0022\\r\\n}\u0022\r\n  }\r\n]",
  "channel.activity.whatsapp.default": "{\u0022ChannelType\u0022:\u0022whatsapp\u0022,\u0022ChannelId\u0022:\u0022default\u0022,\u0022LastStartedUtc\u0022:null,\u0022LastShutdownUtc\u0022:\u00222026-05-01T15:06:35.326945\u002B00:00\u0022,\u0022LastActiveUtc\u0022:\u00222026-05-01T15:06:35.326945\u002B00:00\u0022,\u0022LastInboundMessageUtc\u0022:null,\u0022LastInboundSenderId\u0022:null,\u0022LastInboundSenderDisplayName\u0022:null,\u0022LastOutboundMessageUtc\u0022:null,\u0022LastStartupSignalSentUtc\u0022:null,\u0022LastStartupSignalText\u0022:null}",
  "graph.auth.configured_username": "",
  "graph.auth.user": "pjslauta@outlook.com",
  "graph.auth.configured_password": "",
  "runtime.lifecycle": "{\u0022LastStartedUtc\u0022:\u00222026-05-01T17:04:27.369536\u002B00:00\u0022,\u0022LastShutdownUtc\u0022:\u00222026-05-01T17:05:27.3832455\u002B00:00\u0022}",
  "graph.auth.status": "authenticated"
}
```
