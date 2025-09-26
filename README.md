# CreditSage AI 🚀

**From Credit Score Confusion to Financial Confidence.**

![iOS](https://img.shields.io/badge/iOS-15.0%2B-blue)
![SwiftUI](https://img.shields.io/badge/SwiftUI-4.0%2B-orange)
![Model](https://img.shields.io/badge/Model-XGBoost-success)
![License](https://img.shields.io/badge/License-MIT-green)

CreditSage AI is an iOS app that demystifies credit scores for young Indians. We replace fear and uncertainty with a clear, actionable path to financial goals, powered by a smart simulator and personalized action plans.

---

## The Problem

The CIBIL score is a critical number that dictates financial opportunity, yet for millions, it's a black box. The fear of making a mistake prevents proactive financial planning, blocking access to essential goals like getting a first credit card, a bike loan, or an education loan.

---

## A Winning User Experience ✨

Our solution is built on two core features designed to empower the user:

### **Feature 1: The "What-If" Simulator 🔮**

Our simulator lets you see the future. Users can interactively model the impact of financial decisions *before* they make them.
- *"What happens to my 'Good' rating if I take a new ₹50,000 loan?"*
- *"How does missing one payment affect my credit standing?"*

This provides a risk-free educational sandbox to learn the cause-and-effect of credit behavior.

### **Feature 2: The Goal-Driven Action Plan 🎯**

We connect your credit score to your real-life ambitions.
1.  **Set a Goal:** Tell the app what you want to achieve (e.g., "Qualify for a bike loan").
2.  **Get a Plan:** The app provides a simple, personalized checklist of actions to reach your goal.

This plan isn't based on generic advice; it's generated directly from our AI model's insights about what factors matter most for *your* profile.

---

## The Core ML Engine: Powered by XGBoost 🧠

The brain of CreditSage AI is a classification model that predicts a user's credit health.

-   **INPUT:** A user profile with 8 key values (Age, Income, Number of Loans, etc.).
-   **MODEL:** An **XGBoost (eXtreme Gradient Boosting)** classifier.
-   **OUTPUT:** A clear prediction of **Poor**, **Standard**, or **Good** credit standing.

<br>

<details>
<summary><b>Click to learn why XGBoost is the perfect choice for this project</b></summary>

### Why XGBoost?

Think of XGBoost as building a team of expert decision-makers. The first expert makes a prediction, the second focuses on correcting the first one's mistakes, the third corrects the second's, and so on. This process of learning from errors makes the final team incredibly smart and accurate.

-   **Highest Accuracy**: For tabular data (like our credit score dataset), XGBoost is king. It consistently wins Kaggle competitions because it captures the complex, non-obvious patterns in financial data far better than simpler models.

-   **Incredibly Fast**: Despite its power, XGBoost is highly optimized and trains in minutes. This allows for rapid experimentation and iteration.

-   **The Killer Feature: Built-in Feature Importance**: This is our secret sauce. After training, XGBoost shows us *exactly which factors* it considered most important for its predictions (e.g., `Num_of_Delayed_Payment` might be the #1 factor).
    -   **For our App:** This directly powers the **Goal-Driven Action Plan**. We use the model's top 3 most important features to generate your personalized advice.
    -   **For Presentations:** Showing this proves we understand *why* our model works and that it's not just a black box. 

</details>

---
<br>

## Technology Stack

-   **Machine Learning Model**: XGBoost (trained in a Python environment like Google Colab)
-   **iOS App**: SwiftUI for a modern, declarative UI
-   **ML Integration**: Core ML for on-device, private, and fast predictions
