# Research Methodology

## Overview

This document outlines the scientific methodology behind the TAKFAT-Yawn-Index project, including research questions, hypotheses, data collection procedures, and planned analyses.

## Research Questions

### Primary Research Question

**Can patterns in yawn frequency and characteristics reveal meaningful information about autonomic nervous system function?**

### Secondary Research Questions

1. Is there a correlation between yawn frequency and heart rate variability (HRV)?
2. Do individuals reporting long COVID symptoms show different yawn patterns?
3. Are yawn patterns associated with self-reported stress and energy levels?
4. How do environmental factors (temperature, lighting, activity) influence yawn frequency?
5. Are there circadian patterns in yawn occurrence?
6. Does physical activity level correlate with yawn patterns?

## Hypotheses

### Main Hypothesis

**H1**: Yawn frequency and patterns correlate with markers of autonomic nervous system function, particularly HRV.

**Rationale**: Yawning may be a behavioral manifestation of autonomic regulation. If yawning serves a thermoregulatory or arousal-modulating function controlled by the autonomic nervous system, we might observe correlations with autonomic measures like HRV.

### Supporting Hypotheses

**H2**: Individuals with self-reported long COVID symptoms show altered yawn patterns compared to controls.

**H3**: Higher stress levels correlate with increased yawn frequency.

**H4**: Yawn frequency follows a circadian pattern with peaks during transitions between sleep and wake states.

**H5**: Poor sleep quality correlates with increased daytime yawn frequency.

**H6**: Yawning is more frequent in temperature-uncomfortable environments.

## Study Design

### Study Type

- **Observational**: No intervention or manipulation
- **Longitudinal**: Repeated measurements over time
- **Citizen Science**: Participant-collected data
- **Open Data**: Publicly shared anonymized data

### Inclusion Criteria

- Any age (with parental consent for minors)
- Able to track yawns for minimum 7 consecutive days
- Willing to share anonymized data
- No specific health requirements

### Exclusion Criteria

None - this is an exploratory open science project

### Participant Groups (Optional Categories)

1. **Healthy controls**: Self-reported good general health
2. **Long COVID**: Self-reported post-COVID symptoms
3. **Chronic conditions**: Self-reported chronic health conditions
4. **Age groups**: Children, teens, adults, seniors

## Data Collection Procedures

### Tracking Period

**Minimum**: 7 consecutive days
**Recommended**: 14-28 days for better pattern detection
**Optimal**: Ongoing periodic tracking (e.g., one week per month)

### Data Collection Methods

#### Self-Report Yawn Tracking

**Real-time method** (preferred):
1. Record each yawn as it occurs
2. Note time, context, and environment
3. Add brief notes if relevant
4. Use smartphone app, paper log, or spreadsheet

**Recall method** (acceptable):
1. Count yawns during defined periods
2. Record at end of each period (e.g., every 2 hours)
3. Estimate context if exact details unavailable
4. Less precise but still valuable

#### Daily Summaries

End-of-day recording:
- Total yawn count
- Sleep quality and duration
- Stress level (subjective scale)
- Energy level (subjective scale)
- Physical activity
- Notable events or health changes

#### Wearable Data (Optional)

If available from fitness trackers:
- HRV measurements (preferably morning readings)
- Resting heart rate
- Step count and activity minutes
- Sleep metrics (duration, quality, stages)

### Data Quality Measures

**To ensure data quality:**

1. **Clear Instructions**: Provide detailed tracking guidelines
2. **Templates**: Use standardized forms and formats
3. **Consistency Checks**: Validate data for completeness and plausibility
4. **Participant Feedback**: Allow questions and clarifications
5. **Pilot Testing**: Test procedures with initial participants

**Quality Indicators:**

- ✓ Complete required fields
- ✓ Consistent time formats
- ✓ Reasonable value ranges
- ✓ Minimum tracking duration met
- ✓ Clear participant ID

## Measurement Definitions

### Yawn Index (Primary Outcome)

**Definition**: Average daily yawn count over tracking period

