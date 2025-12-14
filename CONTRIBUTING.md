# Contributing to TAKFAT-Yawn-Index

Thank you for your interest in contributing to our citizen-science experiment! This guide will help you get started with tracking yawns and contributing to our collective understanding of autonomic health.

## 🎯 Ways to Contribute

### 1. As a Participant (Data Contributor)

Track your yawns and submit anonymized data to help us identify patterns.

**Getting Started:**
1. Choose a tracking method (paper, spreadsheet, or app)
2. Use our templates from `data/templates/`
3. Track for at least 7 consecutive days
4. Anonymize your data (see below)
5. Submit via pull request or issue

### 2. As an Educator

Use this project as a teaching tool in your classroom or homeschool.

**What You Can Do:**
- Adapt our materials for your students
- Share lesson plans and activities
- Provide feedback on educational content
- Submit anonymized class aggregate data

### 3. As a Developer

Help improve our tools, templates, and data analysis.

**Contribution Areas:**
- Data visualization tools
- Template improvements
- Documentation enhancements
- Analysis scripts
- Website or app development

### 4. As a Researcher

Provide scientific input, methodology improvements, or analysis.

**How to Help:**
- Review and suggest methodology improvements
- Contribute to data analysis
- Provide literature reviews
- Suggest hypothesis refinements
- Help with statistical analysis

## 📝 How to Track Yawns

### Required Information

For each yawn, record:
- **Date & Time**: When the yawn occurred
- **Context**: What you were doing (e.g., "working at computer", "watching TV", "after waking")
- **Duration**: Approximate length (short/medium/long)
- **Environment**: Indoor/outdoor, temperature comfort level

### Daily Summary

At the end of each day, note:
- **Total yawns**: Count for the day
- **Sleep quality**: Poor/Fair/Good (self-reported)
- **Stress level**: Low/Medium/High (self-reported)
- **Physical activity**: Minutes of exercise
- **General health**: Any symptoms or changes

### Optional Wearable Data

If you use fitness trackers or health devices, you can optionally include:
- **Heart Rate Variability (HRV)**: Daily average
- **Resting Heart Rate**: Morning measurement
- **Steps/Activity**: Total daily count
- **Sleep metrics**: Deep sleep, REM sleep duration
- **Other biometrics**: As available from your device

## 🔐 Data Anonymization Guide

**CRITICAL**: Never submit personally identifiable information!

### Creating Your Anonymous ID

Generate a unique identifier:
```
Format: YI-[4-digit-year-of-birth]-[2-letter-initials]-[random-3-digits]
Example: YI-1990-JD-742
```

Or use a random generator: `YI-` followed by 8 random characters

### What NOT to Include

❌ Real name
❌ Exact birthdate (use year only or age range)
❌ Address or specific location
❌ Email address
❌ Phone number
❌ Exact GPS coordinates
❌ Photos with identifiable features
❌ Device serial numbers

### What TO Include

✅ Anonymous participant ID
✅ Age range (e.g., 18-25, 26-35, 36-45)
✅ General location (country or region only)
✅ Gender (optional)
✅ General health status categories
✅ Yawn tracking data
✅ Anonymized wearable data

## 📤 How to Submit Data

### Method 1: Via Pull Request (Recommended)

1. Fork this repository
2. Create a new file in `data/submissions/YYYY-MM/`
3. Name it: `[your-anonymous-id].csv` or `.json`
4. Ensure data is anonymized
5. Submit a pull request
6. Add label: "data-submission"

### Method 2: Via Issue

1. Go to Issues tab
2. Click "New Issue"
3. Select "Data Submission" template
4. Paste your anonymized data
5. Submit

### Method 3: Email (If Necessary)

If you cannot use GitHub:
- Contact maintainers via issue for submission instructions
- We'll help you submit your data

## 📋 Data Format

### CSV Format (Recommended)

```csv
participant_id,date,time,context,duration,environment,notes
YI-1990-JD-742,2025-01-15,09:30,morning coffee,medium,indoor-comfortable,first yawn of day
YI-1990-JD-742,2025-01-15,14:15,desk work,long,indoor-warm,felt tired
```

