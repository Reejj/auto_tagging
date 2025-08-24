# Auto Tagging Support Tickets using LLM

## 📌 Objective
The goal of this project is to automatically classify support tickets into relevant categories using **Large Language Models (LLMs)**.  
We demonstrate **zero-shot** and **few-shot** classification approaches with Hugging Face Transformers.

This is part of the **DevelopersHub AI/ML Engineering Internship – Advanced Task 5**.

---

## 📊 Dataset
**Name:** [Twitter Customer Support (TwiCS)](https://www.kaggle.com/datasets/thoughtvector/customer-support-on-twitter)  
**File Used:** `twcs.csv`  

Since the dataset is large, it is **not included** in this repository.  
Please download it directly from Kaggle and place it inside the `data/` folder.

---

## 🛠 Approach
1. **Zero-Shot Classification**  
   - Used Hugging Face `facebook/bart-large-mnli` model (and lighter `distilbart-mnli` for faster runs).  
   - Provided candidate categories such as `billing`, `login issue`, `bug`, `refund`, etc.  
   - Model predicts top 3 probable categories per ticket without training.  

2. **Few-Shot Classification (Optional)**  
   - Added example ticket→label pairs to guide the model.  
   - Compared performance with zero-shot predictions.  

3. **Evaluation**  
   - Since dataset does not have explicit labels like “billing” or “bug”, we demonstrated classification results on sample tickets.  
   - Printed top-3 predictions for each support ticket.  

---

## 📈 Results
- Zero-shot classification successfully tags support tickets into relevant categories.  
- Example:
