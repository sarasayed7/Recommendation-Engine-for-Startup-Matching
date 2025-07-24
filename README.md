# Recommendation-Engine-for-Startup-Matching

# 🚀 Recommendation Engine for Startup–Service Provider Matching

## 📌 Project Overview

This project is part of an AI internship task to design a logic-based recommendation engine that matches startup founders with relevant service providers or mentors. The goal is to automate and optimize the pairing process based on domain, skills, project needs, and availability.

---

## 🧠 Problem Statement

Given a dataset containing 50 founders and 50 service providers, the system calculates a match score between every possible pair and ranks the top matches for each founder and provider.

---

## 📁 Dataset

- **File:** `User_Matching_Dataset.csv`
- **Users:** Founders (IDs starting with F) and Service Providers (IDs starting with S)
- **Attributes include:**
  - `startup_industry`, `tech_requirement`, `project_need`, `project_deadline`
  - `industry_preference`, `core_skill`, `preferred_project_type`, `availability`

---

## ⚙️ Matching Logic

Each match is scored out of 100 based on:

| Criteria              | Match Logic                                  | Weight |
|-----------------------|----------------------------------------------|--------|
| Industry Match        | Founder’s industry == Provider’s preference  | 25     |
| Skill Match           | Tech requirement == Core skill               | 25     |
| Project Type Match    | Project need == Preferred project type       | 25     |
| Timeline Match        | Deadline == Availability                     | 25     |

A binary value (`1` or `0`) is used to represent each match criterion.

---

## 📊 Output

- **Match Score Table**: Each founder–provider pair with match score and explanations
- **Recommendation Explanation Table**: Includes `industry_match`, `skill_match`, `project_type_match`, and `timeline_match` for transparency
- **Top 5 Matches**: Generated for each founder based on highest scores
- **Visualizations**:
  - Bar chart: Top matches per founder
  - Heatmap: Match score matrix (optional)

---

## 🛠️ Tech Stack

- Python (Pandas, NumPy)
- Matplotlib / Seaborn for visualization
- Jupyter Notebook / Google Colab

---

## 📈 Sample Output

- Top Matches
| founder_id | provider_id | match_score | industry_match | skill_match | project_type_match | timeline_match |
|------------|-------------|-------------|----------------|-------------|--------------------|----------------|
| F044       | S018        | 100         | 1              | 1           | 1                  | 1              |
| F022       | S011        | 100         | 1              | 1           | 1                  | 1              |

| founder_id | provider_id | match_score | industry_match | skill_match | project_type_match | timeline_match |
|------------|-------------|-------------|----------------|-------------|--------------------|----------------|
| F1         | S3          | 90          | 1              | 1           | 1                  | 1              |
| F2         | S7          | 65          | 1              | 0           | 1                  | 1              |




