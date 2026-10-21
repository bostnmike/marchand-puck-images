# Exhibit 63 — Photo Library

Website-ready photographs for the [Marchand Puck Collection](https://tlpt.org/marchand.html).

Assets are organized by validated artifact number, not career goal number: `images/pucks/<artifact>/front.webp`, `back.webp`, and `edge-01.webp` onward. All supplied, confirmed edge views are retained. Front thumbnails are lossless; gallery images use high-quality WebP, with transparency preserved and no upscaling.

Editing is non-generative. Puck wear, tape, lettering and authentication labels are preserved. Full-resolution masters and raw originals are stored separately, not in this public repository.

For storage optimization, test WebP quality 94, then 96 or 98 as needed against a lossless master at the published dimensions (or the preserved published original). Require exact alpha and unchanged dimensions, at least 41 dB opaque-RGB PSNR for faces and 42 dB for edges, and a minimum 2% size saving. Inspect close-ups of the lowest-scoring images for wear and label readability. Keep the original encoding when those checks fail. COAs and lossless front thumbnails remain unchanged. Existing PNG/JPEG files retain their original formats. Never rotate, resize, recolor, or retouch as part of compression.

The September 28 optimization reduces current published assets; it does not rewrite Git history or delete originals. The website keeps the per-file optimization audit in `data/marchand-image-optimization.json`.

The collection's canonical database is the source of truth for mappings. A mistaken intake filename must not overwrite verified game details. Ambiguous physical artifacts are held until identified. Website gallery associations remain in the main website's `data/marchand-photos.json`; adding files here alone does not publish a gallery.

After an upload, verify deployed image bytes against `assets.json`, then publish the website manifest and test the live galleries. Only successfully published originals may move to the Drive archive.


## Current media ownership and retirement — October 20, 2026

Folder names are stable storage namespaces. They do not establish current artifact ownership. The canonical collection and `data/marchand-photos.json` establish ownership; preserve the following active mappings:

| Current artifact | Physical image namespace |
| --- | --- |
| 49 | `images/pucks/49-20220506/` |
| 57 | `images/pucks/76/` |
| 59 | `images/pucks/77/` |
| 61 | `images/pucks/61-20180123/` |
| 300 | `images/pucks/59/` |
| 301 | `images/pucks/343/` |
| 333 | `images/pucks/342/` |
| 342 | `images/pucks/49/` |
| 500 | `images/pucks/510/` |
| 709 | `images/pucks/717/` |

The historical former57 was consolidated into313. Current57 is the former76 puck, and current59 is the former77 puck. Current300 is the former343 Boston-return puck in physical59. The owner also moved510→500 and717→709. Retired76/77/343/510/717 have no active cards; their still-used source filenames remain legitimate current-owner namespaces. No duplicate images were created. The old `61/coa.webp` was the pre-crop source for current 330, and `68/coa-02.webp` was the pre-crop source for current 341. Their current approved crops remain active. Do not attach an old file merely because a reused artifact number matches its folder. The owner approved the October20 receipt photos for31/49/61 and game photoA. Their active namespaces are `31/`, `49-20220506/` and `61-20180123/`; use the normal full Back and COA views, with no isolated hologram images.

Unused public derivatives and retired COA associations were first archived with exact byte hashes and old-to-current lineage, then permanently deleted on the owner’s explicit instruction. The previous archive receipts are historical; those derivative rollback copies no longer exist. Actual source originals, native reproducible Book inputs, audit metadata and Git history remain preserved. The identical certificates at 613/614 are intentional and remain active. Inventory counts describe active media; historical manifests retain their original counts.

Before future releases, reconcile every artifact and run `node scripts/audit-marchand-media.mjs` in the website repository. To verify the image repository's actual files and hashes too, add `--image-host /absolute/path/to/marchand-puck-images`. Stage unapproved photos outside the active repositories.
