# Text Reader 🎙️

A modern and responsive web application that converts text to speech, allowing users to hear any text aloud with full control over playback speed.

## ✨ Features

- **Text-to-Speech**: Convert any text to audio using the browser's native Web Speech API
- **Speed Control**: Adjust playback speed from 0.5x to 2.0x for your convenience
- **Modern Interface**: Clean and responsive design with attractive visual gradient
- **Data Persistence**: Save text in the browser for later access
- **Play and Pause**: Full control over playback with intuitive buttons
- **Brazilian Portuguese Support**: Automatic detection and selection of pt-BR voices when available
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices

## 🚀 How to Use

1. Open the application in your browser
2. Type or paste the text you want to hear in the text field
3. Click the **Play** button (▶) to start reading
4. Use the slider to adjust the playback speed (0.5x to 2.0x)
5. Click the **Pause** button (⏸) to pause playback
6. Click the **Save** button (💾) to save the text in your browser

## 📋 Requirements

- Modern browser with Web Speech API support
- JavaScript enabled
- Node.js 18+ (for running the local Tailwind build step)
- Internet connection (to load analytics and icon CDN assets)

## 🛠️ Technologies Used

- **HTML5**: Semantic structure
- **CSS3**: Styles with backdrop-filter and gradient support
- **JavaScript**: Application logic
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide Icons**: Modern SVG icons
- **Web Speech API**: Native browser speech synthesis

## 📦 Dependencies

- [Tailwind CSS](https://tailwindcss.com/) - built locally from `src/tailwind.css`
- [Lucide Icons](https://lucide.dev/) - via CDN

## 🛠️ Local development & build

1. Install dependencies: `npm install`
2. Build the CSS bundle: `npm run build:css`
   - This command runs `tailwindcss -i src/tailwind.css -o assets/tailwind.min.css --minify`
   - The generated file is committed to the repository and must be rebuilt whenever you change Tailwind classes or configuration
3. Serve the site locally (e.g. `npx http-server` or `python -m http.server`) and open `http://localhost:8000`
4. Validate the interface on mobile and desktop viewports
5. Before publishing, rerun the build command to guarantee the CSS bundle is up to date

## 🚢 Publishing flow

1. Run `npm run build:css` to ensure `assets/tailwind.min.css` reflects the latest changes
2. Commit the generated CSS alongside your code changes
3. Publish the static files (including the updated CSS bundle) to your hosting provider or GitHub Pages
4. After deployment, execute a PageSpeed Insights test targeting the production URL to confirm the removal of the blocking Tailwind CDN script

## 💾 Local Storage

The application saves text in the browser's `localStorage`, allowing you to easily retrieve your content on future visits.

## 🎯 Available Voices

The application automatically tries to select a Brazilian Portuguese (pt-BR) voice if available on your system. If no pt-BR voice is found, the browser will use the system's default voice.

## 🌐 Supported Browsers

- ✅ Chrome/Chromium (version 25+)
- ✅ Firefox (version 49+)
- ✅ Safari (version 14.1+)
- ✅ Edge (version 79+)
- ⚠️ Opera (with partial support)

## 📝 Notes

- Voice quality depends on the voices available on your operating system
- Some browsers may have limitations on text length for speech synthesis
- Playback speed may vary depending on the browser and operating system

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

Carlos Henrique Bernardes

## 🤝 Contributions

Contributions are welcome! Feel free to open issues or pull requests for improvements and bug fixes.

## 💡 Usage Tips

- Use slower speeds (0.5x - 1.0x) for better comprehension
- Use faster speeds (1.5x - 2.0x) for quick review
- Save frequently used texts for quick access
- Test different voices on your system to find the one that works best

## 🐛 Troubleshooting

### Voice is not working
- Check that JavaScript is enabled in your browser
- Try reloading the page
- Make sure your browser has permission to use speech synthesis

### Save button is disabled
- The Save button only becomes enabled after starting playback
- Check that there is available space in your browser's local storage

### Text is not read completely
- Some browsers have a text length limit for speech synthesis
- Try dividing the text into smaller parts

---

**Enjoy the Text Reader! 🎉**
