# Interactive Function Visualizer

<p align="center">
  <img src="https://i.ibb.co/B2J3c5Xg/image.png" alt="Screenshot of the Interactive Function Visualizer" style="max-width: 100%;">
</p>

A web-based interactive node-based editor for visualizing and managing function flows. This application allows users to create, connect, and organize "function" nodes and group them for better organization, all within a draggable and zoomable canvas.

It's built entirely with HTML, CSS, and vanilla JavaScript, demonstrating a lightweight yet powerful approach to building interactive diagramming tools.

## ✨ Features

*   **Node Creation:** Easily add new function nodes to the canvas.
*   **Node Customization:**
    *   Rename functions.
    *   Change header colors.
    *   Add descriptions for better context.
    *   Dynamically add/remove input and output ports.
    *   Customize port names, data types (Number, String, Boolean, Vector, Object), and example values.
*   **Node Connections:**
    *   Connect output ports to input ports with visual bezier curves.
    *   Connections highlight on selection.
    *   Input ports can only have one incoming connection. Dragging a new connection to an occupied input port will replace the existing one.
    *   Type checking: Connections can only be made between ports of the *same data type*. (Implicitly handled by UI, future enhancement could add a visual indicator for invalid connections).
*   **Group Management:**
    *   Create groups to organize related nodes.
    *   Rename groups and change their background color.
    *   Move groups along with all contained nodes.
    *   Resize groups.
*   **Interactive Canvas:**
    *   **Pan:** Drag the canvas with the middle mouse button, or `Alt/Ctrl + Left Click`.
    *   **Zoom:** Use the mouse scroll wheel to zoom in and out.
*   **Selection & Deletion:**
    *   Select individual nodes, groups, or connections.
    *   Press `Delete` to remove the selected item.
*   **Persistence:**
    *   **Auto-Save:** Your project state is automatically saved to your browser's `localStorage` as you work.
    *   **Auto-Load:** The application will automatically load your last saved project when you revisit the page.
    *   **Manual Save/Import:** Export your project as a `.json` file or import a previously saved `.json` file.
    *   **New Project:** Clear the current workspace and start fresh.

## 🚀 How to Use

1.  **Clone or Download:** Get the `index.html` file (and potentially the `README.md` if you want to keep it).
2.  **Open in Browser:** Open the `index.html` file directly in any modern web browser (Chrome, Firefox, Edge, Safari). No server required!

### Basic Interactions:

*   **Create Node:** Click "New Function" button in the left panel.
*   **Create Group:** Click "New Group" button in the left panel.
*   **Move Node/Group:** Click and drag the header of a node or group.
*   **Connect Nodes:**
    1.  Hover over a port connector (the small circle).
    2.  Click and drag from an **output** port.
    3.  Drag the connection line to an **input** port of a compatible type and release.
*   **Edit Properties:** Click on a node, group, or connection to select it. The "Inspector" panel on the right will update with editable properties.
*   **Pan Canvas:** Middle-click and drag, or `Alt/Ctrl + Left Click` and drag.
*   **Zoom Canvas:** Use the mouse scroll wheel.
*   **Delete Item:** Select a node, group, or connection, then press `Delete` or `Backspace`.
*   **Save Project:** Go to `File > Save Project As...` to download your work as a `.json` file.
*   **Load Project:** Go to `File > Import Project` and select a `.json` file you previously saved.
*   **New Project:** Go to `File > New Project` to clear the current workspace.
*   **Auto-Save:** Your changes are continuously saved to your browser's local storage.

## ⚙️ Technical Details

This application is built as a single `index.html` file, demonstrating a self-contained web application.

*   **HTML5:** Structure of the application.
*   **CSS3:** Styling, including a dark theme, custom fonts (`Nunito`), and subtle animations.
*   **Vanilla JavaScript:** All interactivity, including:
    *   DOM manipulation for creating and updating nodes, groups, and ports.
    *   Event listeners for drag-and-drop, selection, keyboard shortcuts.
    *   SVG for drawing dynamic bezier curve connections.
    *   Canvas transformations (pan and zoom) applied using CSS `transform` property.
    *   Local Storage API for persistence.
    *   File API for import/export functionality.

### Project Structure (Conceptual)
