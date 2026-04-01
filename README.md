# CFR_TEST
# Verification & Validation Project – 21 CFR Atomic Rules

## Project Overview

This project is designed to teach students **Verification & Validation (V&V) of regulatory requirements** using Python scripts, JSON files, and GitHub Actions. Students will work in **groups** to extract rules from CFR sections, produce atomic units, generate expected structure, and create test cases. An **individual component** will involve LLM-based test case generation.

---

## Inputs

1. **Markdown file with CFR section**  
   - Example: `21_CFR_117.130.md`in Input CFR File
   - Contains hierarchical rules with **parent sections and atomic units**.
   - Example snippet: See sample output for requirement_json, expected_structure.json, and test_cases.json
  

## **Group Project Tasks**

### **Task 1: Extract and Structure Requirements**
- Use the provided **Python script** to parse the Markdown CFR section (`21_CFR_117.130.md`) into `requirements.json`.
  
- **Pick 10 atomic rules** from the parsed list.
- Modify the provided python script to generate `expected_structure.json` mapping:
  - Parent requirement ID → list of child letters
  - Modify the script if necessary to:
      - Ignore parent/child numbering in the Markdown
      -Correctly assign child letters


### **Task 2: Generate Minimal Test Cases**
Write a script generate_test_cases.py to produce test_cases.json.
 -Input: requirements.json and selected 10 rules in expected_structure.json.
 -Output format (one test case per requirement):

### **Task 3: Verification and Validation**
 Use scripts from Assignment 6 for verification and validation.

### **Individual Task**
- Generate LLM-based test cases for 5 selected rules.
- Use two LLMs: Mistral and quantized Mistral.
- Each test case should include:

   -test_case_id: Unique ID (e.g., TC-001)
   - requirement_id: Requirement being tested
   -description: What the test verifies
   - input_data: What input the test uses
   -expected_output: What result is expected
   -steps (optional): Step-by-step actions
  - notes (optional): Any special assumptions

 -Compare coverage, correctness, and completeness of outputs.
 -Coverage:
      Did both LLMs produce at least one test case for this requirement?
 -Correctness:
      Does the description match the requirement?
      Check if the test actually tests what the requirement says.
 -Completeness:
      Are all required fields present?
      test_case_id, requirement_id, description, input_data, expected_output
      Are optional fields (steps, notes) useful?




  
2. 

