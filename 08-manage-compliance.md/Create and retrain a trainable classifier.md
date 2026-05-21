## Create and Retrain a Trainable Classifier – Summary

### Overview:
- A **trainable classifier** is a machine learning model you:
  - ✅ Train using sample content  
  - ✅ Test for accuracy  
  - ✅ Publish for use in policies  
- You can **retrain it over time** to improve precision  

---

# ✅ Part 1: Create a Trainable Classifier

## Step-by-Step Process:

---

### 1. Prepare Seed Data (Training Data)
- Collect:
  - ✅ 50–500 **positive samples only**
- These must:
  - Strongly represent the content category  

⚠️ Important:
- Poor-quality samples = poor model accuracy  

---

### 2. Store Seed Data
- Upload samples to:
  - SharePoint Online folder  
- Ensure:
  - Folder contains **only training data**  

✅ Wait ~1 hour for indexing  

---

### 3. Create Classifier in Purview
- Go to:
  - **Microsoft Purview → Data classification → Classifiers**
- Select:
  - **+ Create trainable classifier**
- Provide:
  - Name  
  - Description  
  - Seed data location (SharePoint URL)  

---

### 4. Build Initial Model
- System processes seed data  
- Time required:
  - Up to **24 hours**  

Status:
- ➡️ *In progress* → *Need test items*  

---

### 5. Prepare Test Data
- Collect:
  - ✅ At least **200 test items** (recommended)  
- Include:
  - Positive samples  
  - Negative samples  
  - Ambiguous samples  

---

### 6. Upload Test Data
- Store in separate SharePoint folder  
- Add location in classifier  

✅ Processing time:
- ~1 hour  

---

### 7. Review Predictions
- Status becomes:
  - ✅ **Ready to review**  

---

### 8. Validate Results
- Review items (30 at a time)
- For each item:
  - ✅ Yes (correct)  
  - ❌ No (incorrect)  
  - ⚠️ Not sure  

✅ Review at least 200 items  

---

### 9. Publish Classifier
- When accuracy stabilizes:
  - Status → **Ready to use**  
- Click **Publish**

---

## After Publishing:
Classifier can be used in:
- ✅ Sensitivity auto-labeling  
- ✅ Retention policies  
- ✅ Communication compliance  
- ✅ DLP policies  

---

# ✅ Part 2: Retrain a Trainable Classifier

## Why Retrain?
- Improve:
  - Accuracy  
  - Precision  
  - Reduction in false positives  

---

## Key Concept:
👉 Retraining is based on **user feedback**

---

## Retraining Process:

---

### 1. Go to Content Explorer
- Navigate:
  - **Data classification → Content Explorer**

---

### 2. Select Classifier
- Filter:
  - Trainable classifiers  
- Choose classifier to retrain  

---

### 3. Review Classified Items
- Identify:
  - ✅ Correct matches  
  - ❌ Incorrect matches  

💡 Focus on:
- “Close matches” for best improvement  

---

### 4. Provide Feedback
For each item:
- Select:
  - ✅ Match  
  - ❌ Not a match  
- Optionally:
  - Suggest another classifier  

---

### 5. Submit Feedback
- After **30 feedback entries**:
  - Retraining begins automatically  

---

### 6. Retraining Execution
- Time:
  - ✅ 1–4 hours  

⚠️ Limit:
- Max **2 retraining cycles per day**

---

### 7. Review Results
- Compare:
  - Current model vs retrained model  
- Evaluate:
  - Prediction improvements  

---

### 8. Republish (Optional)
- If satisfied:
  - ✅ Republish updated classifier  
- If not:
  - Provide more feedback → retrain again  

---

## Important Notes:
- ❌ Cannot retrain:
  - Microsoft **pretrained classifiers**
- ✅ Feedback:
  - Stays within your tenant (not sent to Microsoft)
- ⏱️ Data may take:
  - Up to **8 days** to appear in Content Explorer  

---

## End-to-End Workflow:

1. Create classifier → seed data  
2. Test classifier → review predictions  
3. Publish classifier  
4. Monitor results in Content Explorer  
5. Provide feedback  
6. Retrain classifier  
7. Republish improved model  

---

## Best Practices:

- ✅ Use high-quality training samples  
- ✅ Include diverse test data  
- ✅ Review sufficient test items (200+)  
- ✅ Focus on false positives/negatives  
- ✅ Retrain regularly  
- ✅ Monitor performance in reports  

---

## Example Scenario:

### Goal:
- Detect internal “Confidential Contracts”

---

### Steps:
- Train classifier with:
  - Contract documents  
- Test with:
  - Contracts + unrelated files  
- Publish classifier  
- Use in:
  - Auto-labeling  
- Retrain:
  - Based on misclassified documents  

---

## Key Takeaway:
Creating and retraining trainable classifiers enables organizations to:
- Accurately classify complex content  
- Continuously improve detection  
- Reduce manual effort  
- Strengthen DLP and compliance controls  

➡️ With regular retraining, classifiers evolve into **highly precise, business-specific data protection tools**
