# StreamySpace Privacy Policy

**Effective date:** November 17th, 2026  
**Provider:** StreamySpace  
**Contact:** TannerLogan23@gmail.com

## The short version

- StreamySpace is a Windows app that runs on your PC. Your workspaces, settings, sign-ins and connected accounts stay on your PC.
- There are no StreamySpace user accounts. We do not collect your name, your email, the chat messages you moderate, or your viewing or moderation history.
- Chat text is never sent to us. Auto-Monitor runs on your PC and uses no AI service.
- Two small things do reach our online service: a sign-in helper for Kick and Google, and, when no account is connected and "Warn when a channel is not live" is on, the platform and channel name (or YouTube video ID) of a pane. Sections 3 and 6 explain both and how to switch them off.
- You can disconnect accounts, switch features off and delete everything the app keeps (section 6).

## 1. What stays on your PC

The app keeps its files in a folder under your Windows user profile: `%LOCALAPPDATA%\StreamySpace` (the StreamySpace Beta tester build uses a separate folder, `StreamySpace.Beta`, so it never shares data with the regular app). We have no access to them.

- **Settings and workspaces:** your panes (the channel links or names you typed), layouts and preferences.
- **Your Auto-Monitor rules:** the phrases you add.
- **Your plan choice (tester builds only):** the StreamySpace Beta has a switch that lets testers pretend to be on the Free or the Premium plan. Which one you picked is saved in your settings file on your PC. Nothing is sent anywhere.
- **Browser sign-ins:** one browser profile per platform (Twitch, YouTube, TikTok, Facebook, Kick) holding the cookies of the sites you sign in to. They are kept by the Microsoft Edge WebView2 runtime, in the same way a browser keeps them.
- **Connected accounts:** if you connect a Twitch, Kick or YouTube account, the access tokens are stored protected by Windows data protection, so only your Windows account on this PC can read them.
- **An error log** (`logs\streamyspace.log`): technical errors only. It does not contain chat text, user names, channel names, links, cookies or tokens. A link is reduced to its site name, token-like text is removed, and your Windows user name is replaced.
- **A diagnostics report:** created only when you press "Copy diagnostics". It goes to your clipboard and is shared only if you paste it somewhere. It lists the app and Windows versions, what each pane is doing, whether you are signed in and whether API accounts are connected, a few settings and the latest log lines. It contains no chat text, names, channel names, links or logins.

## 2. What goes to the platforms, directly from your PC

- **Platform pages.** StreamySpace shows each platform's own web page (Twitch, YouTube, TikTok, Facebook, Kick) in an embedded browser and adjusts how it looks. These pages talk to the platforms exactly as they would in a browser, under each platform's own privacy policy. We do not see that traffic.
- **Connected accounts (optional).** If you connect an account (the **Connect accounts** button), it uses that platform's official sign-in. The permissions requested are:
  - Twitch: `moderator:manage:banned_users`, `moderator:manage:chat_messages`, `user:read:moderated_channels`.
  - Kick: `user:read`, `channel:read`, `moderation:ban`, `moderation:chat_message:manage`.
  - YouTube: `https://www.googleapis.com/auth/youtube`.
    They are used to confirm which account is connected, to delete a message or time out, ban or unban a user **when you choose to**, to check whether a channel is live, and (Kick) to look up a channel's ID. These requests go from your PC to the platform. We do not receive your messages or moderation actions.
- **Twitch chat connection.** For Twitch chat panes that are part of a Unified Chat group, the app also opens a direct, read-only connection from your PC to Twitch's chat server, the same kind of connection other chat readers use. It signs in anonymously with a random temporary nickname: no account, password or token is sent, and it cannot write or moderate. It sends only the Twitch channel names you are watching (so Twitch can send you that chat), and receives the public chat messages. It goes from your PC to Twitch under Twitch's own privacy policy; nothing goes to us. It is used so Unified Chat and Auto-Monitor read messages reliably; the pane's web page is still shown as before.
- **Creator names.** To show a YouTube channel's name, the app asks YouTube for the public details of the video (by its public video ID).
- **Downloads.** The installer is downloaded from GitHub, which sees the download request under its own privacy statement. The StreamySpace Beta is installed through the Microsoft Store, which handles the download, updates and its own records under [Microsoft's privacy statement](https://privacy.microsoft.com/privacystatement). We do not receive the Store's records about you.

## 3. What goes to our online service

We run a small online service on Cloudflare (`streamyspace-kick-token.streamyspace.workers.dev`, to be moved to a streamyspace.io address). It does two things.

**a) Sign-in help for Kick and Google (YouTube).** Kick and Google require a secret to complete sign-in. We keep it on our server instead of inside the app, where anyone could extract it. When you connect one of those accounts, or when its connection is renewed, the one-time sign-in code or renewal token passes through our service to Kick or Google, and the answer comes back to your PC. Our service does not store or log them. Twitch sign-in does not use our service.

