# utils
Various utilities, tools, scripts

# Convert to PDF and Merge: An Apple macOS Automator Workflow

The **Convert to PDF and Merge.workflow** script is an AppleScript-based Automator workflow designed to streamline converting multiple file types into PDFs and merging them into a single PDF document. This script is handy for MacOS users who need a quick and seamless way to batch convert and consolidate various document formats into one PDF.

## Features
- **Multi-format support**: Converts documents (`doc`, `docx`, `xls`, `xlsx`, `ppt`, `pptx`, `odt`, `ods`, `odp`, `rtf`, `txt`, `csv`) with **LibreOffice**.
- **HTML to PDF**: Converts HTML files using **wkhtmltopdf**.
- **Image to PDF**: Converts images (`jpg`, `jpeg`, `png`, `gif`, `bmp`, `tiff`) to PDF using **ImageMagick**.
- **PDF Merging**: Merges all converted files into a single PDF using **pdfunite**.

## Requirements

Before using this workflow, ensure the following dependencies are installed on your macOS system:
- **LibreOffice**: For document conversion.
- **wkhtmltopdf**: For HTML conversion.
- **ImageMagick**: For image conversion.
- **poppler** (provides `pdfunite`): For merging PDF files.

Install the necessary tools with:
```bash
brew install libreoffice wkhtmltopdf imagemagick poppler
```

## Installation
1. Clone the repository:
```bash
git clone https://github.com/gurol/utils.git
cd utils
```
2. Place the `Convert to PDF and Merge.workflow` in your Automator workflows folder or open it directly with Automator to customize or modify the workflow as needed.

## Usage
1. Run in Automator: Open the workflow in Automator and run it to process selected files.
2. Batch Conversion: Add multiple files of any supported format (see above) to the input. The workflow will convert each file to PDF if necessary and merge them into a single PDF.
3. Output: The output PDF file will be saved in the directory of the first input file and the name of the merged PDF is the parent folder name

Example
To use this workflow in Finder:
1. Select multiple files (e.g., .docx, .jpg, .html).
2. Right-click, and navigate to Quick Actions > Convert to PDF and Merge (or the saved workflow name).
3. A merged PDF containing each selected file will be created in the folder of the first selected file.

License
This project is licensed under the GNU General Public License v3.0 – you're free to use, modify, and distribute the code under the terms of this license.
