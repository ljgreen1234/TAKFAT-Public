# Data Schema Documentation

## Overview

This document describes the data formats and structures used in the TAKFAT-Yawn-Index project. All data should follow these schemas to ensure consistency and enable effective analysis.

## Participant Information Schema

### Participant Profile

```json
{
  "participant_id": "string (required)",
  "age_range": "string (required)",
  "gender": "string (optional)",
  "region": "string (optional)",
  "health_status": "string (optional)",
  "long_covid": "boolean (optional)",
  "wearable_device": "string (optional)"
}
```

**Field Descriptions:**

- `participant_id`: Anonymous identifier (format: `YI-XXXX-XX-XXX` or similar)
- `age_range`: Age bracket (e.g., "18-25", "26-35", "36-45", "46-55", "56-65", "66+")
- `gender`: Optional (e.g., "male", "female", "non-binary", "prefer-not-to-say")
- `region`: General geographic region (e.g., "North America", "Europe", "Asia")
- `health_status`: General category (e.g., "healthy", "chronic-condition", "recovering")
- `long_covid`: Whether participant reports long COVID symptoms (true/false)
- `wearable_device`: Type of device if using (e.g., "fitbit", "apple-watch", "garmin", "none")

## Yawn Event Schema

### Individual Yawn Record

```json
{
  "event_id": "string (optional)",
  "participant_id": "string (required)",
  "timestamp": "ISO 8601 datetime (required)",
  "date": "YYYY-MM-DD (required)",
  "time": "HH:MM (required)",
  "duration": "string (required)",
  "context": "string (required)",
  "environment": "string (required)",
  "temperature_comfort": "string (optional)",
  "lighting": "string (optional)",
  "contagious": "boolean (optional)",
  "notes": "string (optional)"
}
```

**Field Descriptions:**

- `event_id`: Optional unique identifier for this yawn event
- `participant_id`: Links to participant profile
- `timestamp`: Full date and time in ISO 8601 format (e.g., "2025-01-15T09:30:00Z")
- `date`: Date in YYYY-MM-DD format
- `time`: Time in 24-hour HH:MM format
- `duration`: "short" (<3 seconds), "medium" (3-5 seconds), "long" (>5 seconds)
- `context`: Activity during yawn (see Context Values below)
- `environment`: "indoor" or "outdoor"
- `temperature_comfort`: "cold", "cool", "comfortable", "warm", "hot"
- `lighting`: "dark", "dim", "natural", "bright-artificial"
- `contagious`: Whether yawn was triggered by seeing someone else yawn
- `notes`: Additional observations (keep brief, avoid identifying info)

### Context Values

Standardized context categories:
- `waking-up`: Just after waking
- `morning-routine`: Morning activities
- `commuting`: Travel to work/school
- `desk-work`: Computer/office work
- `physical-activity`: Exercise or movement
- `eating`: During or after meals
- `meeting-call`: In meetings or on calls
- `studying`: Reading, learning, concentrating
- `watching-media`: TV, videos, movies
- `relaxing`: Leisure time
- `before-sleep`: Evening routine
- `other`: Specify in notes

## Daily Summary Schema

```json
{
  "participant_id": "string (required)",
  "date": "YYYY-MM-DD (required)",
  "total_yawns": "integer (required)",
  "sleep_hours": "number (optional)",
  "sleep_quality": "string (optional)",
  "stress_level": "string (optional)",
  "caffeine_intake": "string (optional)",
  "physical_activity_minutes": "integer (optional)",
  "screen_time_hours": "number (optional)",
  "general_energy": "string (optional)",
  "symptoms": "array of strings (optional)",
  "notes": "string (optional)"
}
```

**Field Descriptions:**

