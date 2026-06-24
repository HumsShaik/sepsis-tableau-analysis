# Sepsis Dataset Clinical Data Dictionary

## Story 1: Understanding Sepsis – Clinical Overview

This document explains the major variables used in the sepsis dataset and their clinical importance.

---

# 1. ICU Time Variables

## Hour

**Definition:**
Represents the number of hours since ICU monitoring started.

**Clinical Importance:**
Sepsis can worsen quickly. Hourly monitoring helps identify rapid deterioration.

**Example Use in Tableau:**
Analyze how sepsis develops over ICU time.

---

## Unit1

**Definition:**
Represents one ICU unit classification.

**Clinical Importance:**
Different ICU units may manage different patient types, affecting sepsis patterns.

**Example Use in Tableau:**
Compare sepsis prevalence across Unit1.

---

## Unit2

**Definition:**
Represents another ICU unit classification.

**Clinical Importance:**
Helps understand ICU specialization and patient distribution.

**Example Use in Tableau:**
Compare Unit1 vs Unit2 outcomes.

---

## ICULOS (ICU Length of Stay)

**Definition:**
Total number of hours a patient has stayed in ICU.

**Clinical Importance:**
Longer ICU stays often indicate more severe illness or complications.

**Example Use in Tableau:**
Compare average ICU stay between sepsis and non-sepsis patients.

---

## HospAdmTime

**Definition:**
Time from hospital admission to ICU admission.

**Clinical Importance:**
A longer delay before ICU admission may worsen sepsis outcomes.

**Example Use in Tableau:**
Study whether delayed ICU admission increases sepsis severity.

---

# Tableau Insights to Build

### Worksheet 1: Sepsis Progression Over Time

* X-axis: Hour
* Y-axis: Average SepsisLabel
* Goal: Identify when sepsis is more likely to develop.

### Worksheet 2: ICU Stay vs Sepsis

* X-axis: ICULOS
* Y-axis: SepsisLabel
* Goal: See if longer ICU stays correlate with sepsis.

### Worksheet 3: ICU Unit Distribution

* Dimension: Unit1 / Unit2
* Measure: Count of Patients
* Goal: Compare sepsis across ICU units.

# 2. Blood Cell Markers

## Hct (Hematocrit)

**Definition:**
Percentage of red blood cells in blood.

**Clinical Importance:**
Low Hct may indicate anemia, bleeding, or fluid imbalance. In sepsis, abnormal Hct can signal worsening circulation.

**Normal Range:**

* Male: 41–50%
* Female: 36–44%

**Example Use in Tableau:**
Compare Hct levels between sepsis and non-sepsis patients.

---

## Platelets

**Definition:**
Blood cells responsible for clotting.

**Clinical Importance:**
Low platelets (thrombocytopenia) are common in severe sepsis and may indicate organ dysfunction.

**Normal Range:**
150,000–450,000 per microliter

**Example Use in Tableau:**
Analyze platelet drop across sepsis stages.

---

## WBC (White Blood Cell Count)

**Definition:**
Measures immune system activity.

**Clinical Importance:**
High WBC often indicates infection. Very low WBC can indicate severe immune failure.

**Normal Range:**
4,000–11,000 per microliter

**Example Use in Tableau:**
Track infection intensity and sepsis progression.

---

# Tableau Insights to Build

### Worksheet 4: WBC Distribution

* X-axis: WBC
* Color: SepsisLabel
* Goal: Compare infection burden.

### Worksheet 5: Platelets vs Sepsis

* X-axis: Platelets
* Y-axis: SepsisLabel
* Goal: Identify clotting abnormalities.

### Worksheet 6: Hct Trends

* X-axis: Hour
* Y-axis: Hct
* Goal: Observe blood concentration changes over time.
# 3. Electrolytes and Coagulation Markers

## Magnesium

**Definition:**
An essential mineral involved in muscle, nerve, and heart function.

