# LearnQuest

LearnQuest is a Chrome extension that turns YouTube lectures and playlists into a focused learning path. It adds a topic timeline, a course journey, and a small motivation system without replacing the YouTube player.

> The screenshots below show the real LearnQuest interface with a local sample playlist. The sample titles and progress are demonstration data, not claims about a real lecture.

## Screenshots

### Today: daily goal, checkpoints, XP, and achievements

![LearnQuest Today dashboard](docs/screenshots/today-dashboard.png)

### Course: playlist progress and the next lecture

![LearnQuest course journey](docs/screenshots/course-journey.png)

## Download and install

### Download ZIP

1. Open the [LearnQuest GitHub repository](https://github.com/rohansachinpatil/learnquest).
2. Choose **Code → Download ZIP**, then extract the archive.
3. In Chrome, open `chrome://extensions` and turn on **Developer mode**.
4. Choose **Load unpacked** and select the extracted LearnQuest folder—the one containing `manifest.json` and `content.js`.
5. Open or refresh a YouTube video. The LearnQuest button appears at the lower-right of the page.

### Clone with Git

```bash
git clone https://github.com/rohansachinpatil/learnquest.git
```

Then load the cloned folder through `chrome://extensions` → **Developer mode** → **Load unpacked**.

This folder contains the ready-to-load Manifest V3 extension; no build or API key is required.

## Use LearnQuest

1. Open a YouTube lecture or a video in a playlist.
2. Select the floating **LearnQuest** button on the video page.
3. In **Today**, use the `−` / `+` controls to set a goal of 1–8 completed lectures.
4. Watch normally. Each checkpoint completes only when LearnQuest records a lecture as completed (at least 90% watched, or the video ends); seeking over a section alone does not count.
5. Earn 25 XP for a completed lecture. Levels advance in 100 XP steps. Achievements unlock from recorded completions and study days.
6. Use **Timeline**, **Map**, and **Course** to revisit topics, jump to timestamps, and continue to the next available playlist video.

Daily goals, XP, achievements, playlist progress, and viewing history are stored locally by Chrome. Streaks are informational—there are no penalties for taking a break. The extension does not send transcripts or browsing history to a backend.

## Transcript and playlist notes

- LearnQuest uses visible YouTube chapters and timestamped description entries when available.
- Captions are observed while they are visible during playback. Caption availability depends on the video and the learner's caption settings.
- If a detailed timeline is unavailable, use **Transcript** to import an `.srt`, `.vtt`, or timestamped text file. LearnQuest does not fetch transcripts from an unofficial endpoint.
- Playlist entries are read from the playlist information rendered on the current YouTube page. Private, unavailable, or not-yet-rendered entries may be missing.
- The extension works on YouTube pages; it does not add a separate video player.

## Troubleshooting

- If the LearnQuest button is missing, confirm the extension is enabled and you're on `https://www.youtube.com/`, then refresh the page.
- If a playlist is not detected, open a video from the playlist or open its playlist page and allow YouTube's playlist entries to load.
- If no topics appear, check for chapters, turn on available captions while watching, or import a timestamped transcript.

## Privacy

LearnQuest uses the minimum `storage` permission and runs on YouTube pages. Learning records are saved in `chrome.storage.local` on this browser. No account, external AI service, or API key is needed.
