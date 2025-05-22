# FTEC4999 Group G: Portfolio Advising with ILLIQ Factor

This repository contains the Final Year Project for FTEC4999 Financial Technology, developed by Group G. The project includes two Jupyter Notebooks for computing the ILLIQ factor and advising portfolio allocations, a web application (`UI_UX_App`), a project report, and a user manual.

## Project Structure

```
FTEC4999_GroupG_Project/
├── notebooks/
│   ├── Portfolio Formation.ipynb        # Computes ILLIQ factor
│   ├── Portfolio_Advising_App.ipynb     # Portfolio analysis and suggestions
│   ├── data/
│   │   ├── sample_daily_stock_price.csv # Sample raw data
│   │   ├── F-F_Research_Data_5_Factors_2x3_daily.CSV
│   │   ├── F-F_Momentum_Factor_daily.CSV
│   │   ├── illiq_factor_vw.csv         # Processed data
│   │   ├── illiq_factor_ew.csv         # Processed data
│   │   ├── fama_french_data.csv        # Processed data
│   ├── requirements.txt
├── UI_UX_App/
│   ├── backend/                        # FastAPI backend
│   ├── frontend/                       # JavaScript frontend
├── docs/
│   ├── Final_Report_G.docx             # Project report
│   ├── USER_MANUAL.md                  # Setup instructions
├── README.md
├── .gitignore
```

## Setup and Execution

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/FTEC4999-GroupG-Project.git
   cd FTEC4999-GroupG-Project
   ```

2. **Notebooks**:
   - Install Python 3.7.
   - Create a virtual environment:
     ```bash
     python -m venv venv
     source venv/bin/activate  # Linux/macOS
     venv\Scripts\activate     # Windows
     ```
   - Install dependencies:
     ```bash
     pip install -r notebooks/requirements.txt
     ```
   - Run notebooks:
     ```bash
     cd notebooks
     jupyter notebook
     ```
   - Run `Portfolio Formation.ipynb` first, then `Portfolio_Advising_App.ipynb`.
   - **Note**: Processed data (`illiq_factor_vw.csv`, etc.) is included for quick testing. For full raw data processing, download raw data from [OneDrive Link] and place in `notebooks/data/`.

3. **UI_UX_App**:
   - **Backend**:
     ```bash
     cd UI_UX_App/backend
     python -m venv venv
     source venv/bin/activate  # Linux/macOS
     venv\Scripts\activate     # Windows
     pip install -r requirements.txt
     uvicorn src.main:app --host 0.0.0.0 --port 8000
     ```
   - **Frontend**:
     ```bash
     cd UI_UX_App/frontend
     npm install
     npm run dev
     ```
   - **Deployed App**:
     - Backend: [Render URL]
     - Frontend: [Vercel URL]

4. **Documentation**:
   - `docs/Final_Report_G.docx`: Project methodology and results.
   - `docs/USER_MANUAL.md`: Detailed setup instructions.

## Data Notes
- **Processed Data**: Files like `illiq_factor_vw.csv` and `fama_french_data.csv` allow quick testing with `Portfolio_Advising_App.ipynb`’s functional code section.

## License
See `UI_UX_App/LICENSE` for details.
