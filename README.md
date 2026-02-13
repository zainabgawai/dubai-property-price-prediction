# dubai-property-price-prediction
Predicting Dubai Property Prices Using Large Scale Real Estate Data
Team Memebers
- Noura (8877725) - Leader
- Zainab Gawai Zuhair (8540238) - Scribe
- Saadiyah Asif (8416655)
- Sadhguna Kumar (8448899)
- Nahan Salam (8226337)
- Frenica (8488885)
- Laila (8347050)
- Ziya (8417337)
- Rahma (8540184)
- Guzail Rafi (7926972)

Dataset
- Source: Dubai Pulse 
- Size: 1,647,607 records, 46 features
- Link: https://www.dubaipulse.gov.ae/data/dld-transactions/dld_transactions-open

Prerequisites
- Docker Desktop installed
- At least 16GB RAM available

SetUp Instructions (From Local Machine)
1. Increase the WSL2 VM Resource Limits
   ```text
   - Add/ Edit the .wslconfig file: C:\Users\<your-username>\.wslconfig
   - [wsl2]
     memory=14GB
     processors=6
     swap=4GB
   ```

3. Build the Docker image:
   docker build -t csci316-project1 .

4. Run the container:
   docker run -p 8888:8888 -it csci316-project1

5. Access Jupyter at http://localhost:8888
   (Token will be displayed in terminal)

SetUp Instructions (From Github Repo) - The Docker Image can be found under the Packages Section
1. Run on Terminal: docker pull ghcr.io/zainabgawai/dubai-property-price-prediction:latest
2. Then Run: docker run -p 8888:8888 ghcr.io/zainabgawai/dubai-property-price-prediction:latest
3. On yor browser, go to: http://localhost:8888 (Token will be displayed in terminal)

Project Structure
```text
CSCI316_PROJECT1/
├── Dockerfile
├── requirements.txt
├── README.md
├── data/
│   ├── clean/
│   ├── raw/
│   └── parquet_folder/
├── notebooks/
│   ├── 01_datacleaning.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_baseline_models.ipynb
│   ├── 04_bagging_boosting.ipynb
│   ├── 05_manual_10_fold_cross_validation.ipynb
│   └── 06_visualization.ipynb
├── models/
│   ├── baseline_gbt/
│   ├── baseline_rf/
│   └── baseline_lr/
└── results/
    ├── baseline_results/
    └── ensemble_results/
    └── cross_validation/
```