**Calculation**: 
```
Yawn Index = Total Yawns / Number of Days Tracked
```

**Interpretation**:
- Low: 0-5 yawns/day
- Moderate: 6-15 yawns/day
- High: 16+ yawns/day

### Secondary Outcome Measures

1. **Yawn Duration Distribution**: Proportion of short/medium/long yawns
2. **Circadian Yawn Pattern**: Time-of-day distribution
3. **Context-Specific Yawn Rate**: Yawns per activity type
4. **Yawn-HRV Correlation**: Relationship between daily yawn count and HRV
5. **Yawn Variability**: Day-to-day variation in yawn count

### Exposure Variables

1. **Sleep quality** (poor/fair/good/excellent)
2. **Stress level** (low/moderate/high)
3. **Physical activity** (minutes per day)
4. **Screen time** (hours per day)
5. **Caffeine intake** (none/low/moderate/high)
6. **Environmental temperature comfort** (5-point scale)

### Covariates

1. **Age range** (categorical)
2. **Gender** (optional)
3. **Health status** (categorical)
4. **Long COVID status** (yes/no)
5. **Geographic region** (broad categories)
6. **Season** (derived from date)

## Statistical Analysis Plan

### Descriptive Statistics

**For all participants:**
- Mean, median, standard deviation of Yawn Index
- Distribution plots of yawn frequency
- Time-of-day patterns (histograms)
- Context distribution (bar charts)

**By group:**
- Compare distributions across health status groups
- Compare long COVID vs. non-long COVID
- Compare age groups

### Inferential Statistics

**Correlational Analyses:**

1. **Yawn Index vs. HRV**
   - Pearson or Spearman correlation
   - Scatter plots with trend lines
   - Account for within-subject repeated measures

2. **Yawn Index vs. Sleep Quality**
   - Correlation analysis
   - Linear regression adjusting for covariates

3. **Yawn Index vs. Stress Level**
   - Correlation analysis
   - Group comparisons (low vs. moderate vs. high stress)

**Group Comparisons:**