**Clinical Importance:**
Abnormal magnesium can cause arrhythmias, muscle weakness, and worsen sepsis-related organ dysfunction.

**Normal Range:**
1.7–2.2 mg/dL

**Example Use in Tableau:**
Track magnesium imbalance in septic patients.

---

## Fibrinogen

**Definition:**
A blood clotting protein produced by the liver.

**Clinical Importance:**
In sepsis, fibrinogen may initially rise due to inflammation and later fall in severe coagulation disorders like DIC (Disseminated Intravascular Coagulation).

**Normal Range:**
200–400 mg/dL

**Example Use in Tableau:**
Analyze clotting abnormalities in advanced sepsis.

---

## Potassium

**Definition:**
A key electrolyte for heart and muscle function.

**Clinical Importance:**
Abnormal potassium can lead to dangerous cardiac rhythm problems. Sepsis can disrupt potassium due to kidney dysfunction.

**Normal Range:**
3.5–5.0 mEq/L

**Example Use in Tableau:**
Identify potassium imbalance in severe cases.

---

# Tableau Insights to Build

### Worksheet 7: Potassium Distribution

* X-axis: Potassium
* Color: SepsisLabel
* Goal: Detect electrolyte disturbances.

### Worksheet 8: Magnesium vs Sepsis

* X-axis: Magnesium
* Y-axis: SepsisLabel
* Goal: Compare mineral imbalance.

### Worksheet 9: Fibrinogen Levels

* X-axis: Fibrinogen
* Color: SepsisLabel
* Goal: Explore clotting dysfunction.
# 4. Acid-Base Balance Markers

## Base Excess

**Definition:**
Measures excess or deficit of bicarbonate in the blood.

**Clinical Importance:**
Negative base excess often indicates metabolic acidosis, which is common in sepsis due to poor oxygen delivery and lactate buildup.

**Normal Range:**
-2 to +2 mmol/L

**Sepsis Interpretation:**

* Very negative = severe acidosis
* Indicates tissue hypoperfusion

**Example Use in Tableau:**
Track worsening metabolic imbalance in septic patients.

---

## pH

**Definition:**
Measures blood acidity or alkalinity.

**Clinical Importance:**
Low pH (acidic blood) is common in severe sepsis and septic shock.

**Normal Range:**
7.35–7.45

**Sepsis Interpretation:**

* <7.35 = acidosis
* Lower pH often means worse prognosis

**Example Use in Tableau:**
Compare pH changes in septic vs non-septic patients.

---

# Tableau Insights to Build

### Worksheet 10: pH Distribution by Sepsis

* X-axis: pH
* Color: SepsisLabel
* Goal: Identify acidotic patients.

### Worksheet 11: Base Excess Trends

* X-axis: Hour
* Y-axis: Base Excess
* Goal: Observe worsening metabolic acidosis over time.

### Worksheet 12: Base Excess vs pH

* X-axis: Base Excess
* Y-axis: pH
* Color: SepsisLabel
* Goal: Understand acid-base relationship.

# 5. Tissue Hypoxia and Organ Stress Markers

## Lactate

**Definition:**
Measures lactic acid produced when tissues do not receive enough oxygen.

**Clinical Importance:**
One of the strongest markers of sepsis severity. High lactate indicates tissue hypoxia and poor perfusion.

**Normal Range:**
0.5–2.0 mmol/L

**Sepsis Interpretation:**

* > 2 = concern
* > 4 = severe sepsis or septic shock

**Example Use in Tableau:**
Track lactate rise as sepsis worsens.

---

## Alkalinephos (Alkaline Phosphatase)

**Definition:**
An enzyme related to liver and bile duct function.

**Clinical Importance:**
Can increase in sepsis due to liver dysfunction or systemic inflammation.

**Normal Range:**
44–147 IU/L

**Example Use in Tableau:**
Study liver stress during sepsis.

---

## Phosphate

**Definition:**
Mineral important for energy production and cellular repair.

