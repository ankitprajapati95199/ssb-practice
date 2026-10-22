# SSB Practice

A simple, timed practice website for the psychology tests of the SSB (Services Selection Board) interview: **PPDT, TAT, WAT and Lecturette**.

Built with plain HTML, CSS and JavaScript. No install, no libraries, no backend. Just one file, `index.html`.

**Live demo:** _add your GitHub Pages link here_

## Tests and timings

| Test | What you do | Timing |
|---|---|---|
| PPDT | View a picture, then write a story | 30 sec view + 4 min write |
| TAT | 12 slides (the last one is blank) | 30 sec view + 4 min write, per slide |
| WAT | 60 words, write a sentence for each | 15 sec per word |
| Lecturette | Choose 1 of 4 topics, then speak | 3 min prepare + 3 min speak |

A beep sounds when each timer ends, and the next step starts automatically.

## Features

- Four tests in one page
- Automatic countdown with a beep
- Pause / Resume and Skip buttons
- Random word order in WAT and random topics in Lecturette
- Works on phone and computer

## Project structure

```
ssb-practice/
├── index.html      (the whole website)
├── README.md
└── images/         (your pictures)
    ├── pic1.jpg
    ├── pic2.jpg
    └── ... up to pic11.jpg
```

## How to run

**On your computer:** download the files and open `index.html` in any browser.

**Online (free) with GitHub Pages:**
1. Upload all files and the `images` folder to a GitHub repository.
2. Go to **Settings > Pages**.
3. Under **Source**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. After about a minute, your site is live.

## Adding pictures

1. Create a folder named `images` next to `index.html`.
2. Add pictures named `pic1.jpg`, `pic2.jpg` and so on up to `pic11.jpg`.
3. PPDT shows one picture at random. TAT shows them in order, then a blank slide as number 12.

Use your own sketches or photos, or free-licence images from Unsplash, Pexels or Pixabay. Please do not upload copyrighted SSB test material.

## Customising

All settings are at the top of the `<script>` section in `index.html`.

**Change a timing** (in seconds):
```js
var viewTime = 30;
var writeTime = 240;
var wordTime = 15;
var prepTime = 180;
var speakTime = 180;
```

**Change words or topics:** edit the `words` and `topics` lists.

## How the code works

1. **Data:** the `words` and `topics` lists hold the content.
2. **Steps:** clicking a test button fills a `steps` list. Each step has a title, something to show and a number of seconds.
3. **Clock:** `showStep()` displays the current step and starts a timer. `tick()` runs every second and reduces the time left by 1.
4. **Next:** when the time reaches 0, the page beeps and `nextStep()` moves to the next step.

## Ideas for future improvement

- A box to type and save your story or sentences
- A Hindi version
- Group Discussion and Interview timers
- A score or streak tracker
- More topics and a bigger word list

## Contributing

Pull requests are welcome. You can add words, lecturette topics or new features. Open an issue if you find a bug.

## Disclaimer

This is an unofficial practice tool and is not connected to the Indian Armed Forces, the SSB or any official body. Timings are based on commonly followed practice and may differ slightly in the real test.

## License

MIT License. Free to use, copy and modify.
