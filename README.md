![logo](logo.png)
# Bondi Secure DJVU to PDF Converter

This program offers a groundbreaking solution to decode and convert Bondi Secure DJVU files to PDF format. Originally developed by Bondi Digital Publishing, the Bondi DJVU format was a unique archive format based on Celtartem's "Secure DJVU" standard. A primitive version of Bondi DJVU made its first appearance in the New Yorker collection and a more robust implementation was later used in the Playboy and Rolling Stone collections, before eventually becoming obsolete when the company ceased operations. This tool breathes new life into the cherished content, making it accessible on modern operating systems by converting it to the widely supported PDF format.

## Warning
Running from source requires 32-bit Python 3.10. It will not work with 64-bit Python versions because it must access 32-bit DLL files. The binary release should work on all Windows systems. Additionally, the script requires certain DLL files to operate correctly (they must be located in the same directory as the script). These are included with the binary release download but you can also obtain them yourself as noted below. Be aware that if you simply clone the repo and immediately try to run the script with python it will not work. Feel free to open an issue if you have problems.

It is recommended that you copy the DJVU files from the Playboy DVD's to your local file-system first, and then convert the local copies. Converting the files directly from the DVD can result in errors.

Please note that this program will **not** work for the Rolling Stone or New Yorker collections. This will convert the DJVU files from [Playboy: Cover to Cover](https://www.amazon.com/Playboy-Cover-50s-Searchable-Archive-Every/dp/0979526116/) only. To convert the DJVU files from [Rolling Stone: Cover to Cover](https://www.amazon.com/Rolling-Stone-Cover-First-Years/dp/0979526108/), you will need to use the companion tool found [here](https://github.com/reconSuave/RollingStoner). I have also figured out how to convert the New Yorker collection and I will have a repo up soon with a working tool. 

### Required DLL Files
- `msvcr71.dll`
- `msvcp71.dll`
- `System.Drawing.dll`
- `BondiReader.DJVU.dll` (This is a crucial file found in the "Playboy: Cover to Cover" installation directory, typically located at `C:\Program Files (x86)\Bondi\Playboy - Cover to Cover\BondiReader.DJVU.dll`. The DLL file must be copied to the same directory as the Python script.)

## Getting Started

### Using the Compiled Binary (Recommended)
The easiest way to use this software is to [download](https://github.com/reconSuave/PlayboyPDF/releases/download/v1.1/PlayboyPDF-v1.1.zip) the compiled binary (.exe) file from the GitHub Releases page. This binary is compatible with all Windows systems and has been compiled with Nuitka using the `--standalone` and `--onefile` flags for ease of use. However, the aforementioned DLL files must still be located in the same directory as the executable for the program to function. Download from the versions page on the right-hand menu and extract the contents of the zip file. To use the compiled binary, follow the syntax below:

```shell
cd <path to playboy_to_pdf.exe parent directory>
.\playboy_to_pdf.exe <path to DJVU file or directory> --output_dir <output directory>
```
### Running From Source
To run the script from source, ensure you have 32-bit Python 3.10 installed. The same DLL files mentioned above must be in the same directory as the script. Here's a brief overview of how to set it up:

1. Ensure you have 32-bit Python 3.10 installed.
2. Place the required DLL files in the same directory as the script.
3. Run the script via the command line or another Python environment that supports Python 3.10-32.

## Usage
The program can process single DJVU files or entire directories containing DJVU files. There are two required dependencies. Both are stable packages with no history of shenanigans. To install the dependencies, use the following code in Windows:

```shell
python -m pip install Pillow fpdf
```

To use the program, follow the syntax below:

```shell
python playboy_to_pdf.py <path to DJVU file or directory> --output_dir <output directory>
```

## Disclaimer
Use of this software for unlawful purposes is strictly prohibited under the license terms.    

## License
This software is licensed under the terms of the Eclipse Public License 2.0. It is provided 'as-is', without any express or implied warranty. In no event will the authors be held liable for any damages arising from the use of this software. Use of this software for illegal purposes is strictly prohibited. By using this software you agree to all terms.  

## Acknowledgements
This project was inspired by the "Playboy: Cover to Cover" software, a cherished piece of history for its users. A special thanks to the community that has kept the interest in this software alive. 

## Donations
This is a short script that took years to create. Lots of people tried to do this and gave up out of frustration, but I just never gave up. It was a labor of love and I've made it freely available to all. But if you want to show your support, donations are always appreciated.
```
BTC: bc1qlzy99t26sprju85pw249acuwajkyz32zh0jm2e

ETH: 0x952e06F462F457065890725E6597EDD036FC4889
```
