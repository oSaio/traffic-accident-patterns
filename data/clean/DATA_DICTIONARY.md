\# Data dictionary: accidents\_clean.csv



Source: UK Department for Transport, Road Safety Data (STATS19), year 2025. Licence: Open Government Licence v3.0.

Rows: 101,523 (one row per accident). Columns: 15. No missing values.



| Column | Meaning | Type | Values |

|--------|---------|------|--------|

| accident\_index | Unique accident ID (renamed from collision\_index) | text | unique |

| latitude | Latitude of the accident | decimal | inside Great Britain |

| longitude | Longitude of the accident | decimal | inside Great Britain |

| hour | Hour of the day | integer | 0 to 23 |

| weekday | Day of the week | text | Monday to Sunday |

| month | Month of the year | integer | 1 to 12 |

| speed\_limit | Speed limit at the location (mph) | integer | 20, 30, 40, 50, 60, 70 |

| road\_type | Type of road | text | Roundabout, One way street, Dual carriageway, Single carriageway, Slip road, One way street / Slip road, Unknown |

| light\_conditions | Light conditions | text | Daylight, Darkness - lights lit, Darkness - lights unlit, Darkness - no lighting, Darkness - lighting unknown, Unknown |

| weather\_conditions | Weather | text | Fine, Raining, Snowing, Fine + high winds, Raining + high winds, Snowing + high winds, Fog or mist, Other, Unknown |

| road\_surface\_conditions | Road surface | text | Dry, Wet or damp, Snow, Frost or ice, Flood, Unknown |

| urban\_or\_rural\_area | Urban or rural | text | Urban, Rural, Unallocated |

| number\_of\_vehicles | Vehicles in the accident | integer | 1 or more |

| number\_of\_casualties | Casualties in the accident | integer | 1 or more |

| accident\_severity | Severity (renamed from collision\_severity) | text | Fatal, Serious, Slight |



Notes:

\- Unknown means the code was -1 or 9 (missing or unknown) in the raw data.

\- For the Decision Tree, do not use number\_of\_casualties as a feature (data leakage).

\- Severe = Fatal + Serious.

\- Extra file accidents\_vehicle\_features.csv holds vehicle summaries per accident (optional).

\- cleaning\_log.csv lists every cleaning step and the rows removed.

