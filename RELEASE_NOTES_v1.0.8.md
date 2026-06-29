# Chzzk PotPlayer yt-dlp Installer v1.0.8

## 한국어

트위치 `twitch-potplayer-720p-fix` 방식으로 재생할 때 PotPlayer의 yt-dlp 확장이 Streamlink 주소를 잘못 가로채며 `[yt-dlp] CRITICAL ERROR`를 띄우는 문제를 수정했습니다.

- Twitch Streamlink의 `hls://`, `ttvnw.net` m3u8, `127.0.0.1`/`localhost` 로컬 HTTP 주소를 yt-dlp 확장에서 통과 처리합니다.
- 치지직용 기본값은 `live_chat=0`, `reduce_formats=1`, `critical_error=0`으로 유지합니다.
- 전체 m3u8 처리를 끄지 않고, Streamlink 경로만 좁게 제외합니다.
- 확인 스크립트가 Twitch Streamlink HLS/로컬 HTTP 통과 패치까지 검사합니다.

## English

Fixed `[yt-dlp] CRITICAL ERROR` appearing when Twitch is opened through the separate `twitch-potplayer-720p-fix` Streamlink flow.

- Passes through Twitch Streamlink `hls://`, `ttvnw.net` m3u8, and `127.0.0.1`/`localhost` local HTTP URLs in the PotPlayer yt-dlp extension.
- Keeps Chzzk defaults at `live_chat=0`, `reduce_formats=1`, `critical_error=0`.
- Avoids disabling all m3u8 handling; only the Streamlink path is excluded.
- Updates the check script to verify the Twitch Streamlink HLS/local HTTP passthrough patch.
