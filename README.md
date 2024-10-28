# Quarto Background Music Extension For Quarto

This Quarto extension allows you to play an (unstoppable/unpauseable) background sound on your Quarto webpage (using the howler.js JavaScript library).

## Installing

```bash
quarto add melissavanbussel/quarto-background-music
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

After installing the extension in your project, use it via:

```
---
title: "My Document"
format: html
filters:
  - quarto-background music
---
```

In order for the music to play, you **must** create a folder in your project called `assets` and then place the audio file inside the folder, naming the audio file `audio.mp3`, and then add the following to your project's `_quarto.yml` file:

```
project:
  type: website

resources:
  - assets
```

Otherwise, the extension won't know where to find the audio file that should be used for the background music. 

## Example

Here is the source code for a minimal example: [example.qmd](example.qmd).