- `participant_id`: Links to participant profile
- `date`: Date for this summary
- `total_yawns`: Count of yawns recorded this day
- `sleep_hours`: Hours of sleep previous night (decimal allowed, e.g., 7.5)
- `sleep_quality`: "poor", "fair", "good", "excellent"
- `stress_level`: "low", "moderate", "high"
- `caffeine_intake`: "none", "low" (1 cup), "moderate" (2-3 cups), "high" (4+ cups)
- `physical_activity_minutes`: Total minutes of exercise/active movement
- `screen_time_hours`: Hours spent on screens (work + leisure)
- `general_energy`: "low", "moderate", "high"
- `symptoms`: Array of general symptoms (e.g., ["fatigue", "headache"])
- `notes`: Additional daily observations

## Wearable Data Schema

### Heart Rate Variability (HRV)

```json
{
  "participant_id": "string (required)",
  "date": "YYYY-MM-DD (required)",
  "hrv_rmssd": "number (optional)",
  "hrv_sdnn": "number (optional)",
  "resting_heart_rate": "integer (optional)",
  "average_heart_rate": "integer (optional)",
  "measurement_time": "string (optional)"
}
```

**Field Descriptions:**

- `hrv_rmssd`: Root mean square of successive differences (milliseconds)
- `hrv_sdnn`: Standard deviation of NN intervals (milliseconds)
- `resting_heart_rate`: RHR in beats per minute (bpm)
- `average_heart_rate`: Average HR during waking hours (bpm)
- `measurement_time`: "morning", "evening", "all-day"

### Activity/Gait Metrics

```json
{
  "participant_id": "string (required)",
  "date": "YYYY-MM-DD (required)",
  "total_steps": "integer (optional)",
  "distance_km": "number (optional)",
  "active_minutes": "integer (optional)",
  "walking_speed_avg": "number (optional)",
  "gait_symmetry": "number (optional)",
  "sedentary_hours": "number (optional)"
}
```

**Field Descriptions:**

- `total_steps`: Daily step count
- `distance_km`: Distance covered in kilometers
- `active_minutes`: Minutes of active movement
- `walking_speed_avg`: Average walking speed in km/h
- `gait_symmetry`: Gait balance measure (device-specific, 0-100)
- `sedentary_hours`: Hours of sedentary activity

### Sleep Metrics

```json
{
  "participant_id": "string (required)",
  "date": "YYYY-MM-DD (required)",
  "sleep_start": "HH:MM (optional)",
  "sleep_end": "HH:MM (optional)",
  "total_sleep_hours": "number (optional)",
  "deep_sleep_hours": "number (optional)",
  "rem_sleep_hours": "number (optional)",
  "light_sleep_hours": "number (optional)",
  "awake_time_hours": "number (optional)",
  "sleep_score": "integer (optional)"
}
```

## CSV Format Specifications

### Basic Yawn Tracking CSV

```csv
participant_id,date,time,duration,context,environment,notes
YI-1990-JD-742,2025-01-15,09:30,medium,morning-routine,indoor,first yawn of day
YI-1990-JD-742,2025-01-15,11:45,short,desk-work,indoor,during video call
YI-1990-JD-742,2025-01-15,14:20,long,desk-work,indoor,post-lunch
```

**Required Columns:**
- participant_id
- date
- time
- duration
- context
- environment

**Optional Columns:**
- temperature_comfort
- lighting
- contagious
- notes

### Daily Summary CSV

```csv
participant_id,date,total_yawns,sleep_hours,sleep_quality,stress_level,physical_activity_minutes
YI-1990-JD-742,2025-01-15,12,7.5,good,low,30
YI-1990-JD-742,2025-01-16,15,6.0,fair,moderate,0
YI-1990-JD-742,2025-01-17,8,8.5,excellent,low,45
```

### Combined Format CSV

For participants who want all data in one file:

```csv
type,participant_id,date,time,field1,field2,field3,field4,field5
yawn,YI-1990-JD-742,2025-01-15,09:30,medium,morning-routine,indoor,,
daily,YI-1990-JD-742,2025-01-15,,12,7.5,good,low,30
yawn,YI-1990-JD-742,2025-01-15,11:45,short,desk-work,indoor,,
```

