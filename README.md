# 📊 Data Analyzer Pro

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)

A lightweight, modern, browser-based application for statistical analysis and data visualization. 

This tool allows users to upload raw CSV datasets, designate response and explanatory variables, and instantly generate interactive scatterplots alongside simple or multiple linear regression calculations. Everything runs entirely client-side in the browser—no backend server or database installation required.

## ✨ Key Features

* **Drag-and-Drop CSV Uploads:** Instantly parse and read tabular data using a modern, interactive dropzone. 
* **Dynamic Variable Selection:** Automatically detects numeric columns and allows users to designate one Response Variable (Y) and one or multiple Explanatory Variables (X).
* **Statistical Engine:** Computes both simple linear regression and multiple linear regression, outputting the exact mathematical equation, the Coefficient of Determination ($R^2$), and the sample size ($n$).
* **Interactive Visualization:** Generates a responsive scatterplot mapping the actual data. If a single explanatory variable is selected, a trendline (regression line) is automatically drawn.
* **Analysis Notebook:** A built-in, multi-page rich text editor allows users to jot down insights, anomalies, and observations. Notes are automatically tied to the uploaded filename and saved to the browser's Local Storage for future visits.
* **Export Capabilities:** Instantly download generated charts as high-quality PNGs for reports or presentations.
* **Theme Support:** Features a toggleable Dark Mode/Light Mode that automatically updates UI elements and chart palettes.

## 🛠️ Built With

This application relies on vanilla HTML, CSS, and JavaScript, supercharged by three lightweight, open-source libraries via CDN:

* [PapaParse](https://www.papaparse.com/) - Fast and reliable CSV parsing.
* [Math.js](https://mathjs.org/) - Handles the matrix mathematics required to resolve multiple linear regression equations.
* [Chart.js](https://www.chartjs.org/) - Renders the responsive, interactive canvas scatterplots.

## 🚀 Getting Started

Because this application relies entirely on client-side rendering, setup is instantaneous.

### Installation

1. Clone this repository or download the source code.
2. Ensure you have the `index.html` file on your local machine.

### Usage

1. Double-click `index.html` to open it in any modern web browser (Chrome, Firefox, Safari, Edge).
2. Click the dropzone to upload a `.csv` file. Ensure your file has a header row. 
    * *Note: Two sample datasets (`student_data.csv` and `real_estate_sample.csv`) are provided in the `/data` folder for testing.*
3. Select your Response Variable (what you want to predict).
4. Select your Explanatory Variables (your predictors).
5. Click **Generate Analysis**.

## 🧠 How the Math Works

For Simple Linear Regression (one X variable), the app calculates the standard slope and y-intercept. 

For Multiple Linear Regression (multiple X variables), the app constructs matrices and utilizes the Ordinary Least Squares (OLS) estimator formula:  
`B = (X^T * X)^-1 * X^T * Y`

*If you select highly collinear variables (variables that are perfect predictors of one another), the math will fail to resolve, and the app will gracefully catch the error and notify you via a toast notification.*

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
