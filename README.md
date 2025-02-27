# Deep Dork Web

## Description
Deep Dork Web is a modern, browser-based tool designed to simplify and automate Google Dork searches for ethical security research. This web version provides an intuitive interface for performing advanced queries, filtering dorks by category, and seamlessly integrating with search engines like Google.

The tool is ideal for educational purposes, allowing users to explore predefined or custom Google Dorks without needing to manage dependencies or run scripts locally. It also includes features like real-time search filtering, dynamic query generation, and direct links to search results.

---

## Features
- **Advanced Google Dork Search**: Perform targeted searches using predefined or custom Google Dorks.
- **Dynamic Query Generation**: Replace placeholders (e.g., `{nome}`) in dork queries with user-provided input for personalized searches.
- **Category Filtering**: Filter dorks by categories such as "sensitive data," "vulnerabilities," or "misconfigurations."
- **Real-Time Search Results**: Instantly filter and display relevant dorks based on your search terms.
- **Search Engine Integration**: Generate direct links to Google search results for selected dorks.
- **Responsive Design**: A sleek, modern UI that works seamlessly on both desktop and mobile devices.
- **Educational Focus**: Includes a clear disclaimer emphasizing ethical use and legal considerations.

---

## Usage
### Accessing the Tool
1. Visit the hosted version of Deep Dork Web at [https://guilherme-moraiss.github.io/Deep-Dork-Web/](https://guilherme-moraiss.github.io/Deep-Dork-Web/).
2. No installation or setup is required—simply open the link in your browser to start using the tool.

### Performing Searches
1. **Enter a Search Term**:
   - Use the search bar to input keywords or phrases related to your query.
   - The tool will dynamically filter dorks based on your input.

2. **Filter by Category**:
   - Use the dropdown menu to narrow down results by category (e.g., "sensitive data" or "vulnerabilities").
   - Select "All categories" to view all available dorks.

3. **View Results**:
   - Matching dorks will appear below the search bar, displaying their query, category, and description.
   - Click on a dork to generate direct links to search engines like Google.

4. **Search with Generated Links**:
   - After selecting a dork, click on the generated link (e.g., "Google") to open the search results in a new tab.

---

## Ethical Considerations
This tool is intended for **educational purposes only**. Misuse of Google Dorking techniques may violate terms of service and legal regulations in some jurisdictions. Always ensure you have explicit permission before conducting reconnaissance or testing on any system.

A clear disclaimer is included at the top of the interface to remind users of the ethical implications of using this tool.

---

## File Structure
The project consists of the following files:
- **`index.html`**: The main HTML file containing the structure and styling of the web interface.
- **`dorks.json`**: A JSON file containing predefined Google Dorks categorized by type. Each entry includes:
  - `query`: The Google Dork query (with optional placeholders like `{nome}`).
  - `category`: The category of the dork (e.g., "sensitive data").
  - `description`: A brief explanation of the dork's purpose.
- **`assets/`** (optional): Folder for additional assets like images or icons (not included in the current version).

---

## Customization
### Adding New Dorks
To add new dorks to the tool:
1. Fork the repository from [GitHub](https://github.com/Diogo-Lages/Deep-Dork-Web).
2. Open the `dorks.json` file in the forked repository.
3. Add a new entry in the following format:
   ```json
   {
     "query": "site:example.com filetype:pdf {nome}",
     "category": "sensitive data",
     "description": "Searches for PDF files containing the specified keyword on example.com."
   }
   ```
4. Save the file and deploy your forked version using GitHub Pages or another hosting service.

### Modifying the Interface
- **Styling**: Customize the CSS in the `<style>` section of `index.html` to change colors, fonts, or animations.
- **Search Engines**: Add more search engines by modifying the `searchEngines` array in the JavaScript code:
  ```javascript
  const searchEngines = [
    { name: 'Google', url: 'https://www.google.com/search?q=' },
    { name: 'Bing', url: 'https://www.bing.com/search?q=' },
    { name: 'DuckDuckGo', url: 'https://duckduckgo.com/?q=' }
  ];
  ```

---

## Hosting Options
The tool is already hosted on GitHub Pages for public access. You can use it directly at [https://guilherme-moraiss.github.io/Deep-Dork-Web/](https://guilherme-moraiss.github.io/Deep-Dork-Web/).

If you'd like to host your own version:
1. Fork the repository from [GitHub](https://github.com/guilherme-moraiss/Deep-Dork-Web).
2. Enable GitHub Pages in your forked repository settings.
3. Share the hosted URL with others.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

**Note**: The web version of Deep Dork provides a streamlined and accessible alternative to the Python CLI tool. It eliminates the need for users to manage dependencies or run scripts locally, making it suitable for beginners and professionals alike while maintaining the core functionality of the original tool.
