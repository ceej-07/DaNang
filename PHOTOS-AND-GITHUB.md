# Add Unsplash photos and publish on GitHub

## 1. How the photos work
`index.html` shows one photo per day from the `photos` folder, with a caption and credit line. If a file is missing, that photo is hidden, so nothing breaks while you collect them. Saving the photos into your own folder (instead of linking to Unsplash) keeps the site fast and working even if a link changes.

The Unsplash License lets you use photos for free, including in a project like this, without asking permission. Crediting the photographer is not required but is appreciated, and the site already has a credit line for it.

## 2. Find and download the photos
On each photo's page, use the Download button and choose a medium size (about 1600 px wide keeps the site light).

| Save as (in `photos/`) | Search Unsplash for |
|---|---|
| day1-dragon-bridge.jpg | https://unsplash.com/s/photos/dragon-bridge-da-nang |
| day2-golden-bridge.jpg | https://unsplash.com/s/photos/golden-bridge |
| day3-hoi-an.jpg | https://unsplash.com/s/photos/hoi-an-ancient-town |
| day4-lady-buddha.jpg | https://unsplash.com/s/photos/lady-buddha-da-nang |
| day5-marble-mountains.jpg | https://unsplash.com/s/photos/marble-mountains-da-nang |
| day6-my-khe-beach.jpg | https://unsplash.com/s/photos/my-khe-beach |

One photo I found that fits Day 2 (Golden Bridge, by Andreea Popa): https://unsplash.com/photos/people-walking-on-bridge-during-daytime-PknaOrb1lVo
The Golden Bridge and Hoi An search pages were confirmed to exist. The other search links follow Unsplash's usual pattern, so if one comes up empty, type the place name into Unsplash's search box.

Tips: choose bright, landscape (wide) photos, and skip any marked Unsplash+ (those are paid).

## 2b. Motion scenes: real photos and video instead of drawings
Each animated scene now uses a real photo (and optionally a real video clip) from the `photos` folder. Save these:

| File | What to look for |
|---|---|
| scene-plane.jpg | airplane window view, clouds or coastline |
| scene-cable.jpg | cable car over misty mountains |
| scene-car.jpg | van or road trip on a Vietnamese road |
| scene-boat.jpg | Hoi An river, basket boat or Han River |
| scene-walk.jpg | friends walking through a street or market |

Search Unsplash for the photos, and Pexels or Pixabay for free video. For a video, save a short muted clip as `scene-plane.mp4` (same name, `.mp4`). If a video is there, the site plays it. If not, the photo moves like a camera: pan, forward zoom, walking bob or boat sway. A route bar fills as the "trip" progresses. Keep clips under about 8 MB.

## 3. Add credits
In `index.html`, find the `PH` list and put each photographer's name as the third item:
`['photos/day3-hoi-an.jpg','Hoi An Ancient Town','Their Name']`
The Day 2 entry already says Andreea Popa, so change it if you use a different photo.

## 4. Publish on GitHub Pages (free)
1. Sign in at github.com and click **New repository**. Name it `danang-trip-2026` and set it to **Public**. (Free GitHub Pages needs a public repo.)
2. On the repository page choose **Add file > Upload files**. Drag in `index.html` and the whole `photos` folder (with your photos and videos inside), then click **Commit changes**.
3. Open **Settings > Pages**. Under Source choose **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then Save.
4. Wait 1–2 minutes. Your link will be `https://YOUR-USERNAME.github.io/danang-trip-2026/`. Share it with the group.

To update later, open a file on GitHub, click the pencil icon, edit, and commit. The site refreshes in a minute or two.

Command-line version, if you prefer:
```
git init
git add .
git commit -m "Da Nang trip site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/danang-trip-2026.git
git push -u origin main
```

## 5. Keep it safe
A public repo means anyone with the link can see it. Leave out passport details, booking numbers, hotel confirmations and flight reference codes.