### JSON Format

```json
{
  "participant_id": "YI-1990-JD-742",
  "age_range": "30-35",
  "tracking_period": {
    "start_date": "2025-01-15",
    "end_date": "2025-01-22"
  },
  "yawns": [
    {
      "date": "2025-01-15",
      "time": "09:30",
      "context": "morning coffee",
      "duration": "medium",
      "environment": "indoor-comfortable"
    }
  ],
  "daily_summaries": [
    {
      "date": "2025-01-15",
      "total_yawns": 12,
      "sleep_quality": "good",
      "stress_level": "low"
    }
  ]
}
```

See `data/schemas/` for complete specifications.

## ✅ Quality Guidelines

### Good Data Practices

- **Be consistent**: Use the same format throughout
- **Be complete**: Don't leave required fields blank
- **Be honest**: Record actual observations
- **Be regular**: Try to track consistently each day
- **Be detailed**: Context helps identify patterns

### Common Mistakes to Avoid

- Forgetting to anonymize data
- Inconsistent time formats
- Missing context information
- Not tracking for sufficient duration
- Including identifying information

## 🎓 For Educators: Classroom Participation

### Guidelines for Group Submissions

1. **Student Privacy**: Each student should have their own anonymous ID
2. **Parental Consent**: Required for minors (template in `docs/consent-forms/`)
3. **Aggregate Data**: Consider submitting class averages instead of individual data
4. **Educational Focus**: Emphasize learning over data collection
5. **Age-Appropriate**: Adapt tracking complexity to student age

### Lesson Plan Ideas

- Graph and analyze class yawn patterns
- Discuss the scientific method
- Explore autonomic nervous system basics
- Create hypotheses about yawn triggers
- Practice data collection skills

## 🔬 For Researchers: Advanced Contributions

### Scientific Contributions

- Literature reviews on yawning and autonomic function
- Methodology improvements
- Statistical analysis plans
- Hypothesis refinement
- Protocol development

### Technical Standards

- Follow established research ethics
- Use appropriate statistical methods
- Document methodology clearly
- Peer review when possible
- Cite relevant literature

## 📊 Data Usage and Sharing

### How Your Data Will Be Used

- Aggregate analysis to identify patterns
- Educational demonstrations
- Open science publications
- Teaching materials
- Community insights

### Data Sharing Principles

- Only anonymized, aggregate data is shared publicly
- Individual records remain confidential
- No commercial use
- Attribution to "TAKFAT community contributors"
- Open access to all results

## 🛡️ Ethics and Safety

### Ethical Principles

1. **Voluntary Participation**: No one should feel pressured to contribute
2. **Informed Consent**: Understand what you're contributing to
3. **Right to Withdraw**: Can remove your data at any time
4. **No Harm**: Project should not cause distress or health concerns
5. **Transparency**: Methods and purposes are openly documented

### When NOT to Participate

⚠️ Skip participation if:
- You're uncomfortable with data sharing
- You have health concerns about self-monitoring
- You're experiencing significant health issues (consult doctor first)
- You feel pressured by others

### Medical Disclaimer

This is NOT medical research. Do not:
- Use findings for self-diagnosis
- Change medical treatments based on results
- Delay seeking medical care
- Share personal health information

## 💬 Questions and Support

### Need Help?

- 📖 Check our [documentation](docs/)
- ❓ Open an issue with "question" label
- 💡 Suggest improvements
- 🐛 Report problems

### Code of Conduct

- Be respectful and inclusive
- Welcome newcomers
- Focus on science and learning
- No harassment or discrimination
- Maintain privacy and confidentiality

## 🎉 Recognition

Contributors are recognized in:
- Acknowledgments in any publications
- Contributors list (anonymous IDs only)
- Community highlights
- Educational materials

Thank you for being part of this exploration into the science of yawning! Every yawn you track brings us closer to understanding the fascinating connection between this universal behavior and our autonomic health.

---

**Questions?** Open an issue or check our [FAQ](docs/FAQ.md)