**b) "Is this channel live?"** When "Warn when a channel is not live" is on, and you have not connected that platform's account, the app asks our service whether a channel is live. It sends only the **platform and the channel name** (a Twitch or Kick channel name) **or the YouTube video ID**, never a link and never anything about you. Our service asks the platform using our own credentials and answers. Answers are kept for a short time and shared, and are not tied to you. We do not store who asked. The network address of a request is used only briefly, in memory, to limit abuse, and is not stored by us. Cloudflare, our hosting provider, processes the requests technically and may keep its own records under its own policy ([Cloudflare privacy policy](https://www.cloudflare.com/privacypolicy/)).

If you would rather not use it, untick **Warn when a channel is not live** (nothing is then asked, and those warnings are not shown), or connect your account so the platform is asked directly.

The app has no analytics, no advertising and no crash-reporting service.

## 4. What we do not do

- We do not collect or store chat messages, the names of chat participants, or your viewing or moderation history.
- We do not sell your data.
- We do not use AI services. Auto-Monitor runs on your PC and only highlights messages for you to review. It never bans, times out, hides or deletes anything.
- We do not share data with anyone other than the platforms you use, Cloudflare (hosting) and GitHub (downloads), as described above.

## 5. Google and YouTube

StreamySpace's use and transfer to any other app of information received from Google APIs will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

We use YouTube access only to provide the moderation and live-status features you ask for. We do not use it for advertising, we do not sell it, and we do not transfer it to others. The access tokens stay on your PC, and our service does not store them. By using YouTube features you agree to be bound by the [YouTube Terms of Service](https://www.youtube.com/t/terms), and Google's use of data is described in the [Google Privacy Policy](https://policies.google.com/privacy). You can withdraw StreamySpace's access at any time at https://myaccount.google.com/permissions.

## 6. Your choices and deleting your data

- **Disconnect an account:** in the app, open **Connect accounts** and choose **Disconnect**. The token is removed from your PC and the platform is asked to cancel the authorization. You can also remove StreamySpace in the platform's own settings: Twitch (https://www.twitch.tv/settings/connections), Google (https://myaccount.google.com/permissions) and Kick (connected apps in your account settings).
- **Stop live-status lookups:** untick **Warn when a channel is not live**.
- **Remove everything the app keeps:** uninstall StreamySpace, then delete its data folder (`%LOCALAPPDATA%\StreamySpace`, or `%LOCALAPPDATA%\StreamySpace.Beta` for the Beta) if it is still there.
- **Our side:** because we do not hold personal data about you, there is nothing of yours for us to access, correct or delete. If you have a privacy question or request, email TannerLogan23@gmail.com.

## 7. Security

API tokens are protected by Windows data protection. The secrets needed for Kick and Google sign-in are kept on our server, not in the app. The app talks to our service over HTTPS, and the service accepts only a plain platform, channel name or video ID and refuses anything else. No system is perfectly secure, so we cannot guarantee absolute security.

## 8. Children

StreamySpace is not directed to children under 13. The platforms it works with have their own age rules.

## 9. Paid plans

**StreamySpace Beta is free.** It has no payments, no licenses and no accounts. The Free / Premium switch in the Beta only lets testers see what each plan would include; it buys nothing and sends nothing.

If paid plans are ever offered, this policy will be updated first to say how payments and licenses work.

## 10. Where data is processed

StreamySpace runs on your PC. Our small online service runs on Cloudflare's global network, so the few requests described in section 3 may be handled in data centers in different countries. We do not store personal data about you, so there is nothing about you for us to transfer or keep. Cloudflare may keep its own technical records under its own policy (section 3).

## 11. Changes to this policy

We will post changes here with a new effective date. If a change is significant, we will say so in the release notes.

## 12. Contact

TannerLogan23@gmail.com
