# Upload the TVS Residual Engine to GitHub

## 1. Generate the output files locally

Place `Analytics Case Study Dataset.xlsx` in this folder. Open
`TVS_Residual_Engine.ipynb` in Jupyter and select **Kernel > Restart Kernel and
Run All Cells**.

Wait until the notebook displays `Exports created successfully`.

It will generate:

- `TVS_Residual_Lending_Recommendations.csv`
- `TVS_Model_Performance.csv`
- `TVS_Strategy_By_Risk.csv`
- `TVS_Residual_Model.joblib`
- `TVS_Model_Metadata.json`

## 2. Protect confidential data

Do not upload the original Excel dataset to a public repository. Before
uploading the agreement-level CSV, remove or mask `Agmt Id` if the identifiers
are real. The included `.gitignore` excludes the original Excel file and model
binary by default.

## 3. Create the repository

1. Sign in to GitHub and click **New repository**.
2. Name it `tvs-residual-lending-engine`.
3. Choose **Public** only if all uploaded data is anonymized.
4. Create the repository without adding another README.

## 4. Upload the extracted files

Use **Add file > Upload files** and upload the project files themselves. Do not
upload only the ZIP archive. Include the three generated CSV files so the live
dashboard has data to display.

The repository should contain:

```text
app.py
requirements.txt
README.md
TVS_Residual_Engine.ipynb
TVS_Residual_Lending_Recommendations.csv
TVS_Model_Performance.csv
TVS_Strategy_By_Risk.csv
```

Commit the changes.

## 5. Deploy on Streamlit Community Cloud

1. Open https://share.streamlit.io.
2. Click **Create app**.
3. Select the GitHub repository.
4. Set the main file path to `app.py`.
5. Click **Deploy**.

If the app shows `Run all cells first`, confirm that
`TVS_Residual_Lending_Recommendations.csv` is present in the repository root,
then reboot the app from **Manage app**.

