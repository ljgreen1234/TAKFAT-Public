# Frequently Asked Questions (FAQ)

## General Questions

### What is TAKFAT-Yawn-Index?

A citizen-science project exploring whether yawning patterns correlate with autonomic nervous system function. Participants track their yawns and share anonymized data to help identify patterns.

### Who can participate?

Anyone! Kids (with parental permission), teens, adults, and seniors. All ages and health statuses welcome.

### Do I need special equipment?

No! Just paper and pen, or a phone/computer to record data. Optional: fitness tracker for wearable data.

### How long does it take?

- **Daily**: 2-5 minutes tracking yawns
- **Total**: 7+ days minimum
- **Commitment**: About 1 hour total over a week

### Is this real science?

Yes! It's **citizen science** - research conducted with public participation. While informal, it follows scientific principles and contributes to exploratory research.

### Will this cure or diagnose anything?

**No.** This is exploratory research, not medical research. It cannot diagnose conditions or guide treatment.

## Privacy and Safety

### Is my data private?

All data is **anonymized and public**. You create an anonymous ID, and your data is shared in a public repository. See [PRIVACY.md](PRIVACY.md) for details.

### What information do you collect?

- Yawn timing and context (anonymous)
- Age range (not exact age)
- General health category (optional)
- Optional wearable data

### What don't you collect?

- Names, addresses, contact info
- Exact birthdates or ages
- Specific locations
- Photos or videos
- Medical records
- Any personally identifiable information

### Can I delete my data?

Yes! Open an issue requesting deletion, provide your anonymous ID, and we'll remove your data within 7 days.

### Is this approved by an ethics board?

This is informal citizen science, not formal medical research, so IRB approval isn't required. However, we follow ethical research principles.

## Participation Questions

### How do I start?

1. Read the [Quick Start Guide](QUICKSTART.md)
2. Download a template from `data/templates/`
3. Create an anonymous ID
4. Start tracking yawns for 7+ days
5. Submit your anonymized data

### What if I miss some yawns?

That's OK! Track as many as you can. Imperfect data is still valuable.

### What if I forget a whole day?

Just continue with the days you can track. 7 days minimum, but they don't have to be consecutive.

### Can I track for longer than 7 days?

Yes! More data is great. Track for weeks or months if you'd like.

### Do I have to track yawns exactly when they happen?

**Preferred**: Real-time tracking is most accurate
**Acceptable**: Recording at the end of each period (morning, afternoon, evening)
**OK**: Best estimate if you forget exact times

### What if I don't yawn very much?

Perfect! We need data from all types of yawners. Low frequency is interesting data too.

### What if I yawn a LOT?

Also great! High-frequency data is valuable. Track what actually happens.

### Can I participate if I have a health condition?

Yes! We welcome participants with various health statuses. Just note it in general categories (no specific diagnoses).

## Data Tracking Questions

### How do I create an anonymous ID?

**Format options:**
- `YI-[year]-[initials]-[random]` like `YI-1990-JD-742`
- `YI-[random characters]` like `YI-ABC123XYZ`

Just make it unique and remember it!

### What counts as a yawn?

A yawn is the reflex of:
- Opening mouth wide
- Deep breath in
- Brief pause
- Slow breath out

If it felt like a yawn, count it!

### How do I measure yawn duration?

**Simple estimates:**
- **Short**: Quick yawn, under 3 seconds
- **Medium**: Normal yawn, 3-5 seconds
- **Long**: Big, extended yawn, over 5 seconds

Don't overthink it - consistency matters more than precision.

### What are the standard contexts?

Use these categories:
- `waking-up` - Just after waking
- `morning-routine` - Morning activities
- `commuting` - Travel
- `desk-work` - Computer/office work
- `physical-activity` - Exercise
- `eating` - During meals
- `meeting-call` - Meetings or calls
- `studying` - Reading, learning
- `watching-media` - TV, videos
- `relaxing` - Leisure time
- `before-sleep` - Evening routine
- `other` - Anything else

### What if my context isn't listed?

Use `other` and add a brief note, or use the closest match.

### Do I need to track wearable data?

No! Wearable data (HRV, steps, etc.) is completely **optional**. Core tracking is just yawns.

### How do I get HRV data?

Most fitness trackers provide HRV:
- Fitbit
- Apple Watch
- Garmin
- Oura Ring
- Whoop
- Others

Check your device's app for HRV measurements.

### What if I don't have wearable data?

No problem! Yawn tracking alone is valuable. Wearable data is just a bonus.

## Technical Questions

### What format should I use?

**CSV (recommended)**: Simple spreadsheet format
**JSON**: For more complex data structures

Templates available in `data/templates/`

### Can I use Excel or Google Sheets?

Yes! Start with CSV templates, edit in your preferred spreadsheet program.

### How do I submit data?

**Option 1 (preferred)**: GitHub pull request
**Option 2**: Create a GitHub issue with data
**Option 3**: Request help via issue if you can't use GitHub

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed steps.

### I'm not familiar with GitHub. Can I still participate?

Yes! Open an issue explaining you need help submitting data. We'll guide you or provide alternative methods.

