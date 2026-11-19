# StreamySpace

StreamySpace is a Windows app for moderating live streams. Put the streams and chats you care about side by side in one window: up to **4 livestreams** and **4 chats** from **Twitch, YouTube, TikTok, Facebook Live and Kick**. Combine several chats into one **Unified Chat** feed, let **Auto-Monitor** outline messages that may need a look, and use each platform's own moderation tools from the same window.

![StreamySpace 2-stream, 4-chat layout](screenshots/streamyspace-2-stream-4-chat-preview.png)

StreamySpace runs on Windows 10 and 11 (there is no Mac version) and needs the Microsoft Edge WebView2 Runtime, which most PCs already have.

## Beta testing

StreamySpace is in a closed beta on the Microsoft Store. Invited testers: please read the [tester guide](https://tanner-logan.github.io/StreamySpace-releases/tester-guide).

## Getting started

1. **Platform connections.** Sign in to the platforms you use. You can skip any of them. You can come back to this screen any time.
2. **Customize workspace.** Pick or create a workspace, add your livestreams and chats (paste a channel or video URL, or a username), choose a layout style, and press **Open moderation view**.
3. **Moderation view.** Your panes, laid out automatically. Use **Edit workspace** to change anything.

StreamySpace reopens your last workspace on launch.

| Platform | Livestream | Chat |
| --- | --- | --- |
| Twitch | ✅ | ✅ |
| YouTube | ✅ | ✅ |
| TikTok | ✅ | ✅ |
| Facebook Live | ✅ | ✅ |
| Kick | ✅ | ✅ |

## Free and Premium

StreamySpace has a Free plan and a Premium plan.

| | Free | Premium |
| --- | --- | --- |
| Livestream panes | Up to 2 | Up to 4 |
| Chat panes | Up to 2 | Up to 4 |
| Unified Chat (combined feed, moderation actions, Chat Identity themes) | No | Yes |
| Auto-Monitor | No | Yes |
| Connected accounts (Twitch, Kick, YouTube) | No | Yes |
| TikTok: hide follow, share and gift activity | No | Yes |
| TikTok For You pane | No | Yes |

## Workspaces and layout

- Keep as many workspaces as you like: **New, Duplicate, Rename, Delete, Export, Import**. Drag workspaces in the list to put them in your order.
- Layout styles: **Balanced, Chat focus, Stream focus**. StreamySpace re-arranges panes to fit your window as you resize it.
- In the moderation view, drag a pane's title to swap it with another pane, drag a column header to move a column, and drag the dividers to resize. Changes show a **CUSTOM** badge. **Save layout** keeps them, **Reapply layout** goes back to the saved arrangement.
- **Full screen** and **Reload all** are in the toolbar.

## Unified Chat

Combine two or more chats into one feed, in the order messages arrive.

- Turn it on with **Configure Unified Chat** on the workspace screen. You can have up to two groups.
- Each message shows its time, platform logo, the channel it came from and the user. Colours follow the platform.
- **Send to** lets you reply from the feed. Pick the platform (or the channel, when you have several) and type. The box border and placeholder show where your message will go, and nothing is ever sent to more than one platform. It uses your signed-in chat on that platform, so its own rules apply.
- Scroll up in the feed and it holds still, so you can click a message's **⋯** even in a very busy chat. New messages keep arriving below. Scroll back down, or click **Latest**, to follow the chat again. After a message is sent, a short "Sent to <platform>." appears and fades after a few seconds.
- The small face-with-glasses button next to **Send** opens **Chat Identity**: how your own name looks in the feed. It starts as champagne; pick any of eight themes (Champagne, Cosmic Rainbow, Golden Hour, Halloween, Christmas, Cosmic Space, Fire, Ice). Your own messages also get a glowing, tinted box in the theme's colours and a small animation in the corner that plays a few times and then rests.
- A message that replies to you or @mentions you is shaded green in the feed. StreamySpace finds your name from your sign-in on each platform by itself (nothing to set up); if it cannot, nothing is shaded.
- A Kick or Facebook reply shows a small "↪ replying to <name>" line above it (Facebook: English pages).
- Click a platform button above the feed to bring that platform's original chat to the front. The send box is greyed out while you do, so you can't send to the wrong place. Click **Unified** to return.
- The **⋯** on a message opens that platform's moderation options for it. Users you have timed out or banned from the feed are marked.

## Auto-Monitor

Auto-Monitor outlines chat messages that may deserve a closer look. It only highlights: it never bans, times out, hides or deletes anything.

- Outline colours: yellow (low), orange (medium), red (high), thick red (critical). Hover a message to see why it was flagged.
- Turn it on or off in the Moderation section of the workspace screen. It works on every chat pane and in Unified Chat.
- **Detection categories** let you switch each type on or off and set it to Low, Medium or High sensitivity: profanity, harassment, hate speech, threats, sexual harassment and spam. Spam covers flooding, repeated messages, all-caps, emote floods and suspicious links.
- **Auto-Monitor rules** lets you add your own words or phrases with a category and severity. They are added to the built-in rules, and you can test any message in the rules window.
- Everything runs on your PC. No AI services are used and no chat is sent anywhere.

## Moderation with your own account (optional)

Under **Connect accounts** you can connect your Twitch, Kick or YouTube account through each platform's official sign-in (a separate, optional step from signing in to watch and chat). Messages in Unified Chat then get a moderation menu to delete a message, time out, ban or unban a user. What you can do depends on your real permissions in that channel, and StreamySpace tells you when an action is not allowed. Disconnect at any time. Nothing is needed for viewing, chatting or Auto-Monitor.

## Good to know

- Chat panes are always muted, so a hidden video never plays sound.
- TikTok chat can hide follow, share, gift and Fan Club join messages, per pane.
- **TikTok For You** (Premium): in a livestream pane's platform list, choose **TikTok For You** to put your own For You page in the pane, using your TikTok sign-in. Only the feed and its controls are shown (no TikTok side menu), it fits the pane's width and height, and the controls, creator name and caption fade away while your pointer is off the pane so they do not cover the video. It counts as one of your livestream panes, a workspace can have one, and it stays silent until you first click or press a key in it. Like, comment, save, share and pause work as on TikTok.
- If your plan changes to one that allows fewer panes, every workspace is cut down to what the plan allows (the first panes of each kind are kept, in order; the others are removed). A workspace you import or duplicate has to fit your plan: one with more panes than your plan allows, or with a TikTok For You pane on a plan without it, is refused, and the message names what it uses.
- Facebook Live streams start muted when Facebook leaves them paused.
- StreamySpace checks that you are signed in for every platform you use. It cannot see whether you are a moderator, so confirm that on the platform.
- Platform websites change without notice. If a pane stops looking right, press **Reload all** or update StreamySpace.
- A **⚠** in a pane's header means StreamySpace could not set that page up, or that the channel is not live. Hover it to see why. It goes away by itself once the channel is live. Click it (or press **Copy diagnostics**) to copy a report you can send to the developer. The report has no chat messages, names, links or logins in it.
- The "channel is not live" warning works for every platform without signing in to anything. For Twitch, Kick and YouTube it asks the platform itself if you connected that account under **Connect accounts**, and otherwise StreamySpace's online service. That service receives only the platform and the channel name or video ID, and keeps no record of who asked. There is no switch for it; for Twitch, Kick and YouTube, connecting your account means the platform is asked directly and nothing goes to the online service.
- If a platform changes its page so StreamySpace cannot set a pane up, the pane shows an amber notice (and the toolbar a **⚠ pane needs attention** note). Press **Check for fixes** in it, **Reload**, or **Copy diagnostics** and send the report to the developer. A fix for a changed page can often arrive without a new version: StreamySpace downloads a small signed list of page selectors from the developer's website at start and every few hours (nothing about you is sent).
- Your data stays on this PC in `%LOCALAPPDATA%\StreamySpace`: settings, workspaces, custom rules and one separate browser profile per platform for your sign-ins. Deleting that folder resets the app.
- Coming from ModView? Your workspaces, rules and sign-ins move over automatically on first launch.
