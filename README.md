# Free My TV Background Gallery

A public collection of background images for the [Free My TV](https://github.com/simbasjungles/free-my-tv) Tizen app.

The app reads `manifest.json` from this repository and uses the entries to populate its existing **Theme** selector. Each image is a separate theme option; **Carousel** rotates through the gallery images.

## Repository layout

```text
manifest.json
images/
  example-background.jpg
```

## Manifest format

The manifest is a JSON array. Each entry describes one background:

```json
[
  {
    "id": "example-background",
    "name": "Example Background",
    "url": "https://raw.githubusercontent.com/bezhynets/free-my-tv-background-gallery/main/images/example-background.jpg"
  }
]
```

- `id`: permanent, unique identifier. Keep it unchanged when renaming an image.
- `name`: display name shown in the Theme selector. It can be changed at any time.
- `url`: direct HTTPS URL of the image.

## Adding a background

1. Add the image under `images/`.
2. Give it a descriptive filename based on its stable ID.
3. Add an entry for it to `manifest.json`.
4. Commit both changes.

Use images that you have permission to publish. This repository is public, so anyone can view and download its contents.

## Compatibility notes

- Use direct HTTPS image URLs from `raw.githubusercontent.com`.
- Keep image dimensions and file sizes reasonable for an older Tizen TV.
- Do not rename an existing `id` just to change its display name.