**Clinical Importance:**
Abnormal phosphate levels may indicate kidney dysfunction, malnutrition, or severe metabolic stress in sepsis.

**Normal Range:**
2.5–4.5 mg/dL

**Example Use in Tableau:**
Evaluate metabolic instability in sepsis.

---

# Tableau Insights to Build

### Worksheet 13: Lactate Distribution

* X-axis: Lactate
* Color: SepsisLabel
* Goal: Identify severe hypoperfusion.

### Worksheet 14: Lactate Over Time

* X-axis: Hour
* Y-axis: Lactate
* Goal: Track worsening tissue hypoxia.

### Worksheet 15: Phosphate vs Sepsis

* X-axis: Phosphate
* Color: SepsisLabel
* Goal: Observe metabolic instability.

### Worksheet 16: Alkalinephos Levels

* X-axis: Alkalinephos
* Color: SepsisLabel
* Goal: Monitor liver stress.

# 6. Liver Dysfunction Markers

## Bilirubin-direct

**Definition:**
Measures conjugated bilirubin processed by the liver.

**Clinical Importance:**
High direct bilirubin may indicate liver dysfunction, bile flow obstruction, or organ stress during sepsis.

**Normal Range:**
0.0–0.3 mg/dL

**Example Use in Tableau:**
Evaluate liver injury patterns in septic patients.

---

## Bilirubin-total

**Definition:**
Measures total bilirubin in the blood, including direct and indirect bilirubin.

**Clinical Importance:**
Elevated total bilirubin can indicate impaired liver function, which may occur in severe sepsis or multi-organ dysfunction.

**Normal Range:**
0.1–1.2 mg/dL

**Sepsis Interpretation:**
High bilirubin may suggest worsening organ failure.

**Example Use in Tableau:**
Compare liver dysfunction between sepsis and non-sepsis groups.

---

# Tableau Insights to Build

### Worksheet 17: Total Bilirubin by Sepsis

* X-axis: Bilirubin-total
* Color: SepsisLabel
* Goal: Identify liver dysfunction patterns.

### Worksheet 18: Direct vs Total Bilirubin

* X-axis: Bilirubin-direct
* Y-axis: Bilirubin-total
* Color: SepsisLabel
* Goal: Compare liver marker relationships.

# 7. Kidney Function and Electrolyte Markers

## Creatinine

**Definition:**
Waste product filtered by the kidneys.

**Clinical Importance:**
High creatinine suggests kidney dysfunction, a common complication in sepsis.

**Normal Range:**
0.6–1.3 mg/dL

**Sepsis Interpretation:**
Higher values often indicate acute kidney injury (AKI).

**Example Use in Tableau:**
Track kidney injury severity.

---

## BUN (Blood Urea Nitrogen)

**Definition:**
Measures nitrogen waste in the blood.

**Clinical Importance:**
Elevated BUN can indicate kidney failure, dehydration, or poor circulation in sepsis.

**Normal Range:**
7–20 mg/dL

**Example Use in Tableau:**
Compare kidney stress across patients.

---

## Calcium

**Definition:**
Important mineral for nerve, muscle, and heart function.

**Clinical Importance:**
Low calcium is common in severe sepsis and may be linked to poor outcomes.

**Normal Range:**
8.5–10.5 mg/dL

**Example Use in Tableau:**
Study calcium imbalance in septic patients.

---

## Chloride

**Definition:**
Electrolyte involved in fluid balance and acid-base regulation.

**Clinical Importance:**
Abnormal chloride may reflect metabolic imbalance in sepsis.

**Normal Range:**
96–106 mEq/L

**Example Use in Tableau:**
Monitor fluid and electrolyte shifts.

---

# Tableau Insights to Build

### Worksheet 19: Creatinine by Sepsis

* X-axis: Creatinine
* Color: SepsisLabel
* Goal: Detect kidney dysfunction.

### Worksheet 20: BUN Distribution

* X-axis: BUN
* Color: SepsisLabel
* Goal: Compare waste accumulation.

