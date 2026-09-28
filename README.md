# Exhibit 63 — Photo Library

Website-ready photographs for the [Marchand Puck Collection](https://tlpt.org/marchand.html).

Assets are organized by validated artifact number, not career goal number: `images/pucks/<artifact>/front.webp`, `back.webp`, and `edge-01.webp` onward. All supplied, confirmed edge views are retained. Front thumbnails are lossless; gallery images use high-quality WebP, with transparency preserved and no upscaling.

Editing is non-generative. Puck wear, tape, lettering and authentication labels are preserved. Full-resolution masters and raw originals are stored separately, not in this public repository.

For storage optimization, test WebP quality 94, then 96 or 98 as needed against a lossless master at the published dimensions (or the preserved published original). Require exact alpha and unchanged dimensions, at least 41 dB opaque-RGB PSNR for faces and 42 dB for edges, and a minimum 2% size saving. Inspect close-ups of the lowest-scoring images for wear and label readability. Keep the original encoding when those checks fail. COAs and lossless front thumbnails remain unchanged. Existing PNG/JPEG files retain their original formats. Never rotate, resize, recolor, or retouch as part of compression.

The September 28 optimization reduces current published assets; it does not rewrite Git history or delete originals. The website keeps the per-file optimization audit in `data/marchand-image-optimization.json`.

The collection's canonical database is the source of truth for mappings. A mistaken intake filename must not overwrite verified game details. Ambiguous physical artifacts are held until identified. Website gallery associations remain in the main website's `data/marchand-photos.json`; adding files here alone does not publish a gallery.

After an upload, verify deployed image bytes against `assets.json`, then publish the website manifest and test the live galleries. Only successfully published originals may move to the Drive archive.
