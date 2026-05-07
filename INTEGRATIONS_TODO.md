# Integrations Documentation TODO

This file tracks integration documentation that needs to be created in `apps/docs/integrations/`.

## Status

✅ = Documented
🚧 = In Progress
⏳ = Pending

## Integration Documentation Status

### Messaging Platforms

| Integration             | Status | File                     | Notes                                               |
| ----------------------- | ------ | ------------------------ | --------------------------------------------------- |
| WhatsApp (Business API) | ✅     | `whatsapp.mdx`           | Existing                                            |
| WhatsApp QR             | ✅     | `whatsapp-qr.mdx`        | V1 user-facing guide published                      |
| Instagram               | ✅     | `instagram.mdx`          | V1 user-facing guide published (automatic + manual) |
| Facebook Messenger      | ✅     | `facebook-messenger.mdx` | V1 user-facing guide published                      |
| Telegram                | ✅     | `telegram.mdx`           | Existing                                            |
| Crisp Chat              | ✅     | `crisp.mdx`              | Existing                                            |
| Slack                   | ✅     | `slack.mdx`              | V1 user-facing guide published                      |
| Twitter/X               | ✅     | `twitter.mdx`            | V1 user-facing guide published                      |
| LinkedIn                | ✅     | `linkedin.mdx`           | V1 user-facing guide published                      |
| TikTok                  | ✅     | `tiktok.mdx`             | V1 user-facing guide published                      |
| YouTube                 | ✅     | `youtube.mdx`            | V1 user-facing guide published                      |

### Productivity Tools

| Integration     | Status | File                  | Notes                                       |
| --------------- | ------ | --------------------- | ------------------------------------------- |
| Google Drive    | ✅     | `google-drive.mdx`    | Existing (Train With)                       |
| Google Calendar | ✅     | `google-calendar.mdx` | V1 user-facing guide published              |
| Google Sheets   | ✅     | `google-sheets.mdx`   | Ported from internal README; pending polish |
| Notion          | ✅     | `notion.mdx`          | V1 user-facing guide published              |

### Business Tools

| Integration      | Status | File               | Notes                          |
| ---------------- | ------ | ------------------ | ------------------------------ |
| MercadoLibre     | ✅     | `mercadolibre.mdx` | V1 user-facing guide published |
| Odoo ERP         | ✅     | `odoo.mdx`         | ERP integration exists         |
| Xubio Accounting | ✅     | `xubio.mdx`        | Accounting integration exists  |
| Zendesk          | ✅     | `zendesk.mdx`      | Existing                       |

### AI/Developer Tools

| Integration              | Status | File                | Notes                            |
| ------------------------ | ------ | ------------------- | -------------------------------- |
| Langchain                | ✅     | `langchain.mdx`     | Existing (External Integrations) |
| Evolution API (WhatsApp) | ⏳     | `evolution-api.mdx` | Alternative WhatsApp integration |

## Priority Order

### High Priority (User-Requested)

1. **WhatsApp QR** - ✅ Documented (v1)
2. **Instagram** - ✅ Documented (v1)
3. **Google Calendar** - ✅ Documented (v1)
4. **Google Sheets** - ✅ Documented (needs polish)

### Medium Priority (Complete Platform Coverage)

5. Facebook Messenger - ✅ Documented (v1)
6. Slack - ✅ Documented (v1)
7. Twitter/X - ✅ Documented (v1)
8. MercadoLibre (important for Latin America) - ✅ Documented (v1)

### Low Priority (Nice to Have)

9. LinkedIn - ✅ Documented (v1)
10. TikTok - ✅ Documented (v1)
11. YouTube - ✅ Documented (v1)
12. Odoo - ✅ Documented (v1)
13. Xubio - ✅ Documented (v1)
14. Notion - ✅ Documented (v1)

## Documentation Template

When creating new integration docs, use the template from `skills/bravilo-docs/SKILL.md`.

### Required Sections

1. Overview - What the integration does
2. Prerequisites - Account requirements, API access
3. Setup Steps - Obtaining credentials, configuration
4. Configuration Options - Table of settings
5. Usage Examples - Code snippets, screenshots
6. Troubleshooting - Common issues
7. Limitations - Known constraints

### File Location

```
apps/docs/integrations/[integration-name].mdx
```

### After Creating

1. Add to `mint.json` navigation
2. Link from related documentation
3. Create corresponding troubleshooting doc in `docs/troubleshooting/integrations/`

## Source Documentation

Existing documentation to reference when creating integration guides:

- **WhatsApp QR**: `docs/troubleshooting/whatsapp/*` (14 files)
- **Instagram**: `packages/integrations/instagram/` (9+ files)
- **Google Calendar**: `packages/integrations/google-calendar/` (8 files)
- **Google Sheets**: `apps/docs/integrations/google-sheets.mdx`
- **Other Integrations**: `packages/integrations/[integration]/README.md`

## mint.json Update

After creating integration docs, update `apps/docs/mint.json`:

```json
{
  "group": "🚀 Install On",
  "pages": [
    "integrations/whatsapp",
    "integrations/whatsapp-qr",
    "integrations/instagram",
    "integrations/facebook-messenger",
    "integrations/telegram",
    "integrations/crisp",
    "integrations/slack",
    "integrations/twitter"
    // ... etc
  ]
}
```

## Notes

- All integration code exists in `packages/integrations/`
- Most have basic READMEs but need user-facing documentation
- Troubleshooting docs can be consolidated from existing fix files
- Screenshots/GIFs should be added to `/images/integrations/`
