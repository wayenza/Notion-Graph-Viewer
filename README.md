# Notion Graph Viewer

A tool to visualize your Notion database as an interactive graph.

Created by [WebSim](https://github.com/websim)

## Table of Contents

- [Setup](#setup)
- [Usage](#usage)
- [Features](#features)
- [Customization](#customization)
- [Embedding in Notion](#embedding-in-notion)

## Setup

### Step 1: Prepare Your Notion Database

Ensure your Notion database has the following properties:

- **Title**: The main title of each page (default in Notion)
- **Tags**: A multi-select property for categorizing your pages
- **Links**: A relation property that links to other pages in the database

### Step 2: Export Your Notion Database

1. Go to the three-dot menu (...) at the top right of your database view
2. Select "Export"
3. Choose "Markdown & CSV" as the export format
4. Click "Export" and save the zip file

## Usage

### Step 3: Use the Graph Viewer

1. Open the Graph Viewer webpage
2. Click on "Import Notion Export" and select your exported zip file
3. The graph will generate, showing your pages as nodes and their connections

**Note**: The Graph Viewer is a separate tool and not a native Notion feature. You'll need to use it outside of Notion to visualize your data.

## Features

- **Zoom and Pan**: Use your mouse wheel to zoom in/out, and click and drag to pan around the graph
- **Node Selection**: Click on a node to see its details in the info panel
- **Multi-select**: Shift-click to select multiple nodes
- **Connect Nodes**: After selecting multiple nodes, click "Connect Selected Nodes" to create new connections
- **Search**: Use the search bar to find specific nodes

## Customization

To customize the appearance of your graph, modify the following code in the Graph Viewer:

```javascript
function getNodeColor(node) {
    switch(node.type) {
        case 'page':
            return '#61afef';
        case 'tag':
            return '#98c379';
        default:
            return '#c678dd';
    }
}
