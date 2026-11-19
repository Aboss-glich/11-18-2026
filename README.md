# Alya — A Little World Made Just for You 💗

An eight-chapter birthday and friendship website for Alya, made by her friend Anmol. It uses HTML, CSS and vanilla JavaScript modules; there is no build step or package install.

## Run locally

Open the folder in VS Code and use Live Server on `index.html`, or run a local server from this folder:

```powershell
python -m http.server 8000
```

Visit `http://localhost:8000`. A local HTTP server is needed for ES modules. Opening pages directly through `file://` is not supported.

## Publish with GitHub Pages

This is a static site; there is no build command.

1. Create a GitHub repository and upload the contents of this folder to its root.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
4. Open the URL shown on the Pages settings screen after deployment finishes.

Before making the repository public, review the names, social links, photos, group avatars and messages in `config.js` and the image files in this folder. They will be publicly accessible; publish them only with the people’s permission. The playlist MP3 files are not included, so add audio you have permission to publish or leave the player without local songs.

## Birthday journey

`index.html` → `welcome.html` → `letter.html` → `memories.html` → `special.html` → `cake.html` → `gift.html` → `final.html`

The original eight pages, navigation, envelope, letter, photo lightbox, cake wish, gift, and finale are preserved. The Memories chapter keeps Instagram, Free Fire and the Anime Girls and Boys GC together. It now also includes a clickable friendship universe, time capsule, random-memory picker, GC Hall of Fame, saved easter eggs, a friendship quiz and a keyboard/touch-accessible memory book.

## Edit the birthday details

Change names, links, messages, memories, quiz answers, image paths and the playlist in one place: `config.js`.

- Alya: `recipientName`, `recipientNickname`, `birthdayDate`, `recipientInstagram`
- Anmol: `senderName`, `senderInstagram`
- Story and features: `friendshipMemories`, `memoryTimeline`, `memoryBookPages`, `groupMessages`, `surpriseMessages`, `timeCapsuleMessages`, `easterEggs` and `friendshipQuizQuestions`
- GC roster and wishes: `groupMembers` and `groupBirthdayMessages`. Only the names visible in the supplied screenshots are included. Replace or remove the transcribed GC wish if needed. Unknown birthdays remain empty/editable; no missing names or wishes are invented.
- Game: `gamingMemories` and `gamingLinks`. The game section uses original interface-inspired artwork, not fake match screenshots or statistics.
- Update Alya's or Anmol's Instagram profile in `recipientInstagram` or `senderInstagram`. External links open in a new tab.
- `firstMeetingDate` intentionally says **Around 27 May 2025**; confirm it before changing to an exact date.
- An optional `timeCapsuleUnlockDate` may be left blank. Its countdown is a browser-only presentation, not security or server enforcement.

## Alya's photographs

The supplied collages and birthday-story photo used by the scrapbook are in this folder and listed in `galleryPhotos`. Replace an image file or update `galleryPhotos`, `galleryCaptions` and `galleryDates` in `config.js` when changing the scrapbook. Dates not provided were not assigned.

To add a photo, copy it into this folder, give it a unique filename, add that filename (for example `alya-new-photo.jpg`) to `galleryPhotos`, and add a matching caption/date. Do not use stock photos as if they were Alya.

## Anime Girls and Boys GC screenshots and members

The small GC header icon and readable member avatars have been cropped from the supplied screenshots and are in this folder. The page uses the readable member names only. `groupMembers` and `groupBirthdayMessages` in `config.js` control names, avatar paths, badges and optional wishes. Add a uniquely named portrait here and set that member's `image` path; leave it blank if no real portrait is available. Replace a birthday wish only with a message you want included. The page does not recreate private chat threads.

Add any other screenshots to this folder with unique filenames, then add their filename to the appropriate configuration item. Gaming screenshots are still optional; add only genuine screenshots when available.

## Music playlist

The shared floating player appears on each website page. It supports a five-song playlist, previous/next, track selection, volume and visual feedback. **Playback never starts automatically.** Each chapter is a separate HTML page, so browsers may pause audio during navigation; the current track and position are remembered for that tab, and you can press play to resume on the next page.

The playlist is already configured for these filenames. **The MP3 files were not present in the project or the supplied local Downloads folder when the website was packaged**, so copy any music you have permission to publish into this folder with these names for playback:

- `happy-birthday-funk.mp3` — Happy Birthday Funk · E's Jammy Jams
- `happy-birthday.mp3` — Happy Birthday · E's Jammy Jams
- `birthday-cake.mp3` — Birthday Cake · Reed Mathis
- `look-at-me-now.mp3` — Look At Me Now · The Soundlings
- `birthday-party.mp3` — Birthday Party · half.cool feat. Jasmine Mangos

The track records and local filenames are editable in `musicTracks` in `config.js`. If a file is missing, the player remains usable and reports the missing local file. No audio files are created from external music.

## Flat project files

```text
index.html, welcome.html, letter.html, memories.html
special.html, cake.html, gift.html, final.html
*.css, *.js, *.png, README.md, .gitignore
```

All website files are kept together in the repository root; there are no asset, CSS or JavaScript subfolders. Give added photos and audio files unique names.

## Accessibility and preview

Semantic landmarks, visible keyboard focus, reduced-motion support, lazy-loaded photos, keyboard-operable gallery/dialog, touch/keyboard page turning and responsive controls are included. Fonts and optional GSAP/ScrollTrigger/Lucide enhancements use CDNs; if the network blocks them, local page styles and interactions still work.
