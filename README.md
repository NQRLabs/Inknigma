<img alt="Inknigma-logo" src="./assets/images/logo.png" style="margin-left:auto; margin-right:auto; display:block; width:200px;"/>

# Inknigma

**Write in Invisible Ink**

Inknigma is a web-based tool for steganography, allowing you to hide secret messages or images within a base image. It uses a variety of encoding techniques to embed hidden data in a way that is difficult to detect with the naked eye. The tool also provides a suite of "lighting" effects, which are visual filters designed to reveal the presence of hidden data.

## Features

- **Load Base Image**: Start with any image as your canvas.
- **Hidden Layers**: Add multiple layers of hidden content, which can be text or other images.
- **Multiple Encoding Effects**: Choose from a curated list of steganography algorithms, including:
    - LSB (Least Significant Bit) manipulation
    - Hue and Chroma nudging
    - High-pass and local contrast watermarking
- **Interactive Controls**: Easily position, resize, and rotate your hidden layers directly on the canvas.
- **Strength Adjustment**: Control the intensity of the encoding effect for each layer.
- **Lighting Preview Mode**: Switch to a special viewing mode to test how different visual analysis techniques might reveal your hidden content. Includes over 170 different lighting effects.
- **Download Image**: Save your final encoded image as a PNG file.

### Info Panel Behavior

- In Encoding preview, the INFO panel shows Method Details for the currently selected hidden layer: the encoding method, brief background, and a recommended viewer.
- In Lighting preview, the INFO panel switches to Filter Details for the active detection filter: what the algorithm does, how it can elicit hidden information, and how to use it diagnostically. It also lists relevant parameters when applicable.
- The INFO panel updates live when you toggle preview modes, scroll through lighting effects (including Alt+Scroll group jumps), or jump to a filter via the input box.

## How to Use

1.  **Load a Base Image**: Click the "Load Base Image" button to select an image from your computer.
2.  **Add Hidden Layers**:
    - Click "Add Text" to create a new text layer. Type your secret message in the text box.
    - Click "Add Image" to hide an image within the base image.
3.  **Position and Style**:
    - Click and drag a layer to move it.
    - Use the handles to resize and rotate the layer.
    - Use the controls in the left panel to change the encoding effect, adjust its strength, or invert the content.
4.  **Preview**:
    - Click "Switch to Lighting Preview" to see how your image looks under various analytical filters.
    - Scroll while in lighting mode to cycle through different effects. Use Alt+Scroll to jump by effect groups, or enter an index to jump directly.
    - Lighting filters now apply even if you have no hidden layers added; the base image is processed directly in this mode.
5.  **Download**:
    - Once you're happy with your hidden message, click "Download Image" to save the result.

## Technical Details

Inknigma is a self-contained HTML file that runs entirely in your browser. It uses the Canvas API for image manipulation and does not require any server-side processing. All encoding and decoding happens locally on your machine.

The lighting effects are based on the detection methods used in tools like [Lucyra](https://nqrlabs.com/Lucyra/), providing a way to "red team" your own steganographic images.

### Controls & Shortcuts

- Pan: drag on the canvas (always in Lighting preview; hold Ctrl in Encoding preview)
- Zoom: Ctrl + Scroll (zooms to cursor)
- Change lighting effect: Scroll; Alt + Scroll to jump between effect groups
- Change layer effect: Scroll over a selected layer’s box
- Maintain aspect ratio when resizing: Shift + drag

Notes

- The transient 1-second popup when switching layer effects has been removed. Popups remain for other actions (loading files, adding layers, downloads, etc.).