### Worksheet 21: Calcium vs Sepsis

* X-axis: Calcium
* Color: SepsisLabel
* Goal: Identify mineral imbalance.

### Worksheet 22: Chloride Trends

* X-axis: Chloride
* Color: SepsisLabel
* Goal: Observe electrolyte changes.

# 8. Oxygenation, Energy, and Cardiac Stress Markers

## FiO2 (Fraction of Inspired Oxygen)

**Definition:**
The percentage of oxygen a patient is receiving.

**Clinical Importance:**
Higher FiO2 often means the patient needs oxygen support due to respiratory distress.

**Normal Range:**
21% (room air)

**Sepsis Interpretation:**
Higher FiO2 may indicate severe lung involvement.

**Example Use in Tableau:**
Analyze oxygen dependency in septic patients.

---

## SaO2 (Arterial Oxygen Saturation)

**Definition:**
Measures how much oxygen is bound to hemoglobin in arterial blood.

**Clinical Importance:**
Low SaO2 indicates poor oxygen delivery.

**Normal Range:**
95–100%

**Example Use in Tableau:**
Compare oxygenation levels.

---

## Glucose

**Definition:**
Blood sugar level.

**Clinical Importance:**
Sepsis can cause hyperglycemia due to stress response or hypoglycemia in severe organ failure.

**Normal Range:**
70–140 mg/dL

**Example Use in Tableau:**
Track glucose instability.

---

## Troponin I

**Definition:**
A protein released when heart muscle is damaged.

**Clinical Importance:**
Elevated Troponin I may indicate cardiac injury in severe sepsis.

**Normal Range:**
<0.04 ng/mL

**Example Use in Tableau:**
Measure cardiac stress during sepsis.

---

# Tableau Insights to Build

### Worksheet 23: FiO2 by Sepsis

* X-axis: FiO2
* Color: SepsisLabel
* Goal: Assess oxygen support needs.

### Worksheet 24: SaO2 Distribution

* X-axis: SaO2
* Color: SepsisLabel
* Goal: Compare oxygen saturation.

### Worksheet 25: Glucose Levels

* X-axis: Glucose
* Color: SepsisLabel
* Goal: Detect metabolic stress.

### Worksheet 26: Troponin I by Sepsis

* X-axis: TroponinI
* Color: SepsisLabel
* Goal: Identify cardiac injury.
# 9. Blood Oxygen, Liver Injury, and Coagulation Markers

## Hgb (Hemoglobin)

**Definition:**
Protein in red blood cells that carries oxygen.

**Clinical Importance:**
Low hemoglobin reduces oxygen delivery to tissues, worsening sepsis-related hypoxia.

**Normal Range:**

* Male: 13.5–17.5 g/dL
* Female: 12.0–15.5 g/dL

**Example Use in Tableau:**
Study oxygen transport efficiency.

---

## AST (Aspartate Aminotransferase)

**Definition:**
An enzyme found in the liver and other tissues.

**Clinical Importance:**
Elevated AST may indicate liver damage or cellular injury during severe sepsis.

**Normal Range:**
10–40 U/L

**Example Use in Tableau:**
Track liver injury severity.

---

## PTT (Partial Thromboplastin Time)

**Definition:**
Measures how long blood takes to clot.

**Clinical Importance:**
Prolonged PTT may indicate coagulation dysfunction, common in severe sepsis and DIC.

**Normal Range:**
25–35 seconds

**Example Use in Tableau:**
Assess clotting abnormalities.

---

# Tableau Insights to Build

### Worksheet 27: Hemoglobin by Sepsis

* X-axis: Hgb
* Color: SepsisLabel
* Goal: Compare oxygen-carrying capacity.

### Worksheet 28: AST Levels

* X-axis: AST
* Color: SepsisLabel
* Goal: Detect liver injury.

### Worksheet 29: PTT Distribution

* X-axis: PTT
* Color: SepsisLabel
* Goal: Measure coagulation delays.
