# Growth Charts Calculator

[![GitHub top language](https://img.shields.io/github/languages/top/faliwar/growthcharts?style=flat-square&color=blue)](https://github.com/faliwar/growthcharts)
[![GitHub license](https://img.shields.io/github/license/faliwar/growthcharts?style=flat-square)](LICENSE)
[![GitHub repo size](https://img.shields.io/github/repo-size/faliwar/growthcharts?style=flat-square)](https://github.com/faliwar/growthcharts)
[![GitHub stars](https://img.shields.io/github/stars/faliwar/growthcharts?style=flat-square)](https://github.com/faliwar/growthcharts/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/faliwar/growthcharts?style=flat-square)](https://github.com/faliwar/growthcharts/network/members)
[![GitHub issues](https://img.shields.io/github/issues/faliwar/growthcharts?style=flat-square)](https://github.com/faliwar/growthcharts/issues)

An anthropological growth calculator optimized for Electronic Health Records (EHR) / medical records. This application calculates percentiles and Z-scores for child and adolescent development based on international standards (WHO/OMS, CDC, and Nellhaus).

The tool runs completely on the client side (in the browser) and is fully functional offline.

👉 **[Live Demo](https://fabianoposwar.com/percentis/)** (in Brazilian Portuguese)

---

## Key Features

- **Anthropometric Metrics**: Calculates percentiles and Z-scores for Weight ($P$), Height/Length ($E$), Head Circumference ($PC$), and BMI ($IMC$).
- **Growth Standards**: Supports WHO (OMS), CDC, and Nellhaus tables.
- **EHR Integration**: Optimized for copying results directly into patient clinical charts/notes.
- **Dynamic Themes**: Automatically changes the interface color scheme based on the selected sex (blue for male, pink for female).
- **Responsive Design**: Mobile-friendly interface that works on smartphones, tablets, and desktop computers.
- **No Installation Required**: Run locally with a single click.

---

## How to Install and Run Locally (No Node.js or Setup Required)

This project consists of pure, static files (HTML, CSS, and JavaScript) and a JSON database. You do **not** need Node.js, npm, or any development tools to use it.

### Option 1: Run Directly (Offline Mode)

1. **Download the files**:
   - Go to the top of this repository on GitHub.
   - Click the green **Code** button and select **Download ZIP**.
   - Extract the downloaded ZIP file to any folder on your computer.
2. **Open the Calculator**:
   - Double-click the `index.html` file to open it in your web browser.
3. **CORS Local Fallback**:
   - Modern web browsers block websites from fetching local files (`dados_percentis.json`) when opened directly from your hard drive (via the `file://` protocol) due to security restrictions.
   - When you open the page, a yellow/orange banner will appear warning you about this.
   - Simply click **Choose File** (or "Selecionar arquivo") in that banner and select the `dados_percentis.json` file from the same folder.
   - Once selected, the database will load instantly, and the application is ready to run offline.

### Option 2: Run Using a Simple Local Web Server (Recommended to Avoid CORS Prompts)

If you prefer to load the database automatically without having to select the JSON file every time, you can host the files using a simple static web server.

#### Using Python (If installed)
1. Open your Terminal (macOS/Linux) or Command Prompt/PowerShell (Windows) in the folder where you extracted the files.
2. Run the following command:
   ```bash
   python -m http.server 8000
   ```
3. Open your browser and go to `http://localhost:8000`. The calculator will load and function without any local file warnings.

#### Using PHP (If installed)
1. Run the following command in the folder:
   ```bash
   php -S localhost:8000
   ```
2. Open your browser and go to `http://localhost:8000`.

---

## How to Use

1. **Select the Patient's Sex**: Choose Male (Masculino) or Female (Feminino). The theme will update automatically.
2. **Input Dates**:
   - **Data das Medidas** (Measurement Date): Defaulted to today's date in `DD/MM/YYYY` format.
   - **Data de Nascimento** (Date of Birth): Paste or write the patient's birth date.
3. **Input Anthropometric Data**: Enter the measurements in the text box. The format is flexible, for example:
   ```text
   P: 32 kg
   E: 135 cm
   PC: 52 cm
   ```
4. **Calculate**: Click the **Processar Dados** button.
5. **Copy Results**: The calculated percentiles and Z-scores will appear in the output area. Click **Copiar Resultado** to copy the formatted text to your clipboard, ready to be pasted into your clinical notes.

---

## Project Structure

- `index.html`: The main web application containing the layout, styling, and calculation logic.
- `dados_percentis.json`: The database file containing the growth standards data (WHO/OMS, CDC, and Nellhaus).

---

## License

This project is licensed under the [MIT License](LICENSE).
