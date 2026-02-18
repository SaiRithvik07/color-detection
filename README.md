🎨 Color Detection using OpenCV

A simple and interactive Color Detection Application built using Python, OpenCV, Pandas, and NumPy.
This project allows users to double-click on any part of an image to detect the color name along with its RGB values.

📌 Features

Detect color name on double-click

Displays RGB values

Matches closest color using minimum distance algorithm

Works with any input image

Handles light colors with automatic text color adjustment

🛠️ Technologies Used

Python 3

OpenCV

NumPy

Pandas

Argparse

📂 Project Structure
Color-Detection/
│
├── color_detection.py
├── colors.csv
├── sample_image.jpg
└── README.md

📄 colors.csv Format

The CSV file should contain color data in this format:

color,color_name,hex,R,G,B
0,Black,#000000,0,0,0
1,White,#FFFFFF,255,255,255
...

🚀 Installation
1️⃣ Clone the repository
git clone https://github.com/yourusername/color-detection.git
cd color-detection

2️⃣ Install dependencies
pip install opencv-python numpy pandas

▶️ How to Run
python color_detection.py -i sample_image.jpg


Replace sample_image.jpg with your image path.

🖱️ How It Works

The image is loaded using OpenCV.

When the user double-clicks on the image:

The RGB values of the clicked pixel are captured.

The program compares them with all colors in colors.csv.

It calculates the minimum distance:

d = |R-Ri| + |G-Gi| + |B-Bi|


The closest matching color name is displayed.

A colored rectangle appears showing:

Color Name

RGB Values

🧠 Algorithm Used

The program uses Manhattan Distance to find the closest color match:

distance = |R - Rcsv| + |G - Gcsv| + |B - Bcsv|


The color with the minimum distance is selected.

📸 Example Output

Double-click on image

A color bar appears at the top

Displays:

Sky Blue R=135 G=206 B=235

🎯 Future Improvements

Add HEX color display

Convert to HSV color detection

Add real-time webcam color detection

Deploy as a web application using Flask

