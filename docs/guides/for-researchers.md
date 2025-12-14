# TAKFAT-Yawn-Index for Researchers

## Technical Documentation for Scientific Community

This document provides detailed information for researchers interested in analyzing data, contributing scientific expertise, or building upon this citizen-science project.

## Project Overview

### Research Focus

Investigation of potential correlations between yawning patterns (yawn frequency, timing, context) and autonomic nervous system (ANS) function, with particular interest in post-viral autonomic dysfunction.

### Study Type

- **Design**: Observational, longitudinal, open cohort
- **Data Collection**: Self-reported with optional objective wearable data
- **Population**: Open enrollment, all ages, voluntary participation
- **Duration**: Ongoing, rolling enrollment
- **Framework**: Citizen science / participatory research

### Primary Research Question

Do yawning patterns correlate with markers of autonomic nervous system function (particularly HRV) and autonomic health status?

### Secondary Questions

1. Association between yawn frequency and sleep quality
2. Differences in yawn patterns between long COVID and control groups
3. Circadian and environmental influences on yawning
4. Correlation between yawning and subjective measures (stress, energy, fatigue)

## Scientific Background

### Yawning Physiology

**Known Mechanisms:**
- Associated with arousal and attention regulation
- Potential thermoregulatory function (brain cooling hypothesis)
- Dopaminergic system involvement
- Social/empathetic component (contagious yawning)

**Neurological Basis:**
- Hypothalamic control (paraventricular nucleus)
- Brainstem coordination
- Cortical involvement in contagious yawning (mirror neurons)

**Triggers:**
- Drowsiness and sleep transitions
- Boredom and low stimulation
- Temperature changes
- Social observation (contagious yawning)

### Autonomic Nervous System Function

**Key Concepts:**
- Sympathetic vs. parasympathetic balance
- Heart rate variability as ANS marker
- Autonomic dysfunction in disease states
- Post-viral autonomic syndromes (POTS, dysautonomia)

**Long COVID Relevance:**
- Documented autonomic dysfunction in subset of patients
- HRV changes post-COVID infection
- Dysautonomic symptoms: fatigue, tachycardia, exercise intolerance
- Need for accessible monitoring approaches

## Data Structure and Access

### Data Repository

**Location**: GitHub repository (this repo)
**Path**: `data/submissions/`
**Format**: CSV and JSON
**Schema**: See [data-schema.md](../data-schema.md)

### Data Fields

**Participant Demographics:**
```
- participant_id (anonymous)
- age_range (categorical)
- gender (optional)
- health_status (categorical)
- long_covid_status (boolean)
- region (broad geographic)
```

**Yawn Events:**
```
- timestamp (ISO 8601)
- duration (short/medium/long)
- context (standardized categories)
- environment (indoor/outdoor)
- temperature_comfort (scale)
- contagious (boolean)
```

**Daily Summaries:**
```
- total_yawns
- sleep_hours, sleep_quality
- stress_level, energy_level
- physical_activity_minutes
- caffeine_intake
```

**Wearable Data (optional):**
```
- HRV (RMSSD, SDNN)
- resting_heart_rate
- activity metrics
- sleep metrics
```

### Data Quality Considerations

**Strengths:**
- Large potential sample size
- Longitudinal within-subject data
- Real-world ecological validity
- Minimal cost and barrier to entry

**Limitations:**
- Self-report bias
- Selection bias (volunteer sample)
- Variable compliance and completion
- Heterogeneous measurement protocols
- Missing data
- No validated outcome measures

**Validation Approaches:**
- Flag outliers and implausible values
- Assess internal consistency
- Compare subgroups with known differences
- Sensitivity analyses excluding low-quality data

## Statistical Analysis Framework

### Descriptive Analysis

**Variables:**
- Yawn Index (mean daily yawns)
- Yawn frequency distribution
- Temporal patterns (hourly, daily, weekly)
- Context-specific rates

**Visualization:**
- Histograms of yawn frequency
- Time series plots
- Heatmaps of yawn timing
- Box plots by group

### Inferential Statistics

**Correlational Analyses:**

Primary correlation:
```
Pearson/Spearman r between Yawn Index and HRV
Control for: age, sleep quality, health status
```

Secondary correlations:
```
Yawn Index ~ Sleep Quality
Yawn Index ~ Stress Level
Yawn Index ~ Physical Activity
```

**Group Comparisons:**

Long COVID vs. Control:
```
Independent t-test or Mann-Whitney U
Effect size: Cohen's d with 95% CI
Adjust for confounders: age, sex, activity level
```

Age groups:
```
One-way ANOVA or Kruskal-Wallis
Post-hoc: Bonferroni correction
```

**Regression Models:**

Multiple linear regression:
```
Yawn_Index = β0 + β1(HRV) + β2(Sleep) + β3(Stress) + 
             β4(Age) + β5(Activity) + ε
```

Mixed-effects models (if adequate sample):
```
Level 1: Daily yawn count ~ Time + HRV + Sleep + Stress
Level 2: Random intercept and slope by participant
```

**Time Series Analysis:**

