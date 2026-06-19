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
