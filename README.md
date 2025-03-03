# Remove Background with GrabCut

A web-based tool that uses OpenCV's GrabCut algorithm to remove backgrounds from images directly in the browser. Built with a dark theme, it includes a loading spinner for better user experience and allows users to download the processed image as a transparent PNG.

## Features
- **Background Removal**: Utilizes OpenCV.js and the GrabCut algorithm to separate foreground from background.
- **Dark Theme**: Clean, modern UI with a dark color scheme.
- **Loading Spinner**: Visual feedback during image processing.
- **File Upload**: Supports image uploads via a simple file input.
- **Download Option**: Export the result as a transparent PNG file.
- **Responsive Design**: Works well across different screen sizes.

## Demo
(Insert a GIF or screenshot here to showcase the tool in action. You can generate one by recording your screen and converting it to GIF using a tool like [EZGIF](https://ezgif.com/).)

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/remove-bg-grapcut.git
   cd remove-bg-grapcut
   ```
2. **Serve the Project**:
   - You can use a local server like [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) in VS Code, or run:
     ```bash
     python -m http.server 8000
     ```
   - Open your browser and navigate to `http://localhost:8000`.

3. **Dependencies**:
   - The project relies on `opencv.js`, which is loaded via a `<script>` tag in the HTML. Ensure you have an internet connection for the initial load, or host `opencv.js` locally by downloading it from the [OpenCV.js GitHub releases](https://github.com/opencv/opencv/releases) and updating the script source.

## Usage
1. Open the webpage in your browser.
2. Click the "Choose File" button to upload an image.
3. Once the image loads, click "Remove Background" to process it (a spinner will appear during processing).
4. After processing, the result will display on the canvas.
5. Click "Download PNG" to save the image with a transparent background.

## How It Works
- **OpenCV.js**: The tool uses OpenCV's JavaScript binding to perform image processing in the browser.
- **GrabCut Algorithm**: Automatically segments the foreground from the background based on a rectangular region.
- **Transparency**: The alpha channel is modified to make the background transparent, and the result is rendered on a canvas.

## Screenshots
Here are examples of the input and output using the tool:

| Input Image (1024x1024) | Output Image (1024x1024) |
|-------------------------|--------------------------|
| ![Input Image](example/input.png) | ![Output Image](example/output.png) |

## Contributing
Contributions are welcome! Feel free to:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

## Known Issues
- Large images may take longer to process due to browser limitations.
- The GrabCut algorithm may not perfectly segment complex backgrounds; manual refinement isn't supported yet.

## Future Improvements
- Add support for refining the mask manually (e.g., foreground/background markers).
- Optimize performance for larger images.
- Include additional image processing options (e.g., edge smoothing).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Built with [OpenCV.js](https://opencv.org/opencv-js/).
- Inspired by the need for simple, browser-based image editing tools.

---

### Notes:
- The images are displayed in a Markdown table for a clean side-by-side comparison, which GitHub renders nicely.
- Ensure the `example` folder with `input.png` and `output.png` is in the root of your repository and pushed to GitHub.
- Replace `your-username` with your actual GitHub username in the clone command.
- If you want to adjust the layout (e.g., stack the images vertically instead of a table), let me know, and I can tweak it!

