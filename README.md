# 📱 Mobile Game Analytics & A/B Testing

This project explores user behavior and monetization in a mobile game dataset through two key components:

1. **Player Retention Analysis** — understanding how player engagement with the game evolve over time.
2. **A/B Testing** — evaluating the impact of a new penalty-based feature on monetization metrics like revenue and in-app purchases.

---

## 🔍 Project Structure

### 📊 1. `Mobile Game Analytics.ipynb`

This notebook performs **exploratory analysis and retention analysis** based on user registration and login activity. Key steps include:

- Parsing and transforming registration and activity timestamps
- Performing cohort-based retention analysis (daily, weekly, monthly)
- Calculating user engagement metrics such as percentage of active years

📌 **Key Insight:**  
Player retention decays quickly over time. Most users do not return after their first few sessions, emphasizing the need for better onboarding and re-engagement strategies.

---

### 🧪 2. `AB Test.ipynb`

This notebook performs statistical testing to evaluate the impact of introducing a **penalty mechanic during a limited-time event**. The hypothesis is that with exclusive rewards and greater difficulty, players will be more incentivized to spend.

#### Tests Performed:
- **T-Test on Revenue** (One-tailed two-sample t-test)
- **Z-Test on In-App Purchase Rate** (One-tailed z-test for proportions)

#### Results:
| Metric            | Test Used           | p-value | Conclusion                                      |
|-------------------|---------------------|---------|-------------------------------------------------|
| Revenue           | One-tailed two-sample t-test | 0.63    | ❌ Not statistically significant                |
| In-App Purchase % | Z-test for proportions | 0.79 | ❌ Not statistically significant                |

📌 **Key Insight:**  
The new feature did **not significantly increase monetization**. Both average revenue and purchase rates remained statistically similar between control and treatment groups. Further experimentation may be needed with alternate reward structures or segmentation.

---

## 📁 Files Included

- `Mobile Game Analytics.ipynb` – Player retention analysis
- `AB Test.ipynb` – A/B testing to evaluate monetization impact

---

## 📌 Possible Future Work

- Explore segmentation (e.g., new vs. returning users, geographic breakdown)
- Run additional A/B tests with adjusted reward structures
- Include session-level engagement metrics and funnel analysis

---
