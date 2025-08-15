# Study Title

<!-- Replace with your actual study title -->

## 🎯 Purpose

<!-- Brief description of the research question and objectives -->

## 👥 Study Team

- **Lead**: [Lead Name] ([Lead Institution])
- **Analyst**: [Analyst Name] ([Institution])
- **Coordinator**: [Coordinator Name] ([Institution])

## 📋 Protocol

<!-- Link to protocol document -->
**Protocol**: [Link to protocol document]

**IRB Status**: [Lead-site IRB approval status and reference]

## 🏥 Data Partners

<!-- This section is automatically updated by partner management workflows -->

**Current Partner Count**: [Auto-updated by workflows]

**Partner Sites**: [Auto-managed list]

### Working with Data Partners

1. **Adding a new partner**: Use the "Add Data Partner" issue form to create a trackable issue for each site
2. **Partner status tracking**: Each partner has a dedicated issue that moves through: Potential → Invited → Diagnostics Sent → Diagnostics Returned → Package Executed → Results Uploaded
3. **Weekly nudges**: Automated weekly reminders (default: Monday 9 AM ET) for stale partner issues
4. **Configuring nudges**: Update repository variables if you need to change the schedule:
   - `NUDGE_DAY`: Day of week (Mon, Tue, Wed, etc.)
   - `NUDGE_HOUR_LOCAL`: Hour in 24-hour format (0-23)
   - `NUDGE_TZ`: Timezone (e.g., "America/New_York")

## 🏗️ Study Structure

### Cohorts & Phenotypes

<!-- Links to ATLAS cohort definitions -->
- **Target Cohort**: [ATLAS cohort link]
- **Outcome Cohort**: [ATLAS cohort link]
- **Additional Cohorts**: [Links as needed]

### Analysis Plan

<!-- Brief description or link to detailed analysis plan -->

## 📊 Current Stage

This study follows the standard OHDSI network study stages:

1. ✅ Protocol development
2. ⏳ Data diagnostics  
3. ⏳ Phenotype development
4. ⏳ Phenotype evaluation
5. ⏳ Analysis specifications
6. ⏳ Network execution
7. ⏳ Study diagnostics
8. ⏳ Evidence synthesis
9. ⏳ Results evaluation

**Current Stage**: [Auto-updated by workflows]

### How to Advance Stages

To move to the next stage, complete all items in the current stage checklist issue and close it. The study stage will automatically update in both this repository's project and the org-wide Factory view.

## 🔄 Execution

### For Study Leads

1. **Track progress**: Use the project board to see all stage checklists and partner issues
2. **Add partners**: Use issue forms to add new data partners
3. **Stage advancement**: Close stage checklist issues when milestones are complete
4. **Monitor partners**: Review weekly nudge summaries and respond to stale partners

### For Data Partners

1. **Find your site issue**: Look for an issue titled "Data Partner: [Your Site]"
2. **Check assignments**: You should be assigned to your site's issue
3. **Stay updated**: Comment on your issue with progress updates
4. **Request help**: Use issue comments to ask questions or request assistance

## 📁 Repository Structure

```
├── docs/               # Documentation
│   └── STRATEGUS.md   # Strategus scaffold (optional)
├── analysis/          # Analysis scripts and notebooks
├── cohorts/           # Cohort definitions and exports
├── results/           # Study results and outputs
└── data-partners/     # Partner-specific instructions and templates
```

## 🔧 Technical Implementation

### Analysis Environment

This study uses standard OHDSI tools and follows OHDSI best practices:

- **Database**: OMOP CDM v5.x or v6.x
- **Platform**: [Specify: R/HADES, Python, SQL, etc.]
- **Package Management**: [renv, conda, etc.]

### Optional: Strategus Integration

This repository can be enhanced with a [Strategus](https://ohdsi.github.io/Strategus/) scaffold for standardized execution across the network. See `docs/STRATEGUS.md` for details on adding Strategus support when it becomes stable.

## 📞 Support

- **Study questions**: Contact the study lead or create an issue
- **Technical issues**: Tag the analyst team in issue comments
- **OHDSI community**: Post in [OHDSI Forums](https://forums.ohdsi.org/)

## 📜 License

This study protocol and code are shared under [specify license] for use by the OHDSI community.

---

**Factory Integration**: This study is tracked in the [OHDSI Factory](link-to-factory-project) portfolio for organizational visibility and coordination.