Circadian patterns:
```
Aggregate by hour-of-day
Fit sinusoidal model
Identify peak yawning times
Compare morning vs. afternoon vs. evening
```

Autocorrelation:
```
Assess day-to-day correlation
Determine optimal tracking period
```

### Sample Size and Power

**Current Status:**
- Rolling enrollment, no fixed N
- Planned interim analyses at N=30, 100, 300

**Power Analysis:**

For correlation (r = 0.3, α = 0.05, power = 0.80):
```
Required N ≈ 85 participants
```

For group comparison (d = 0.5, α = 0.05, power = 0.80):
```
Required N ≈ 64 per group
```

**Recommendations:**
- Report actual sample size with all analyses
- Compute observed power post-hoc
- Use confidence intervals (not just p-values)
- Interpret with caution given citizen science context

## Methodological Considerations

### Validity

**Construct Validity:**
- Is self-reported yawn count valid measure?
- Does Yawn Index capture meaningful individual differences?
- Are categories (duration, context) reliable?

**Internal Validity:**
- Observer effects (tracking changes behavior)
- Demand characteristics (participants guess hypothesis)
- Confounding variables not measured

**External Validity:**
- Volunteer sample differs from general population
- Self-selection for interest in health/science
- Generalizability limited

### Reliability

**Test-Retest:**
- Unknown for yawn tracking
- May vary by individual and context
- Could assess with repeated tracking periods

**Inter-Rater:**
- Not applicable (self-report)
- Could validate with observer in subset

**Internal Consistency:**
- Assess within-week stability
- Compare weekdays vs. weekends
- Check for systematic drift over time

### Bias Assessment

**Selection Bias:**
- Volunteers likely differ from non-participants
- May attract health-conscious individuals
- Potential over-representation of long COVID interest

**Recall Bias:**
- Real-time tracking preferred
- Retrospective counts less accurate
- May forget yawns (under-counting)
- May over-count if anxious about participation

**Social Desirability:**
- Minimal expected (yawning not stigmatized)
- Possible pressure to report "interesting" patterns

**Mitigation:**
- Transparent documentation of limitations
- Sensitivity analyses
- Compare early vs. late tracking days
- Assess for systematically implausible data

## Research Ethics

### Ethical Framework

**Principles:**
1. **Autonomy**: Voluntary participation, informed consent
2. **Beneficence**: Aim to generate useful knowledge
3. **Non-maleficence**: Minimize risks (minimal risk project)
4. **Justice**: Open to all, no discrimination

### IRB Status

**Not Formally Approved:**
- Informal citizen science project
- Not medical research
- No institutional affiliation currently
- Not intended for clinical application

**Alignment with Ethical Standards:**
- Follows general research ethics principles
- Strong privacy protections (anonymization)
- Transparent methods and open data
- No deception or withholding information

### Data Privacy

**Protections:**
- No collection of identifiable information
- Participant-generated anonymous IDs
- Public repository (all data already public)
- No commercial use

**Compliance Considerations:**
- GDPR: Aligns with principles (consent, minimization, transparency)
- COPPA: Parental consent required for children
- HIPAA: Not applicable (not collecting PHI)

### Informed Consent

**Elements Provided:**
- Project purpose and procedures
- Data usage and sharing
- Risks (minimal) and benefits (learning, contribution)
- Voluntary nature and right to withdraw
- Contact information
- Privacy protections

**Process:**
- Documented in README and CONTRIBUTING.md
- Participation implies consent
- Can withdraw by requesting data deletion

## Contributing as a Researcher

### Ways to Contribute

1. **Scientific Input**
   - Review and critique methodology
   - Suggest hypothesis refinements
   - Provide literature context
   - Identify potential biases

2. **Data Analysis**
   - Conduct statistical analyses
   - Create visualizations
   - Write interpretation summaries
   - Share code and methods

3. **Validation Studies**
   - Compare with clinical data
   - Conduct laboratory validation
   - Test against gold-standard measures
   - Assess reliability and validity

4. **Literature Synthesis**
   - Compile relevant yawning research
   - Review autonomic function literature
   - Identify knowledge gaps
   - Suggest future directions

5. **Tool Development**
   - Create analysis scripts
   - Build visualization dashboards
   - Develop mobile apps
   - Improve data collection instruments

### Collaboration Opportunities

**Academic Partnerships:**
- Use as pilot for formal studies
- Validate methods in research setting
- Contribute to publications
- Supervise student projects

**Data Requests:**
- All data is already public and available
- No special permission needed
- Attribution appreciated
- Share findings back to community

## Analysis Code and Reproducibility

### Computational Environment

**Recommended Tools:**
```
R or Python for analysis
Git for version control
Jupyter/RMarkdown for notebooks
```

**Required Packages (Python example):**
```python
pandas  # Data manipulation
numpy   # Numerical operations
scipy   # Statistical tests
matplotlib/seaborn  # Visualization
statsmodels  # Regression models
```

**Required Packages (R example):**
```r
tidyverse  # Data manipulation and viz
lme4       # Mixed models
ggplot2    # Visualization
psych      # Descriptive stats
```

### Analysis Pipeline

