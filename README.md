JPG to WebP Converter



📌 Introduction

JPG to WebP Converter is a simple and efficient tool that allows users to convert JPEG/JPG images to WebP format, reducing file size without compromising quality. WebP is a modern image format developed by Google, offering superior compression and better performance for web applications.

🚀 Features

🔄 Fast & Efficient Conversion: Converts JPG images to WebP format in seconds.

📉 Reduced File Size: WebP images are 30-80% smaller than JPGs with the same quality.

🎨 Retains Image Quality: Supports lossless and lossy compression.

📂 Bulk Conversion: Convert multiple JPG files at once.

🖥️ Cross-Platform Support: Works on Windows, macOS, and Linux.

🔧 Adjustable Quality: Set compression level for optimal balance between size and quality.

📥 Installation

1. Install via npm (for Node.js users)

npm install -g webp-converter

2. Install cwebp (Command Line Tool)

Windows

Download WebP tools from Google Developers.

Extract and add the binary to your system PATH.

Mac/Linux

sudo apt install webp   # Debian/Ubuntu
brew install webp       # macOS

🔄 How to Use

1. Convert a Single JPG to WebP

cwebp -q 90 input.jpg -o output.webp

-q 90 → Sets quality to 90 (adjust as needed).

input.jpg → Replace with your source image file.

output.webp → Name of the converted WebP file.

2. Bulk Convert All JPGs in a Folder

Linux/macOS

for file in *.jpg; do cwebp -q 90 "$file" -o "${file%.jpg}.webp"; done

Windows PowerShell

Get-ChildItem -Filter *.jpg | ForEach-Object { & cwebp -q 90 $_.Name -o ($_.BaseName + ".webp") }

3. Convert Using Python (Automation)

Install Pillow library:

pip install pillow

Run the following script:

from PIL import Image
import os

input_folder = "images/"
output_folder = "webp-images/"

os.makedirs(output_folder, exist_ok=True)

for filename in os.listdir(input_folder):
    if filename.endswith(".jpg") or filename.endswith(".jpeg"):
        img = Image.open(os.path.join(input_folder, filename))
        webp_filename = os.path.splitext(filename)[0] + ".webp"
        img.save(os.path.join(output_folder, webp_filename), "WEBP", quality=90)

print("✅ Conversion complete!")

🌍 Why Use WebP Over JPG?

Feature

JPG

WebP

Compression

Lossy

Lossy/Lossless

Transparency

❌ No

✅ Yes

Animation

❌ No

✅ Yes

File Size

Larger

Smaller (~30-80%)

Browser Support

✅ Yes

✅ Yes (Modern Browsers)

📌 License

This project is open-source under the MIT License. Feel free to modify and contribute!

🤝 Contributing

Fork the repo

Clone the project: git clone https://github.com/yourusername/jpg-to-webp-converter.git

Create a feature branch: git checkout -b feature-name

Commit changes: git commit -m 'Add new feature'

Push to GitHub: git push origin feature-name

Create a Pull Request 🚀

📞 Contact


