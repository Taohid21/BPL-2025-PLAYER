<!DOCTYPE html>
<html>
<head>
    <title>BPL 2025 LIVE PLAYER | TI SPORTS</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1"/>
    <script src="https://cdn.jsdelivr.net/clappr/latest/clappr.min.js"></script>
    <script src="https://cdn.jsdelivr.net/clappr.level-selector/latest/level-selector.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@clappr/hlsjs-playback@1.0.1/dist/hlsjs-playback.min.js"></script>
    <style>body { background-color: #000000; margin: 0; padding: 0; }</style>
</head>
<body>
    <div id="player" style="height: 100vh; width: 100%;"></div>

    <script>
        // Video source URL
        var sourceURL = "https://bdixtv24.site/tsports/stream.php?stream=https://live-cdn.tsports.com/live-02/master_1080.m3u8";

        // Debugging: Log the source URL
        console.log("Source URL:", sourceURL);

        // Initialize the Clappr player
        if (sourceURL) {
            var player = new Clappr.Player({
                source: sourceURL,
                width: '100%',
                height: '100%',
                autoPlay: true,
                plugins: [Clappr.HLS, LevelSelector],
                mimeType: "application/x-mpegURL",
                mediacontrol: { seekbar: "#ff0000", buttons: "#eee" },
                parentId: "#player",
            });
        } else {
            // Display an error message if the source URL is invalid or missing
            document.body.innerHTML = `
                <div style="color: white; text-align: center; margin-top: 20%;">
                    <h2>Invalid or Missing Video Source</h2>
                    <p>Please provide a valid video source URL.</p>
                </div>
            `;
        }
    </script>
</body>
</html># BPL-2025-PLAYER
