# Exhibit 63 — Photo Library

Website-ready photographs for the [Marchand Puck Collection](https://tlpt.org/marchand.html).

Assets are organized by validated artifact number, not career goal number: `images/pucks/<artifact>/front.webp`, `back.webp`, and `edge-01.webp` onward. All supplied, confirmed edge views are retained. Front thumbnails are lossless; gallery images use quality-96 WebP, with transparency preserved and no upscaling.

Editing is non-generative. Puck wear, tape, lettering and authentication labels are preserved. Full-resolution masters and raw originals are stored separately, not in this public repository.

The collection's canonical database is the source of truth for mappings. A mistaken intake filename must not overwrite verified game details. Ambiguous physical artifacts are held until identified. Website gallery associations remain in the main website's `data/marchand-photos.json`; adding files here alone does not publish a gallery.

After an upload, verify deployed image bytes against `assets.json`, then publish the website manifest and test the live galleries. Only successfully published originals may move to the Drive archive.
