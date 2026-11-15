# SnapGrab

YouTube, Facebook, Instagram, TikTok আর X থেকে ভিডিও আর অডিও (MP3) ডাউনলোড করার Android অ্যাপ।

এই repo-তে শুধু অ্যাপের release ফাইল আর আপডেটের তথ্য (`update.json`) থাকে।

## ডাউনলোড

### 👉 [abulhasanatabdullah.github.io/snapgrab-releases](https://abulhasanatabdullah.github.io/snapgrab-releases/)

পেজটা খুলে **ডাউনলোড করুন** বোতামে চাপ দিন। ওই একটা ফাইলই (`SnapGrab.apk`) যথেষ্ট, বাকি ফাইলগুলো নামানোর দরকার নেই।

সরাসরি লিংক, যা সবসময় সর্বশেষ ভার্সন দেয়:
https://github.com/abulhasanatabdullah/snapgrab-releases/releases/latest/download/SnapGrab.apk

| ফাইল | কার জন্য |
|---|---|
| **`SnapGrab.apk`** | **প্রায় সবার জন্য। এটাই নিন।** |
| `SnapGrab-purono-phone-32bit.apk` | শুধু খুব পুরনো ফোনে, যদি উপরেরটা install না হয় |
| `SnapGrab-emulator-x86_64.apk` | কম্পিউটারের এমুলেটর বা Chromebook |
| `snapgrab-*-source.zip` | সোর্স কোড, ফোনে লাগে না |

Android 8.0 বা তার পরের ভার্সন লাগবে।

### Install

1. APK ফাইলটা ফোনে নামান, তারপর খুলুন।
2. ফোন "অজানা উৎস থেকে অ্যাপ install" করার অনুমতি চাইলে, যে অ্যাপ দিয়ে ফাইলটা খুলছেন (যেমন Chrome বা Files) তাকে অনুমতি দিন।
3. Install চাপুন।

অ্যাপ নিজেই নতুন ভার্সন খুঁজে নেয়, আর আপডেট এলে জানায়।

### APK আসল কিনা যাচাই

প্রতিটা release একই key দিয়ে sign করা। সেই certificate-এর SHA-256 fingerprint:

```
70:0F:C1:86:64:48:9C:F2:74:1E:39:92:7C:CE:BE:1B:6E:75:F1:BD:54:6B:24:22:DD:92:5A:D2:DC:4E:85:07
```

`apksigner verify --print-certs SnapGrab.apk` চালালে এই মানই আসার কথা। অন্য মান এলে ফাইলটা install করবেন না।

## সোর্স কোড

অ্যাপটা GNU GPL v3 license-এর অধীনে প্রকাশিত। প্রতিটা release-এর সাথে ওই ভার্সনের পূর্ণ সোর্স কোড (`snapgrab-<version>-source.zip`) দেওয়া থাকে।

অ্যাপে আরও যা ব্যবহার হয়েছে, নিজ নিজ license-সহ:
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) (Unlicense)
- [youtubedl-android](https://github.com/JunkFood02/youtubedl-android) (GPL-3.0)
- [FFmpeg](https://ffmpeg.org) (GPL build; সোর্স ffmpeg.org আর youtubedl-android-এর build থেকে পাওয়া যায়)
- Plus Jakarta Sans font (SIL Open Font License)

---

**English:** Android app for downloading video and audio. This repo holds only the release APKs and the in-app update manifest (`update.json`). Download page: https://abulhasanatabdullah.github.io/snapgrab-releases/ — `SnapGrab.apk` fits almost every phone. Signing certificate SHA-256: `700fc18664489cf2741e39927ccebe1b6e75f1bd546b2422dd925ad2dc4e8507`. Licensed under GPL-3.0; each release includes the full source of that version.
