# AI-Paper-Checker-App

## Overview
AI-Paper-Checker-App is an automated Optical Mark Recognition (OMR) system built using Python and OpenCV. It scans and grades multiple-choice answer sheets (bubble sheets) with high accuracy, making exam evaluation faster and more efficient.

## Features
- **Automated OMR**: Detects and evaluates bubble sheets using OpenCV.
- **Fast and Accurate Grading**: Compares answers with an answer key to calculate scores.
- **Support for Multiple Formats**: Works with various answer sheet templates.
- **Easy-to-Use Interface**: Simple and intuitive UI/CLI for scanning and checking papers.
- **Report Generation**: Generates detailed reports with students' scores.
- **Error Handling & Correction**: Detects multiple markings and incorrect responses.

## Technologies Used
- **Python** (Primary programming language)
- **OpenCV** (Image processing for OMR)
- **NumPy** (Data manipulation)
- **Matplotlib** (Visualization of results).
- **FastAPI** (Web-based interface and API support)
- **FullStack Developement** (Complete Webiste)
- **MOngo DB** (Store Data)
  

## Folder Structure
*(This is a suggested folder structure. You may follow your own based on your development needs.)*
```
AI-Paper-Checker-App/
│── data/                     # Sample answer sheets, test images, and datasets
│── models/                   # Pre-trained models for advanced AI-based grading
│── src/                      # Source code
│   │── core/                 # Core OMR processing logic
│   │   │── image_processing.py  # Image pre-processing and feature extraction
│   │   │── omr_engine.py     # Main OMR detection and evaluation
│   │── api/                  # FastAPI-based backend for web services
│   │   │── main.py           # FastAPI entry point
│   │   │── routes.py         # API endpoints
│   │── ui/                   # User interface components (CLI & Web)
│   │── utils/                # Helper functions (e.g., file handling, logging)
│   │── config.py             # Configuration settings
│── tests/                    # Unit and integration tests
│── docs/                     # Documentation, API references, and guides
│── requirements.txt          # Dependencies list
│── README.md                 # Project overview and setup instructions
│── main.py                   # Entry point for CLI execution
│── web_app.py                # Web-based interface (FastAPI)
```

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/AI-Paper-Checker-App.git
   cd AI-Paper-Checker-App
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the FastAPI application:
   ```sh
   uvicorn src.api.main:app --reload
   ```

## Usage
1. **Capture/Scan Answer Sheet**: Upload or scan an image of the bubble sheet.
2. **Process Image**: The system preprocesses and identifies marked answers.
3. **Evaluate Score**: Matches marked answers against the answer key.
4. **Generate Report**: Displays scores and exports results as needed.

## Configuration
- Modify `config.py` to set answer key, sheet layout, and grading rules.
- Adjust preprocessing settings in `image_processing.py` for different answer sheet formats.

## API Endpoints (FastAPI)
- `POST /upload` - Upload an answer sheet for processing
- `GET /results/{student_id}` - Fetch results for a specific student
- `GET /health` - Check API health status

## Example
```sh
uvicorn src.api.main:app --reload
```

## Roadmap
- [ ] Implement a full-fledged web-based UI
- [ ] Add AI-powered handwriting recognition
- [ ] Support for subjective answers
- [ ] Integration with Learning Management Systems (LMS)
- [ ] Mobile App for Answer Sheet Scanning

## Contributions
Contributions are welcome! Feel free to fork the repository and submit pull requests.

## License
MIT License. See `LICENSE` for more details.

## References
- [Bubble Sheet Scanner and Test Grader using OpenCV](https://pyimagesearch.com/2016/10/03/bubble-sheet-multiple-choice-scanner-and-test-grader-using-omr-python-and-opencv/)
