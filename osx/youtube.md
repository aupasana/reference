# Youtube


The following zsh function downloads the audio track from youtube as an 50Kbps m4a. It's useful for spoken content.

Prerequisites: Install yt-dlp via brew.

```zsh
function yt-m4a () {
    yt-dlp -f 139 --yes-playlist --download-archive archive.txt $1
}
```
