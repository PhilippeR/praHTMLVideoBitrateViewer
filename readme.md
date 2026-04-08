# HTML Video Bitrate Viewer

A lightweight local tool to visualize per-frame bitrate from FFprobe JSON output when you can't install software.

Made with my friend claude ai

## Features

- Drop a `frames.json` file to load frame-level video metadata.
- Interactive chart with smoothed bitrate and individual I/P/B frame markers.
- Zoom, pan and unit switching between `kbps` and `Mbps`.
- Sliding window smoothing for clearer bitrate trends.

## Usage

1. Generate `frames.json` from your video file using FFprobe:

   ```bash
   ffprobe -v quiet -select_streams v:0 -show_frames -show_entries frame=best_effort_timestamp_time,pkt_size,pict_type -of json input.mp4 > frames.json
   ```

2. Open `index.html` in your browser.
3. Drop the generated `frames.json` into the viewer.
4. Adjust smoothing, toggle frame types, and explore the chart.

---

# Visualiseur de débit vidéo

Outil léger pour visualiser le débit par image à partir d'une sortie JSON FFprobe quand on ne peut pas installer de logiciel sur son pc.
Fait avec mon ami claude ai

## Fonctionnalités

- Glisser-déposer un fichier `frames.json` pour charger les métadonnées vidéo image par image.
- Graphique interactif avec débit lissé et marqueurs I/P/B.
- Zoom, panoramique et changement d'unité entre `kbps` et `Mbps`.
- Lissage par fenêtre glissante pour mieux voir les tendances de débit.

## Utilisation

1. Générez `frames.json` depuis votre fichier vidéo avec FFprobe :

   ```bash
   ffprobe -v quiet -select_streams v:0 -show_frames -show_entries frame=best_effort_timestamp_time,pkt_size,pict_type -of json input.mp4 > frames.json
   ```

2. Ouvrez `index.html` dans votre navigateur.
3. Déposez le fichier `frames.json` généré dans le visualiseur.
4. Ajustez le lissage, sélectionnez les types de frames et explorez le graphique.






