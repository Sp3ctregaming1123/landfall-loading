# Landfall loading screen

Static GMod loading page (sv_loadingurl). Fullscreen VP9/Opus WebM background with poster fallback,
amber ODST-style HUD driven by GMod's loading callbacks (GameDetails, SetStatusChanged, SetFilesTotal,
SetFilesNeeded, DownloadingFile).

- media/landfall_720p.webm  primary (VP9 + Opus, plays in GMod CEF 86 / CEF 137)
- media/landfall_720p.mp4   H.264/AAC fallback (normal browsers / GModPatchTool users only)
- media/poster.jpg          still shown before playback and on Awesomium (Linux main branch)
- Video plays once from 0:00, then loops only the drop-pod segment (from 1:42) with a fade through black.
- Audio: 0.3 x the player's in-game music volume (snd_musicvolume); AUDIO toggle top-right.
- Preview locally: index.html?demo=1 (fills fake loading data), &t=SECONDS to seek.

server.cfg:  sv_loadingurl "https://<host>/?map=%m&steamid=%s"