**Step 1: Data Import**
```python
import pandas as pd
data = pd.read_csv('data/submissions/aggregated.csv')
```

**Step 2: Cleaning**
```python
# Remove outliers
# Handle missing values
# Validate value ranges
# Create derived variables
```

**Step 3: Descriptive Statistics**
```python
# Calculate Yawn Index per participant
# Summarize distributions
# Create visualizations
```

**Step 4: Inferential Analysis**
```python
# Correlations
# Group comparisons
# Regression models
```

**Step 5: Visualization**
```python
# Create publication-quality figures
# Export for sharing
```

### Reproducibility Checklist

- [ ] Code is documented and commented
- [ ] Random seeds set for reproducibility
- [ ] Package versions documented
- [ ] Data provenance tracked
- [ ] Analysis pre-registered or documented
- [ ] All steps from raw data to results included
- [ ] Figures have generating code
- [ ] Results match reported findings

## Publication and Sharing

### Open Science Practices

**Encouraged:**
- Preprints on bioRxiv, PsyArXiv, etc.
- Open access publication
- Sharing analysis code on GitHub
- Depositing data on Zenodo/OSF (already public here)
- Pre-registration of analyses

### Authorship

**Community Contribution Model:**
- Credit "TAKFAT Community Contributors" as data providers
- Individual researchers author analyses
- Acknowledge specific technical contributors
- Follow standard authorship guidelines for analysis

### Citation

**For the Project:**
```
TAKFAT-Yawn-Index Project. (2025). 
Citizen Science Investigation of Yawning and Autonomic Health.
GitHub repository: https://github.com/ljgreen1234/TAKFAT-Public
```

**For Data:**
```
TAKFAT Community Contributors. (2025).
Yawn Tracking Dataset [Data set].
Available at: [repository URL]
```

## Quality Assurance

### Data Validation

**Automated Checks:**
```python
def validate_yawn_data(df):
    # Check required fields present
    # Validate date formats
    # Check value ranges
    # Flag implausible patterns
    # Return quality score
```

**Manual Review:**
- Inspect outliers
- Check for patterns suggesting fake data
- Verify anonymization
- Assess completeness

### Analysis Validation

**Internal Validation:**
- Check for coding errors
- Verify statistical assumptions
- Assess model fit
- Conduct sensitivity analyses

**External Validation:**
- Compare with published literature
- Seek peer review
- Share with community for feedback
- Replicate in independent sample if possible

## Future Directions

### Methodological Improvements

1. **Validated Instruments**: Develop standardized yawn tracking protocol
2. **Objective Measures**: Integrate video coding or EMG
3. **App Development**: Real-time mobile tracking
4. **Ecological Momentary Assessment**: Prompt-based sampling
5. **Wearable Integration**: Direct API connections to devices

### Research Extensions

1. **Interventions**: Test effects of sleep, temperature, breaks
2. **Experimental**: Manipulate yawn triggers systematically
3. **Comparative**: Cross-cultural or cross-species comparisons
4. **Longitudinal**: Track individuals over months/years
5. **Clinical**: Formal comparison with diagnosed conditions

### Integration Opportunities

1. **Other Projects**: Link with sleep or autonomic function studies
2. **Existing Datasets**: Compare with validated samples
3. **Clinical Trials**: Pilot as outcome measure
4. **Educational Research**: Study learning through participation

## Technical Support

### Getting Started

1. Clone repository
2. Review data schema
3. Explore existing data
4. Run example analyses
5. Contribute findings

### Resources

- [Data Schema](../data-schema.md)
- [Methodology](../methodology.md)
- [Example Analyses](../../examples/) (to be added)
- [FAQ](../FAQ.md) (to be created)

### Contact

- Open issues for questions
- Use "researcher" label
- Propose collaborations
- Share findings

## References

### Key Literature on Yawning

- Guggisberg, A. G., et al. (2010). Why do we yawn? *Neuroscience & Biobehavioral Reviews*
- Walusinski, O. (2014). How yawning switches the default-mode network to the attentional network
- Gallup, A. C., & Eldakar, O. T. (2013). The thermoregulatory theory of yawning

### Autonomic Function and HRV

- Shaffer, F., & Ginsberg, J. P. (2017). An overview of heart rate variability metrics
- Task Force of ESC and NASPE (1996). Heart rate variability standards
- Laborde, S., et al. (2017). Heart rate variability and cardiac vagal tone in psychophysiological research

### Long COVID and Autonomic Dysfunction

- Dani, M., et al. (2021). Autonomic dysfunction in 'long COVID'
- Johansson, M., et al. (2021). Long-haul COVID-19 symptoms presenting as a variant of postural orthostatic tachycardia syndrome
- Goldstein, D. S. (2021). The possible association between COVID-19 and postural tachycardia syndrome

### Citizen Science Methods

- Bonney, R., et al. (2014). Next steps for citizen science
- Kullenberg, C., & Kasperowski, D. (2016). What is citizen science?

---

**For questions or to contribute as a researcher, please open an issue with the "researcher" label.**

**We welcome scientific collaboration and peer review of methods and findings.**
