```markdown
# IT Support Ticket Classification

This repository contains a Machine Learning demonstration project developed as part of my industrial internship at **Beeline Kazakhstan (Kar-Tel LLP)** within the IT Technical Support and Data Engineering Department.

> ** NDA Disclaimer:** > As Beeline is a major telecommunications provider, strict Non-Disclosure Agreements (NDA) and corporate security policies prohibit the sharing of actual proprietary data, source code, or infrastructure details. 
> 
> *This repository is a "pet project" created in an isolated local environment using a synthetic dataset.* It serves to safely demonstrate the data engineering, NLP, and Machine Learning methodologies I applied in my actual daily workflow without compromising corporate security.

## Project Goal
With the rapid onboarding of new employees, the volume of internal IT support requests has grown significantly. Manual triage of these tickets is a bottleneck. 

The goal of this project is to automate the prioritization of incoming IT support tickets using **Natural Language Processing (NLP)**. The model reads the text description of an IT incident and automatically predicts its urgency level (`Critical`, `High`, `Medium`, `Low`), effectively reducing the Mean Time To Acknowledge (MTTA).

## Technology Stack
* **Language:** Python
* **Data Processing:** Pandas
* **Machine Learning:** Scikit-Learn (`TfidfVectorizer`, `RandomForestClassifier`)
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / VS Code

## Model Methodology
1. **Feature Engineering:** Raw text descriptions are converted into numerical matrices using Term Frequency-Inverse Document Frequency (`TF-IDF`), extracting the top 3,000 most relevant features while removing standard English stop words.
2. **Classification:** A Random Forest Classifier (`n_estimators=100`) is trained on the vectorized text. This ensemble algorithm was chosen for its high resistance to overfitting on sparse, high-dimensional text data.
3. **Evaluation:** The model is evaluated using a Confusion Matrix to ensure it accurately distinguishes critical infrastructure failures from routine software requests.

## Repository Structure
* `classification_model.ipynb` — The main Jupyter Notebook containing data preprocessing, model training, and visualizations.
* `tickets_clean.csv` — The synthetic dataset containing ~10,000 mocked ITSM logs used for training.
* `README.md` — Project documentation.

## How to Run locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/alesha-ofc-he/DemoRracriceKarTelAlikhanKassymbekov])
   ```
2. Install the required dependencies:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
   ```
3. Open `classification_model.ipynb` in VS Code or Jupyter Notebook and click **Run All**.

---
*Developed by Alikhan Kassymbekov | Astana IT University | 2026*
```