1. **Long COVID vs. Controls**
   - Independent t-test or Mann-Whitney U test
   - Effect size estimation (Cohen's d)
   - Confidence intervals

2. **Age Group Differences**
   - ANOVA or Kruskal-Wallis test
   - Post-hoc pairwise comparisons

**Time Series Analyses:**

1. **Circadian Patterns**
   - Aggregate by hour of day
   - Identify peak yawning times
   - Compare morning vs. afternoon vs. evening

2. **Day-of-Week Effects**
   - Compare weekday vs. weekend patterns
   - ANOVA across days of week

### Multivariate Analyses

**Multiple Regression:**
```
Yawn Index ~ HRV + Sleep Quality + Stress + Activity + Age + [covariates]
```

**Mixed Effects Models** (if sufficient data):
```
Yawn Count ~ Time + HRV + [covariates] + (1 | Participant)
```

### Sample Size Considerations

As a citizen science project with rolling enrollment:
- No predetermined sample size
- Planned interim analyses as data accumulates
- Report sample size with all analyses
- Interpret with appropriate caution given sample characteristics

**Minimum targets:**
- 30 participants for preliminary analyses
- 100 participants for robust correlational analyses
- 300+ participants for subgroup analyses

## Limitations and Biases

### Known Limitations

1. **Self-Selection Bias**: Participants opt-in voluntarily
2. **Self-Report Bias**: Yawn counts may be inaccurate
3. **Recall Bias**: Retrospective counting less accurate
4. **Observer Effects**: Tracking may change behavior
5. **Missing Data**: Incomplete records common in citizen science
6. **Confounding**: Many unmeasured variables
7. **Causality**: Cannot establish causal relationships

### Mitigation Strategies

1. **Clear Instructions**: Minimize measurement error
2. **Data Validation**: Flag implausible values
3. **Sensitivity Analyses**: Test robustness of findings
4. **Transparent Reporting**: Document all limitations
5. **Conservative Interpretation**: Avoid overstatement
6. **Replication**: Encourage independent verification

## Data Analysis Workflow

### Step 1: Data Cleaning

1. Import all submitted data files
2. Standardize formats and field names
3. Check for missing required fields
4. Validate value ranges
5. Flag outliers for review
6. Document any exclusions

### Step 2: Exploratory Analysis

1. Calculate descriptive statistics
2. Create visualizations
3. Identify patterns and anomalies
4. Check data quality by participant
5. Assess completeness and consistency

### Step 3: Primary Analysis

1. Test main hypotheses
2. Calculate correlation coefficients
3. Perform group comparisons
4. Estimate effect sizes
5. Generate confidence intervals

### Step 4: Secondary Analysis

1. Explore additional relationships
2. Test secondary hypotheses
3. Conduct subgroup analyses
4. Investigate interesting patterns

### Step 5: Reporting

1. Create summary visualizations
2. Write results narrative
3. Acknowledge limitations
4. Share findings with community
5. Make analysis code available

## Ethical Considerations

### Principles

1. **Voluntary Participation**: No coercion
2. **Informed Consent**: Clear information about project
3. **Privacy Protection**: Strict anonymization
4. **Beneficence**: Aim to generate useful knowledge
5. **Justice**: Open to all who want to participate

### Risk Assessment

**Minimal Risk Project**:
- No physical interventions
- No collection of sensitive medical data
- No risk beyond normal daily activities
- No financial costs to participants

**Potential Benefits**:
- Learn about scientific process
- Increase self-awareness
- Contribute to collective knowledge
- Educational value

### Informed Consent Elements

Participants should understand:
- Purpose of the project
- What data will be collected
- How data will be used and shared
- That participation is voluntary
- That they can withdraw anytime
- How to contact researchers
- Limitations of the project

## Data Sharing and Transparency

### Open Science Practices

1. **Open Data**: All anonymized data publicly available
2. **Open Methods**: All procedures documented
3. **Open Analysis**: Analysis code shared
4. **Open Results**: Findings shared publicly
5. **Preregistration**: This methodology document serves as preregistration

### Data Repository

- Primary: GitHub repository (this repo)
- Secondary: May archive on Zenodo or OSF for DOI
- Format: CSV and JSON with metadata
- License: CC0 or CC-BY for data

## Future Directions

### Potential Enhancements

1. **Mobile App**: Easier real-time tracking
2. **Automated Analysis**: Regular aggregate reports
3. **Data Visualization Dashboard**: Interactive exploration
4. **Validated Instruments**: Standardized questionnaires
5. **Collaboration**: Partner with research institutions
6. **Longitudinal Follow-up**: Track participants over months/years

### Research Extensions

1. **Experimental Studies**: Test specific hypotheses
2. **Intervention Studies**: Effects of sleep, stress reduction
3. **Comparison Studies**: Validate against clinical data
4. **Meta-Analysis**: Combine with other yawning studies
5. **Physiological Validation**: Direct ANS measurements

## References and Background

### Scientific Basis

**Yawning Research:**
- Yawning serves thermoregulatory and arousal functions
- Associated with dopaminergic system activity
- Contagious yawning involves empathy networks
- Frequency increases with fatigue and boredom

**Autonomic Nervous System:**
- Controls involuntary physiological functions
- Heart rate variability reflects ANS balance
- Can be affected by stress, sleep, and health conditions
- Dysautonomia reported in some long COVID cases

**Relevant Literature** (examples):
- Guggisberg et al. (2010): "Why do we yawn?"
- Shaffer & Ginsberg (2017): "An Overview of Heart Rate Variability Metrics"
- Studies on autonomic dysfunction in post-viral syndromes

## Updates and Versioning

**This methodology document:**
- Version 1.0: Initial release (December 2025)
- Living document: May be updated with community input
- Major changes will be versioned and documented
- All versions maintained in version control

## Questions and Contributions

**Have suggestions for improving the methodology?**
- Open an issue for discussion
- Provide scientific references
- Suggest additional analyses
- Identify potential biases we should address

---

**Document Version**: 1.0
**Last Updated**: December 2025
**Status**: Active
