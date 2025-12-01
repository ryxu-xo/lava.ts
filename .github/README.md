# GitHub Actions Setup for lava.ts

This repository uses GitHub Actions to automatically send notifications to Discord.

## Setting Up Discord Webhook

1. **Create a Discord Webhook:**
   - Go to your Discord server
   - Right-click on the channel where you want notifications
   - Click `Edit Channel` → `Integrations` → `Webhooks`
   - Click `New Webhook`
   - Copy the webhook URL

2. **Add Webhook to GitHub Secrets:**
   - Go to your repository on GitHub
   - Click `Settings` → `Secrets and variables` → `Actions`
   - Click `New repository secret`
   - Name: `DISCORD_WEBHOOK_URL`
   - Value: Paste your Discord webhook URL
   - Click `Add secret`

3. **Done!** Now you'll receive Discord notifications for:
   - 🚀 **Pushes** to master/main branch
   - 🔀 **Pull Requests** (opened, closed, reopened)
   - 🎉 **Releases** (published)
   - 🐛 **Issues** (opened, closed)

## Notification Examples

### Push Notification
```
🚀 New Push to ryxu-xo/lava.ts
Commit: a1b2c3d
Message: Add Spotify recommendations to AutoPlay
Author: ryxu-xo
Branch: master
```

### Pull Request Notification
```
🔀 Pull Request opened
PR: #42 - Add voice region optimization
Author: contributor
Status: opened
Base: master ← Head: feature-branch
```

### Release Notification
```
🎉 New Release: v1.0.0
lava.ts v1.0.0 - Initial Release

Features:
- Plugin system
- AutoPlay with Spotify recommendations
- Loop modes, history, favorites
- And much more!

[View Release]
```

## Customization

Edit `.github/workflows/discord-notify.yml` to:
- Change notification colors
- Modify message formats
- Add/remove event types
- Customize bot name and avatar

## Logo (Optional)

To use a custom bot avatar, add a logo image:
1. Create `.github/assets/` folder
2. Add `logo.png` (512x512 recommended)
3. Commit and push

The workflow will automatically use it!
