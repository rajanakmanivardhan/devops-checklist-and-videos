# DevOps & Cloud Playlist Tracker

A single-file, no-dependency web app for tracking your progress through a 158-video DevOps and cloud YouTube playlist. Tick videos off as you finish them and watch your progress, hours watched and per-topic completion update instantly.

![Screenshot of the tracker](docs/screenshot.png)
<!-- Add a screenshot at docs/screenshot.png, or delete this line. -->

## Features

- **Real checkboxes** for every video, with finished rows highlighted and struck through
- **Live progress ring** showing percent complete and videos done out of 158
- **Hours tracking**: hours watched and hours left, out of roughly 102 hours of content
- **Next up card** that shows the first unfinished video in learning order, with a Watch button and a one-click Mark done
- **Per-topic progress bars** for all 15 topics; click a bar to jump to that section
- **Search** across video titles and topics
- **Filters** to show All, To do or Done
- **Collapsible topics** with "Mark all done" and "Clear topic" buttons
- **Direct links** to every video inside the original playlist
- **Responsive layout** for phones and desktops, with automatic light and dark mode
- **Saved progress** in your browser, with a two-click reset to avoid accidents

## Topics covered

Videos are arranged in a suggested learning order:

1. DevOps fundamentals and SDLC
2. Linux administration
3. Shell scripting
4. Networking
5. Git and GitHub
6. Python for DevOps
7. AWS
8. Azure
9. Docker and containers
10. Kubernetes
11. Terraform and Infrastructure as Code
12. Ansible
13. CI/CD and Jenkins
14. Monitoring and observability
15. AI-assisted DevOps

Within each topic, videos follow their original playlist order, and the `#` shown next to each title is its position in the playlist.

## Getting started

There is nothing to install or build.

1. Download or clone this repository.
2. Open `index.html` in any modern browser.

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
# then open index.html in your browser
```

> If your file is named `DevOps_Playlist_Tracker.html`, rename it to `index.html` so GitHub Pages can serve it automatically.

## Host it on GitHub Pages

1. Push the repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select your main branch and the `/ (root)` folder, then save.
4. After a minute or two, the tracker is live at `https://<your-username>.github.io/<your-repo>/`.

## How progress is saved

Progress is stored in your browser's `localStorage` under the key `devops-playlist-done-v1`, as a list of completed playlist positions.

- It stays on the device and browser where you ticked the videos, so it does not sync across devices.
- Clearing your browser data, or using a private window, will erase it.
- The **Reset progress** button at the bottom clears it (click twice to confirm).

## Customizing the playlist

All content lives in one `<script>` block near the bottom of the file, so you can adapt the tracker to a different playlist.

```js
const BASE = "https://www.youtube.com/playlist?list=...";   // playlist URL
const T = ["Topic one", "Topic two", /* ... */];            // topic names
const V = [                                                  // videos
  // [topicIndex, playlistPosition, "Title", durationInSeconds]
  [0, 1, "Day-1 | Fundamentals of DevOps", 1840],
];
```

- `topicIndex` is the zero-based position of the topic in `T`.
- `playlistPosition` is the video's number in the playlist; each link is built as `BASE + "&index=" + playlistPosition`.
- Videos appear in the order they are listed in `V`, and "Next up" follows that same order.
- If you change the video list, also change the `localStorage` key (`KEY`) so old saved progress doesn't clash with the new list.

## Project structure

```
.
├── index.html      # the entire app (HTML, CSS and JavaScript)
├── README.md
└── docs/
    └── screenshot.png   # optional
```

## Tech

- Plain HTML, CSS and vanilla JavaScript
- No frameworks, libraries, build step or network requests (apart from the YouTube links you click)
- Works in current versions of Chrome, Edge, Firefox and Safari

## Notes

- Video titles and durations come from a playlist snapshot taken on 20 Nov 2026. Video availability and durations on YouTube may change.
- All video content belongs to its original creators. This project only links to the public playlist and does not host or copy any videos.

## License

Add a license of your choice (for example [MIT](https://choosealicense.com/licenses/mit/)) and update this section.
