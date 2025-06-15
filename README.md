# Custom Threadmilling Calculator

A powerful, mobile-friendly web application designed to calculate precise X-Axis end values for CNC threadmilling operations. This tool was built to streamline workshop calculations, replacing manual spreadsheet lookups with a fast, interactive, and purely math-driven interface.

The app is built as a single, self-contained HTML file, making it incredibly portable and easy to use on any device with a web browser, both online and offline.

---

## ✨ Key Features

* **Dual Calculation Modes:** Separate, optimized calculators for both **Metric** and **Imperial** threads.
* **Streamlined Math Engine:** Automatically calculates the correct drill size based on standard formulas (`Major Dia - Pitch`), reducing manual input and potential errors.
* **Incremental Cut Outputs:** Enter a percentage increment to see a full list of X-Axis end values for multiple passes (e.g., 25%, 50%, 75%, 100%).
* **Fine-Tune Control:** A dedicated input allows for calculating precise values for custom percentages (e.g., 105% for a finishing pass).
* **Adjustable Precision:** Easily adjust the number of decimal places for the final output using simple `+` and `-` controls.
* **Smart Imperial Conversion:** The Imperial calculator automatically converts decimal inch inputs to the nearest common fraction (e.g., `0.4375` displays as `7/16"`) and calculates the metric pitch from TPI.
* **Persistent State:** The app automatically saves your last used values to your browser's local storage, so your data is waiting for you the next time you open it.
* **Mobile-First Design:** A clean, responsive interface that is optimized for use on mobile phones in a workshop environment.

---

## 🔧 How It Works: The Core Calculation

The primary purpose of this app is to determine the **X-Axis End Value**. This is the radial distance from the center of the pre-drilled hole to the center of the threadmill cutter required to produce the correct thread diameter.

The calculation is based on the following formula:

// 1. Find the radius of the material to be removedDifference (Radius) = (Major Thread Diameter - Drill Size) / 2// 2. Find the distance from the cutter edge to the hole edgeTM to Hole Edge = (Drill Size / 2) - (Thread Mill Diameter / 2)// 3. Combine these values with the desired cut percentageX-Axis End Value = TM to Hole Edge + (Difference (Radius) * Percentage of Cut)
For the **Metric** calculator, the `Drill Size` is automatically calculated as `Major Thread Diameter - Pitch`.

---

## 🚀 How to Use & Deploy

This calculator is a single `index.html` file.

### Local Use
1.  Download the `index.html` file from this repository.
2.  Open it with any modern web browser (Chrome, Firefox, Safari).

### Online Deployment (Recommended)
You can host this app for free using either **Netlify** or **GitHub Pages**.

**To Deploy on GitHub Pages:**
1.  Ensure the HTML file in this repository is named `index.html`.
2.  Go to the **Settings** tab of this repository.
3.  Navigate to the **Pages** section on the left menu.
4.  Under "Build and deployment", select the source as **`main`** branch and the folder as **`/ (root)`**.
5.  Save your changes. Your site will be live at `https://your-username.github.io/your-repository-name/`.

---

### How to Add the Screenshot to Your README

1.  Take a screenshot of the app running on your computer or phone.
2.  In your GitHub repository, go to the **"Issues"** tab and click **"New Issue"**.
3.  Drag and drop your screenshot into the text box of the issue. GitHub will upload it and generate a Markdown URL that looks like `![image](https://user-images.githubusercontent.com/...)`.
4.  **Copy the entire Markdown line** (`![image](...)`).
5.  You can now close the new issue without saving it.
6.  Edit this `README.md` file and paste the copied Markdown line at the top to replace the placeholder.
