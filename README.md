# Destiny STL Generator

A web application to generate 3D-printable STL files for thousands of weapons, armor, and ships from the Destiny universe.

This project uses the same mobile assets found on the official Destiny mobile app and the Bungie website to construct the 3D models.

## How it Works

The application is built with Python and the Flask web framework. It reads item and geometry data from pre-compiled JSON files to generate 3D models.

1.  The user selects an item for Destiny 1 or Destiny 2 from the main page.
2.  The Flask backend receives the request and uses the `DestinyModel` class to process the geometry.
3.  It generates an `.stl` file for the selected item.
4.  The user is then prompted to download the generated file.
5.  Generated files are cached on the server to speed up subsequent requests for the same item.

## Running Locally

To run the Destiny STL Generator on your local machine, follow these steps:

### Prerequisites

- Python 3.x
- `pip` for installing packages

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/destiny-stl-generator-web.git
    cd destiny-stl-generator-web
    ```

2.  **Create and activate a virtual environment:**
    - On Windows:
      ```bash
      python -m venv venv
      .\venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```bash
      python3 -m venv venv
      source venv/bin/activate
      ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the application:**
    ```bash
    python main.py
    ```

5.  Open your web browser and navigate to `http://127.0.0.1:5000` to view the application.

## Usage

1.  Navigate to the homepage.
2.  Select a game (Destiny 1 or Destiny 2).
3.  Use the search box to find the weapon, armor piece, or ship you want to generate.
4.  Click the "Generate" button.
5.  On the next page, click the download link for the `.stl` or `.zip` file.
6.  Import the file into your preferred 3D printing slicer or CAD software.

*Note: Some models may require cleanup. The site suggests using a service like [Microsoft 3D Tools](https://tools3d.azurewebsites.net/) for this purpose.*

## Disclaimer

This is a hobby project and is not financed by or associated with Bungie. All item models, names, and other assets are the property of Bungie.
