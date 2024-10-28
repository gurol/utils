# utils
Various utilities, tools, and scripts by Gürol Canbek

# Convert Multiple Files to PDF and Merge in Finder: An Apple macOS Automator Workflow
The **Convert to PDF and Merge.workflow** script is an AppleScript-based Automator workflow designed to streamline converting multiple file types into PDFs and merging them into a single PDF document. This script is handy for MacOS users who need a quick and seamless way to batch convert and consolidate various document formats into one PDF. See the demo below.

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
2. Place the `Convert to PDF and Merge.workflow` in your Automator workflows folder (`~/Library/Services`, `/Library/Services`, and `/System/Library/Services`) or open it directly with Automator to customize or modify the workflow as needed.

## Usage
1. Run in Automator: Open the workflow in Automator and run it to process selected files.
2. Batch Conversion: Add multiple files of any supported format (see above) to the input. The workflow will convert each file to PDF if necessary and merge them into a single PDF.
3. Output: The output PDF file will be saved in the directory of the first input file and the name of the merged PDF is the parent folder name

## Example
To use this workflow in Finder:
1. Select multiple files (e.g., .docx, .jpg, .HTML).
<img width="912" alt="ConvertPDFandMerge_Demo_1" src="https://github.com/user-attachments/assets/53cd6959-c394-4e7e-a073-67b3ee680cbc">

2. Right-click, and navigate to Quick Actions > Convert to PDF and Merge (or the saved workflow name).
<img width="943" alt="ConvertPDFandMerge_Demo_2" src="https://github.com/user-attachments/assets/2e689052-8a26-4574-8387-53bbee2162d0">

3. Alternatively, enable preview by selecting `View | Show Preview` menu in Finder and then click `Convert to PDF and Merge` button at the Preview Panel.
<img width="428" alt="ConvertPDFandMerge_Demo_3" src="https://github.com/user-attachments/assets/2d5a71f4-022d-476b-a240-3a898e3202df">
<img width="743" alt="ConvertPDFandMerge_Demo_4" src="https://github.com/user-attachments/assets/0a25a901-a3c5-4192-81e2-14f4cd87d0a8">

4. A merged PDF containing each selected file will be created in the folder of the first selected file.
<img width="931" alt="ConvertPDFandMerge_Demo_5" src="https://github.com/user-attachments/assets/584f8c91-9557-4ec1-ae21-36dba7e4d9a1">

Some temporary PDF files are created during the process. They are erased at the end of the operation. Please wait for the process to be completed.

License
This project is licensed under the GNU General Public License v3.0 – you're free to use, modify, and distribute the code under the terms of this license.