### What file naming should I use?

**Format**: `[your-ID]_[start-date]_[end-date].csv`
**Example**: `YI-1990-JD-742_2025-01-15_2025-01-22.csv`

### My CSV has errors. What should I do?

Check:
- Column names match template
- Dates in YYYY-MM-DD format
- Times in HH:MM format
- Required fields aren't blank
- Duration is short/medium/long
- Context matches standard categories

## Scientific Questions

### What is the autonomic nervous system?

The ANS controls automatic body functions like heart rate, breathing, and digestion. See [ANS Basics](guides/ans-basics.md) for details.

### Why study yawning?

Yawning may be connected to ANS function, arousal regulation, and thermoregulation. It's common, easy to track, and potentially informative.

### What is Heart Rate Variability (HRV)?

HRV measures variation in time between heartbeats. Higher HRV generally indicates better ANS balance and health. Many fitness trackers measure it.

### What is long COVID?

Long COVID (post-COVID conditions) refers to health problems that continue weeks or months after COVID-19 infection. Some people experience autonomic dysfunction.

### Could this help diagnose long COVID?

**No.** This is exploratory research only. If you have health concerns, consult a healthcare provider.

### What will you do with the data?

- Analyze patterns in yawning behavior
- Look for correlations with health status
- Explore circadian patterns
- Compare groups (e.g., long COVID vs. controls)
- Share findings with community
- Educational purposes

### Will this be published?

Results may be shared as:
- Blog posts or reports in this repository
- Open-access publications
- Educational materials
- Conference presentations

All data is already public in this repository.

### How is this different from medical research?

**Medical research**: Formal protocols, IRB approval, diagnostic/treatment goals
**Citizen science**: Exploratory, educational, community-driven, hypothesis-generating

This is the latter - exploratory and educational.

## For Educators

### Can I use this in my classroom?

Yes! See [For Educators](guides/for-educators.md) guide. It teaches scientific method, data collection, and biology.

### Do I need parental permission?

**Yes**, if students are under 18 and will submit data. Template provided in documentation.

### Can students work together?

Yes! Each student should have their own anonymous ID. You can submit class aggregate data too.

### What grade levels is this appropriate for?

- **Elementary (8-11)**: Simplified tracking
- **Middle School (12-14)**: Standard protocol
- **High School (15-18)**: Full protocol with analysis

Adapt complexity to student level.

### How long should the unit be?

- **Minimum**: 1-2 weeks (intro + tracking)
- **Recommended**: 2-3 weeks (includes analysis)
- **Extended**: Ongoing project over semester

## For Researchers

### Can I use this data for research?

Yes! All data is public and available. Please cite the project and share findings back to the community.

### What are the data quality limitations?

- Self-reported (not objective measurement)
- Volunteer sample (selection bias)
- Variable compliance
- No standardized validation

See [Methodology](methodology.md) for full discussion.

### Can I collaborate on analysis?

Absolutely! Open an issue to discuss, or submit analyses via pull request.

### Where is the dataset?

In this repository under `data/submissions/` (as data is submitted).

### What license is the data under?

MIT License (same as repository). Data is openly available for research and educational use.

## Troubleshooting

### The tracking seems hard to remember

**Solutions:**
- Set phone reminders every few hours
- Keep tracking sheet visible
- Use a partner/buddy system
- Simplify to just tallying counts

### I'm yawning more because I'm tracking!

That's normal! Just being aware of yawning can trigger more yawns. Track what actually happens - it's still valid data.

### My patterns don't seem interesting

All patterns are interesting! Even "boring" data contributes to understanding normal variation.

### I made a mistake in my data

If you haven't submitted yet, just fix it. If already submitted, open an issue with correction details.

### How do I update already-submitted data?

Open an issue explaining what needs to be updated, reference your participant ID, and provide corrected data.

## About the Project

### Who created this project?

This is an open community project. See repository contributors and maintainers.

### Is this affiliated with a university?

Not currently. It's an independent citizen-science initiative.

### How is this funded?

It's not! This is a volunteer project with no funding requirements.

### Can I contribute besides data?

Yes! Contribute:
- Documentation improvements
- Analysis code
- Visualizations
- Educational materials
- Translation
- Spreading the word

### How can I stay updated?

- Watch the GitHub repository
- Check for updates in README
- Follow discussion in issues

### Can I suggest improvements?

Please do! Open an issue with suggestions.

## Still Have Questions?

### Not answered here?

1. **Check documentation**:
   - [README](../README.md)
   - [CONTRIBUTING](../CONTRIBUTING.md)
   - [Methodology](methodology.md)

2. **Search existing issues**: Someone may have asked already

3. **Open a new issue**: 
   - Use "question" label
   - Provide details
   - We'll respond publicly to help others too

4. **Review guides**:
   - [Quick Start](QUICKSTART.md)
   - [For Kids](guides/for-kids.md)
   - [For Educators](guides/for-educators.md)
   - [For Researchers](guides/for-researchers.md)

---

**This FAQ is updated regularly based on community questions. If your question isn't here, please ask - it helps everyone!**
