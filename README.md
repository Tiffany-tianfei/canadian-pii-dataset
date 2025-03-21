# Canada-Specific PII Database for Detection and Analysis

## **Project Objective**  
This project aims to **build a structured and scalable database containing synthetic Canadian personal identifiable information (PII)**. The dataset is designed for **PII detection, privacy-preserving analysis, and financial applications**, ensuring compliance with Canadian formatting standards.  

## **Methodology**  

### **1. Sentence Generation Using a Large Language Model (LLM)**
- Sentences are generated using an **LLM**, with **placeholders** replacing sensitive data to facilitate structured processing.  
- The generated text primarily focuses on **financial contexts**, including:  
  - Banking notifications  
  - Customer identity verification  
  - Fraud alerts  
  - Credit card approvals  

**Example of an LLM-generated sentence with placeholders:**  
"Your loan application is being processed, [NAME]. Please confirm your details."


### **2. Synthetic PII Generation Using Faker and Custom Rules**
- After generating placeholder-based sentences, **Python Faker** is used to generate **synthetic Canadian PII**, including:  
  - Names, emails, phone numbers  
  - Canadian Social Insurance Numbers (SIN)  
  - Canadian passport numbers  
  - Street addresses and postal codes  
- For PII types not natively supported by Faker (e.g., SIN, PR numbers), **custom validation rules** are applied to ensure compliance with Canadian formatting standards.

### **3. Replacing Placeholders with Synthetic PII**
- The generated PII values replace the corresponding placeholders in the LLM-generated sentences.  
- If Faker cannot produce a valid value, **local formatting rules** are applied to generate compliant data.  

**Example of a final sentence after PII replacement:**  
"Your loan application is being processed, John Smith. Please confirm your details."


## **Project Structure**  



### **Key Components**
1. **Simple Faker Generator**  
   - Directly generates synthetic **Canadian-style** PII, ensuring **data accuracy and privacy**.  

2. **LLM-Generated Sentences (Placeholder-Based)**  
   - Produces **diverse financial and banking-related sentences** with placeholders, facilitating structured text analysis.  


## **Advantages of This Approach**  

### **1. Privacy-Preserving Yet Realistic**
- No real PII is used; all data is **synthetically generated** to match **Canadian-specific formats**.  

### **2. Flexible and Scalable**
- Supports **multiple PII types** with structured data formatting.  
- Enables **bulk data generation and seamless updates** without affecting sentence structures.  

### **3. Suitable for Multiple Applications**
- **Training PII detection models** for financial and regulatory use cases.  
- **Testing anonymization techniques** in AI-driven systems.  
- **Conducting privacy-preserving data analysis** for compliance and security assessments.  

## **Conclusion**  
This project provides a **structured, anonymized, and scalable dataset of Canadian PII**. By leveraging **LLMs, Faker, and Gretel AI**, it ensures **data quality, compliance, and flexibility** for various applications in AI development, financial security, and regulatory compliance.  
