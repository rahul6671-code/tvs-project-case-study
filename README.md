# TVS Credit Dynamic Residual Pricing and Lending Engine

An end-to-end machine-learning prototype that forecasts vehicle liquidation
value, converts expected recovery shortfall into an explainable residual-risk
score, and recommends risk-adjusted LTV, pricing and tenure.

## Run locally

1. Put `Analytics Case Study Dataset.xlsx` in this folder.
2. Open `TVS_Residual_Engine.ipynb` in Jupyter.
3. Select **Kernel > Restart Kernel and Run All Cells**.
4. Confirm the model-comparison table and selected model.
5. Start the dashboard with `streamlit run app.py`.

The notebook exports agreement-level recommendations, model metrics, risk-band
strategy, metadata and the trained pipeline. See `GITHUB_UPLOAD_STEPS.md` for
deployment instructions.

## Important limitation

The recommendation rules are prototype policy guardrails, not an approved TVS
Credit lending policy. Validate them through a controlled champion-challenger
pilot before production use. Never publish confidential customer-level data.
