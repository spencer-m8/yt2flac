:: sources: 
:: https://www.reddit.com/r/audiophile/comments/yikkxn/converting_audio_file_types_with_ffmpeg_guide/
:: https://askubuntu.com/questions/95753/convert-lossless-m4a-to-flac
:: https://www.reddit.com/r/software/comments/1la096i/ytdlp_best_video_downloader_and_tips_on_how_to/

IF NOT EXIST flac\NUL mkdir flac_output

set /p url=Enter video url: 
yt-dlp -o "flac_output/%%(title)s.%%(ext)s" %url%  -f "bestaudio" --extract-audio --format m4a

for %%a in ("flac_output\*.m4a") do ffmpeg -i "%%a" -vn -f flac "flac_output\%%~na.flac"

@echo off
pause
