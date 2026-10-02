# Privacy Policy – Live Subtitles — Speech Translator

_Last updated: 3 October 2026_

Live Subtitles is a browser extension plus a companion app that run entirely on your own computer.

## What the extension and companion app do with your data

- **Tab audio.** When you press "Start on this tab", the extension captures that tab's audio and sends it to a speech-recognition and translation server running **on your own PC** (address `127.0.0.1`, which never leaves your machine). The resulting text is shown as subtitles on the page. The audio and text are **not** sent to the developer, to any cloud service, or to any third party, and they are **not stored**: audio chunks exist in memory only while they are processed.
- **Settings.** Your language, appearance and server-port choices are saved in the browser's extension storage (`chrome.storage.local`) on your PC.
- **No accounts, no analytics, no advertising, no tracking.** The extension and the companion app do not collect personal information, usage statistics or crash reports.

## Network access

The only connections the software makes to the internet are:

1. **One-time model downloads** by the companion app from Hugging Face (`huggingface.co`) — the open-source speech models (Whisper) and translation models (Hy-MT2). Hugging Face may log standard request metadata such as your IP address, under its own privacy policy.
2. **Software installation** by the companion installer from public package sources (PyPI for Python packages, python.org and GitHub for the Python runtime and the llama.cpp translation engine).

No audio, subtitle text, or browsing information is included in any of these requests.

## Local-only server

The companion's server listens only on `127.0.0.1` and accepts requests only from this extension (it checks the request's origin and a per-session secret), so web pages you visit cannot use it.

## Permissions

The extension requests: `tabCapture` and `offscreen` (to process the audio of the tab you choose), `scripting` and `activeTab` (to show subtitles on that tab), `storage` (to save your settings) and `nativeMessaging` (to start and stop the local companion app). Each is used only for these purposes.

## Removing your data

Uninstall the extension from Chrome to remove its settings. Uninstall "Live Subtitles Companion" from Windows Settings → Apps to remove the app; the uninstaller offers to delete the downloaded models and logs.

## Changes and contact

If this policy changes, the date above is updated. https://github.com/wk-hoo/live-subs-releases/issues
