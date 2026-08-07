# Web Repository Manager (Homemade "Web FTP")

A lightweight, web-based file manager built with pure HTML, CSS, and JavaScript that connects directly to a GitHub repository using the GitHub REST API. This tool allows you to browse folders, create new directories, upload documents, and delete files directly through a web interface without needing a traditional FTP server.

## Features

* **Visual Directory Browsing**: Navigate through your repository folders and subpaths cleanly.
* **Document Uploading**: Drop or select files to upload them instantly into the current directory.
* **Folder Creation**: Automatically generates tracked directory structures using GitHub placeholder files (`.gitkeep`).
* **Client-Side Interface**: Runs entirely in the browser as a self-contained application or static page.

## Getting Started

### Prerequisites
* A GitHub account and a target repository (e.g., `ftp`).
* A GitHub **Personal Access Token (PAT)** with full `repo` scope permissions.

### Setup Instructions

1. Clone or download this project's code into an `index.html` file.
2. Open the file in any modern web browser.
3. Enter your connection credentials into the login interface:
   * **GitHub Username / Organization**: Your exact GitHub account or organization slug (e.g., `techgrid-systems` — ensure there are no spaces).
   * **Repository Name**: The target repository name (e.g., `ftp`).
   * **GitHub Personal Access Token**: Your generated API token with repo permissions.
4. Click **Connect to Repository** to start managing your files.

## Technical Details

* **API Integration**: Communicates via the `https://api.github.com/repos/{owner}/{repo}/contents/{path}` endpoints.
* **Authentication**: Utilizes Bearer token authorization headers.
* **Empty Folder Handling**: Because GitHub does not natively support empty folders, folder creation places a hidden `.gitkeep` file to maintain structural integrity within the repository tree.
