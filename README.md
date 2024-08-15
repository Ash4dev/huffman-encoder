# Huffman Encoding with Tkinter Interface
## Overview
This project implements Huffman Encoding for file compression and provides a user-friendly interface using Tkinter. Huffman Encoding is a lossless data compression algorithm that assigns variable-length codes to input characters, with shorter codes assigned to more frequent characters. This project enables users to upload a file, compress it using Huffman Encoding, and download the compressed file.

## Features
- File Upload: Upload your initial file through the Tkinter interface.
- Compression: Compress the file using Huffman Encoding.
- Download: Download the compressed file.

## Repository Structure
- logic: Contains the core compression logic and file type conversion utilities.
  - compressorDecompressor.py: Implements Huffman Encoding and decoding logic.
  - FileTypeParser.py: Handles conversion between PDF and intermediate text formats.
- ui: Contains the Tkinter-based user interface.
  - desktopApplication.py: Provides the graphical user interface for file upload, compression, and download.
- test: Contains sample files for testing different variations of the compression algorithm.

## Requirements
- Python 3.x
- Tkinter (usually included with Python)
- heapq module (standard library)
- collections module (standard library)
- PyPDF2 module (for PDF handling, can be installed via pip install PyPDF2)

## Installation
1. Clone the Repository
```
git clone https://github.com/Ash4dev/huffman-encoder.git
cd huffman-encoder
```
2. Install Dependencies
Ensure you have Python 3.x installed. Install any additional packages if required:
```
pip install PyPDF2
```
## Usage
1. Run the Application
```
python ui/desktopApplication.py
```
2. Using the Interface

  - Upload File: Click the "Upload File" button to select and upload the file you want to compress.
  - Compress File: The application will process the file and compress it using Huffman Encoding.
  - Download Compressed File: After compression, click "Download File" to save the compressed file.

## Implementation Details
### Huffman Encoding
The Huffman Encoding algorithm is implemented in compressorDecompressor.py and includes:

- BinaryTree Class: Represents nodes in the Huffman Tree.
- HuffmanCode Class: Contains methods for:
- __getTextFrequency(): Counts character frequencies.
- __buildHeap(): Builds a priority queue (heap) from character frequencies.
- __buildBinaryTree(): Constructs the Huffman Tree from the heap.
- __getBinaryCodeFromTree(): Generates binary codes from the Huffman Tree.
- __encode(): Encodes text into binary based on Huffman codes.
- __getPaddedCode(): Adds padding to the encoded text.
- __convertToBytes(): Converts the padded binary string into bytes.
- fileCompress(): Compresses the file and saves it with a .bin extension.
- __decode(): Decodes the compressed binary data.
- __removePadding(): Removes padding from the binary data.
- fileDecompress(): Decompresses the file and saves it as a .txt file.

### File Type Conversion

FileTypeParser.py provides functions for converting between PDF and text formats:
- pdf_to_txt(pdf_path, txt_path): Converts a PDF file to text.
- txt_to_pdf(txt_path, pdf_path): Converts a text file back to PDF.

### Tkinter Interface
The Tkinter interface is implemented in desktopApplication.py and includes:

- upload_file(): Handles file upload and compression.
- download_file(): Manages downloading of the processed (compressed) file.

## Example
Here's an example of how the application works:

1. Run ui/desktopApplication.py.
2. Click "Upload File" to select a text or PDF file.
3. Wait for the file to be compressed.
4. Click "Download File" to save the compressed file.

## Testing
Sample files for testing different variations are available in the test folder. Use these files to validate the functionality of the compression algorithm.

# Conclusion
Thank you for using the Huffman Encoding with Tkinter Interface project. Happy compressing!
