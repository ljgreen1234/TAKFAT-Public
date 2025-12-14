# Examples

This directory contains example data files to help you understand the data format and get started with your own tracking.

## Sample Data Files

### sample-week-tracking.csv
Complete example of yawn event tracking for one week. Shows:
- Individual yawn events with timestamps
- Different contexts and environments
- Various durations and conditions
- Including optional fields (temperature_comfort, lighting, contagious)

**Use this as a template** for detailed yawn-by-yawn tracking.

### sample-daily-summary.csv
Example of daily summary data for one week. Shows:
- Daily yawn totals
- Sleep quality and duration
- Stress and energy levels
- Physical activity tracking
- Caffeine intake patterns

**Use this as a template** for end-of-day summaries.

### sample-complete-submission.json
*(Coming soon)* Full example of a complete data submission in JSON format including:
- Participant profile
- Yawn events
- Daily summaries
- Optional wearable data

## Using These Examples

### For Learning
1. **Study the format**: See how data is structured
2. **Understand fields**: Learn what each column means
3. **See patterns**: Notice how yawning varies by context and time

### For Templates
1. **Copy the file**: Start with an example file
2. **Replace the data**: Put in your own observations
3. **Keep the structure**: Don't change column names or format
4. **Delete example rows**: Remove sample data before submitting

### For Testing
1. **Validate tools**: Use to test data analysis scripts
2. **Practice visualization**: Create charts from sample data
3. **Learn analysis**: Try statistical analyses on examples

## Data Characteristics in Examples

### Participant Profile
- **ID**: YI-1990-JD-742 (example anonymous ID)
- **Age range**: 30-35
- **Typical patterns**: Office worker, moderate yawning

### Patterns Shown
- **Morning peak**: Yawns upon waking
- **Post-lunch dip**: Increased afternoon yawning
- **Evening yawns**: Before bedtime
- **Context effects**: More yawns during desk work
- **Sleep relationship**: More yawns after poor sleep
- **Activity effects**: Fewer yawns on active days

### Realistic Features
- **Variable counts**: 4-10 yawns per day
- **Contagious yawning**: Some triggered by others
- **Environmental factors**: Temperature and lighting noted
- **Day-to-day variation**: Different patterns weekday vs weekend

## Data Quality Examples

### Good Practices Demonstrated
✅ Consistent format throughout
✅ Complete required fields
✅ Realistic value ranges
✅ Clear, brief notes
✅ Proper anonymization
✅ Varied contexts documented

### What NOT to Do
❌ Don't include real names or identifying info
❌ Don't use inconsistent date/time formats
❌ Don't leave required fields blank
❌ Don't record implausibly high counts (>50/day)

## Analysis Examples

*(To be added)*

Future additions will include:
- Example analysis scripts (Python, R)
- Visualization code
- Statistical analysis examples
- Interpretation guides

## Questions?

If you have questions about the examples:
- Check the [data schema documentation](../docs/data-schema.md)
- Review the [CONTRIBUTING guide](../CONTRIBUTING.md)
- Open an issue for clarification

## Contributing Examples

Have you created interesting visualizations or analyses?
Please share them!

1. Fork the repository
2. Add your example to this directory
3. Update this README
4. Submit a pull request

**Remember to anonymize any real data!**
