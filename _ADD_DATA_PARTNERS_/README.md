# Data Partner Management System

## Overview
This directory contains the Data Partner Management System that automatically creates and manages Data Partner Issues when data partners are added to a study.

## How It Works

### 1. Add Data Partners
Add data partners to the `data_partners.csv` file with the following format:
```csv
Site Name,Contact Name,Contact GitHub Username
Johns Hopkins University,Jane Smith,janesmith
Mayo Clinic,Bob Johnson,bjohnson
Stanford Medicine,Alice Davis,adavis
```

### 2. Automatic Issue Creation
When you commit changes to `data_partners.csv`, the system will automatically:
- Create a new GitHub Issue for each data partner (if it doesn't exist)
- Title the issue with the Site Name
- Add the `data-partner` label
- Assign the issue to the Contact GitHub Username
- Set initial status to "Preparation"

### 3. Data Partner Issue Format
Each Data Partner Issue includes:
- **Title:** [Site Name]
- **Status:** Preparation (gray) → Analysis (orange) → Results (green)
- **Assignee:** Contact GitHub Username
- **Labels:** `data-partner`, `status:preparation`

### 4. Issue Body Content
```
Contact: [Contact Name]
Contact GitHub Username: @[Contact GitHub Username]
Days in Status: [Calculated days since last status change]

---

**Data Partner Information**
- **Site Name:** [Site Name]
- **Primary Contact:** [Contact Name]
- **GitHub Username:** @[Contact GitHub Username]
- **Current Status:** [Current Status]
- **Created:** [Creation Date]

**Status History**
- [Date]: Created with status "Preparation"
- [Date]: Changed status from "Preparation" to "Analysis" (X days in previous status)

---

*This is a Data Partner tracking issue. Status changes will be monitored to track partnership progress.*
```

## Data Partner Statuses

### 1. Preparation (Gray)
- Initial status when data partner is added
- Partner is being onboarded and prepared for analysis
- Label: `status:preparation`

### 2. Analysis (Orange)  
- Data partner is actively participating in analysis
- Analysis package is being executed
- Label: `status:analysis`

### 3. Results (Green)
- Analysis is complete and results are being finalized
- Data partner has completed their participation
- Label: `status:results`

## Managing Status Updates

### Manual Status Updates
Use the "Update Data Partner Status" workflow to manually update status:
1. Go to Actions → Update Data Partner Status
2. Click "Run workflow"
3. Enter:
   - Repository name
   - Issue number
   - New status

### Automatic Status Tracking
- The system automatically calculates "Days in Status"
- Status history is maintained in each issue
- Labels are updated automatically when status changes

## File Requirements

### CSV Format
- **Required columns:** Site Name, Contact Name, Contact GitHub Username
- **Headers:** Must be exact (case-sensitive)
- **Format:** Standard CSV with comma separators
- **GitHub Usernames:** Must be valid GitHub usernames (without @ symbol in CSV)

### Important Notes
- Removing rows from CSV has no effect (system only adds new partners)
- `data_partners.csv` should always contain the complete list of study data partners
- Duplicate entries (same Site Name) will not create duplicate issues
- Invalid GitHub usernames will cause assignment to fail but issues will still be created