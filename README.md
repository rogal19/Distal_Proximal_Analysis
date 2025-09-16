# Proximal vs. Distal Isometric Force Analysis

This repository contains the Python code used in the master's thesis:

**"How does the use of proximal and distal effectors affect timing precision and stability in coordination during rhythmic isometric contractions with increasing movement frequency?"**

The code performs data processing, peak detection, and synchronization analysis for isometric force experiments with increasing metronome frequency.  

---

## 🔹 Features
- Import and process force data from Excel files
- Signal smoothing with Savitzky–Golay filter
- Detection of R-points using `scipy.signal.find_peaks`
- Dynamic thresholding to avoid false peaks
- Separation of pre- and post-interval force responses
- Generation of metronome sequences (60–240 BPM, +10 BPM every 8 seconds)
- Synchronization and timing error analysis
- Export of interactive Plotly HTML graphs
- Export of detailed Excel result tables

---

## 🔹 Requirements
The analysis runs in **Python 3.8+**.  
Install dependencies with:


pip install -r requirements.txt
Typical libraries used:

numpy

pandas

scipyd

plotly

openpyxl

##🔹 Usage
Mount or specify your data folder containing .xlsx files.
Example (Google Colab):

python
from google.colab import drive
drive.mount('/content/drive')
Update the test_path variable in the script to point to your folder:

python
test_path = '***'
Run the main script:

python
Kopier kode
analyze_all_files()
Results:

Interactive HTML graphs are saved in grafer_html1/

Processed Excel result files are exported for further analysis

🔹 Example Output
Force curves with detected R-points (right hand in red, left hand in cyan)

Metronome markers aligned with force response

Excel summary including timing errors, synchronization analysis, and BPM at first synchronization

🔹 Reproducibility
The full dataset and code can be archived on Zenodo with a DOI for citation.
To reproduce analyses:

Place your raw Excel data in the specified folder

Run the provided notebook or script in Google Colab / local Python environment

🔹 Citation
If you use this code in your research, please cite:

Rogalski, P. C. (2025). How does the use of proximal and distal effectors affect timing precision and stability in coordination during rhythmic isometric contractions with increasing movement frequency? Master’s Thesis.
