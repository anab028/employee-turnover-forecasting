# employee-turnover-forecasting

# Employee Attrition Prediction for Salifort Motors

## Overview  
This project uses machine learning to predict which employees are most likely to leave Salifort Motors. We trained and compared several models on ~12,000 HR survey records and selected XGBoost as our best performer. This lets HR flag at-risk employees early and design targeted retention interventions.

---

## Business Problem  
Salifort Motors invests heavily in recruiting and training. Employee turnover—whether voluntary or involuntary—carries significant costs in lost productivity, recruitment, and ramp-up time. HR wants a data-driven way to identify staff at high risk of leaving so they can proactively address the root causes and improve retention.

---

## Data  
- **Source:** Internal HR survey (`HR_capstone_dataset.csv`), 11,991 rows, 10 columns  
- **Features:**  
  - `satisfaction_level` (0 – 1)  
  - `last_evaluation` (0 – 1)  
  - `num_projects`  
  - `average_monthly_hours`  
  - `years_at_company`  
  - `work_accident` (0/1)  
  - `promotion_last_5_years` (0/1)  
  - `department` (10 categories)  
  - `salary` (low, medium, high)  
- **Target:** `left` (0 = stayed, 1 = left)  
- **Limitations:** Self-reported data; no demographic or geographic fields.



## Key Findings  
1. **Low Satisfaction** is the strongest predictor of turnover.  
2. **Low Salary Band** employees churn at much higher rates.  
3. **High Workload** (> 200 hrs/month or 5–6 projects) increases risk.  
4. **Lack of Recent Promotion** correlates with higher exit probability.  
5. **Mid-Tenure Employees** (2–5 years) are most likely to leave.

---

## Recommendations  
1. **Monthly Risk Scoring**  
   - Integrate the XGBoost model into the HR dashboard to compute a “leave-risk” score (0 – 1) for every employee each month.  
2. **Targeted Check-Ins**  
   - Focus on the top 10–15% highest-risk employees for quick one-on-one meetings or pulse surveys.  
3. **Workload Management**  
   - Cap the number of active projects at four per employee and monitor overtime closely.  
4. **Compensation Reviews**  
   - Fast-track salary equity assessments and adjustments for at-risk employees in the low-pay band.  
5. **Career Development**  
   - Launch a formal mentorship program and clear promotion pathways, especially for staff in years 2–5.

---

## Next Steps  
- **Threshold Tuning:** Experiment with different probability cutoffs to balance recall and precision.  
- **Quarterly Retraining:** Update the model with new turnover data every quarter to maintain performance.  
- **Fairness Audits:** Regularly check for any bias (by department, pay band, etc.) and recalibrate as needed.  
- **Extended Analysis:** Explore predicting “time-to-exit” or team-level churn to deepen insights.

---

## Repository Contents  