## JSON Format Specifications

### Complete Submission Format

```json
{
  "submission_metadata": {
    "submission_date": "2025-01-22T10:00:00Z",
    "data_version": "1.0",
    "tracking_period": {
      "start_date": "2025-01-15",
      "end_date": "2025-01-22"
    }
  },
  "participant_profile": {
    "participant_id": "YI-1990-JD-742",
    "age_range": "30-35",
    "gender": "prefer-not-to-say",
    "region": "North America",
    "health_status": "healthy",
    "long_covid": false,
    "wearable_device": "fitbit"
  },
  "yawn_events": [
    {
      "timestamp": "2025-01-15T09:30:00",
      "duration": "medium",
      "context": "morning-routine",
      "environment": "indoor",
      "temperature_comfort": "comfortable",
      "notes": "first yawn after waking"
    }
  ],
  "daily_summaries": [
    {
      "date": "2025-01-15",
      "total_yawns": 12,
      "sleep_hours": 7.5,
      "sleep_quality": "good",
      "stress_level": "low",
      "physical_activity_minutes": 30,
      "general_energy": "high"
    }
  ],
  "wearable_data": {
    "hrv_measurements": [
      {
        "date": "2025-01-15",
        "hrv_rmssd": 45.2,
        "resting_heart_rate": 62,
        "measurement_time": "morning"
      }
    ],
    "activity_metrics": [
      {
        "date": "2025-01-15",
        "total_steps": 8543,
        "active_minutes": 35,
        "sedentary_hours": 9.5
      }
    ]
  }
}
```

## File Naming Conventions

### Individual Submissions

Format: `{participant_id}_{start_date}_{end_date}.{ext}`

Examples:
- `YI-1990-JD-742_2025-01-15_2025-01-22.csv`
- `YI-1990-JD-742_2025-01-15_2025-01-22.json`

### Monthly Aggregations

Format: `aggregate_{YYYY-MM}.{ext}`

Examples:
- `aggregate_2025-01.json`
- `aggregate_2025-01.csv`

## Data Validation Rules

### Required Validations

1. **Participant ID**: Must follow pattern `YI-[alphanumeric-with-hyphens]` (e.g., `YI-1990-JD-742`)
2. **Dates**: Must be valid dates in YYYY-MM-DD format
3. **Times**: Must be in 24-hour HH:MM format
4. **Duration**: Must be one of: "short", "medium", "long"
5. **Context**: Must be from standardized context list
6. **Environment**: Must be "indoor" or "outdoor"

### Recommended Validations

1. **Yawn Count**: Reasonable range (0-50 per day)
2. **Sleep Hours**: Reasonable range (0-14 hours)
3. **Activity Minutes**: Reasonable range (0-300 minutes)
4. **HRV Values**: Device-appropriate ranges

### Data Quality Flags

Mark data for review if:
- Extremely high yawn counts (>30/day)
- Missing required fields
- Inconsistent timestamps
- Suspicious patterns suggesting bot/fake data

## Version History

- **v1.0** (December 2025): Initial schema definition
- Future versions will be documented here with change logs

## Using This Schema

### For Participants

1. Choose CSV or JSON format
2. Use provided templates in `data/templates/`
3. Follow required field specifications
4. Submit via GitHub pull request

### For Developers

1. Validate submissions against schema
2. Use consistent field names in tools
3. Handle optional fields gracefully
4. Document any extensions

### For Researchers

1. All analysis should reference schema version
2. Document any transformations
3. Report data quality issues
4. Suggest improvements via issues

## Questions?

- See examples in `examples/` directory
- Check templates in `data/templates/`
- Open an issue for clarification
- Suggest improvements via pull request

---

**Schema Version**: 1.0
**Last Updated**: December 2025
