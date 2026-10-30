# Sonic

A browser-based music visualiser with multiple visual modes, colour options, track upload, playback controls, and a song list. `Sonicv2.html` is the main entry point. Visitors can choose an audio file through the upload control and use the available visual and playback controls. No package installation is required.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

    python -m http.server 8000

Then visit http://localhost:8000/Sonicv2.html.

Browser audio policies may require a direct user action before sound starts.

## Manual review checklist

These are actions to perform, not verified results:

- Open `Sonicv2.html` and review the visualiser, song list, and available controls.
- Try the visual modes and colour options. Observe how the display responds while audio is playing, if playback is available.
- Choose a non-sensitive audio file with the upload control, then try the playback controls. Check the visible response to selecting, playing, and pausing a track.
- Check any local image, audio, or other file paths referenced by the page against the files present. For a user-selected track, check the upload interaction in the browser rather than expecting a repository asset.
- Inspect the page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the visualiser, track list, and controls remain visible and usable.

## Accessibility review checklist

These are future review checks, not claims that accessibility has been verified:

- Navigate `Sonicv2.html` using only the keyboard. Check that the upload input, playback controls, song-list interactions, and visual mode and colour options can be reached and operated.
- Check for a clearly visible focus indicator on each focused control and confirm that focus order follows the page’s task flow.
- Check that playback, upload, mode, and colour controls have meaningful accessible names and that the selected track or playback state is communicated in text, not only by visual changes.
- Check text, control, and focus-indicator contrast against the page background and within the visualiser. Do not rely on colour alone to distinguish modes or states.
- If the page references images, check their alternatives in the HTML; if a visualiser conveys information not otherwise available, consider what text equivalent or status information a user would need.
- Check the visualiser with reduced motion enabled. Review whether its animation can be reduced or stopped, and whether the controls and track information remain usable without motion.

## Personalize the page

Use `Sonicv2.html` to review and edit the visible labels, song-list text, and page presentation. The page references Google Fonts; preserve those font links if you want to keep the current typefaces. Keep `Sonicv2.html` at its current location, or update any links that point to it if you rename or move it. If you add local assets, keep their paths aligned with their locations relative to the HTML file. Repeat the relevant manual review steps above after changes.