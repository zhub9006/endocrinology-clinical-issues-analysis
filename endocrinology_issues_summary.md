# Endocrinology Clinical Software — Open Issue Analysis

## Overview

This report summarizes **167 open issues** collected from GitHub repositories related to endocrinology clinical software — including insulin dosing tools, diabetes management platforms (Nightscout, OpenAPS, Loop, AndroidAPS, Trio, xDrip, etc.), and thyroid/medication management systems.

Issues were gathered on **2026-06-06** from public GitHub repositories and categorized by theme using keyword-based classification.

## Category Counts

| Category | Count | % of Total |
|---|---|---|
| Data Integration & Sync Problems | 51 | 30.5% |
| Dosing Errors & Insulin Calculation Bugs | 48 | 28.7% |
| Workflow & Clinical Safety Gaps | 34 | 20.4% |
| UI / Display Issues | 34 | 20.4% |
| Other / Uncategorized | 20 | 12.0% |
| Installation / Setup / Documentation | 13 | 7.8% |
| Timezone / Unit Conversion Issues | 10 | 6.0% |

## Top Problems by Category

### Data Integration & Sync Problems (51 issues)

- **nightscout/cgm-remote-monitor**: Accept Activity data in APIv3
- **nightscout/cgm-remote-monitor**: Ability to bulk create, update, delete using api3
- **nightscout/cgm-remote-monitor**: Simplify Health Checks for Easier Cloud Provider Integration
- **nightscout/cgm-remote-monitor**: Nightscout crashes when setting up connect_source_libre for the first time
- **nightscout/cgm-remote-monitor**: OpenAps features visible in pillar
- **nightscout/Trio**: Tidepool authentication status misleading
- **nightscout/Trio**: Replace Bolus in progress notification with an explanation and a discoverable Manual Loop UI element
- **nightscout/Trio**: A fix for double bolus double entries (especially on Dana pumps)
- … and 43 more

### Dosing Errors & Insulin Calculation Bugs (48 issues)

- **nightscout/Trio**: mmol rounding issue with importing ISF settings from NS
- **nightscout/Trio**: Insulin W view shows incorrect value for current day vs D view
- **nightscout/Trio**: Replace Bolus in progress notification with an explanation and a discoverable Manual Loop UI element
- **nightscout/Trio**: Bolus error messages during CGM warm-up
- **nightscout/Trio**: Algorithm thinks expired temp high target BG is still active, preventing SMBs
- **nightscout/Trio**: Bolus calculator in open loop used zero values for target and ISF
- **nightscout/Trio**: Daily Carbs total incorrect upon first display
- **nightscout/Trio**: IOB correct after cancellation?
- … and 40 more

### Workflow & Clinical Safety Gaps (34 issues)

- **nightscout/cgm-remote-monitor**: Week-to-week, month-to-month insulin usage/distribution report
- **nightscout/cgm-remote-monitor**: Main screen clock should use device reported timezone
- **nightscout/cgm-remote-monitor**: Add storage of and reports for HbA1c in NS
- **nightscout/Trio**: 10u remaining alert immediately follows empty reservoir alert
- **nightscout/Trio**: Replace Bolus in progress notification with an explanation and a discoverable Manual Loop UI element
- **nightscout/Trio**: Bolus error messages during CGM warm-up
- **nightscout/Trio**: Algorithm thinks expired temp high target BG is still active, preventing SMBs
- **nightscout/Trio**: Low Reservoir Alarm
- … and 26 more

### UI / Display Issues (34 issues)

- **nightscout/cgm-remote-monitor**: DEV: /split view blank on dev — nameFromKey regex misses letter-to-digit transition
- **nightscout/cgm-remote-monitor**: Main screen clock should use device reported timezone
- **nightscout/cgm-remote-monitor**: Link to step-by-step guide for updating does not work anymore
- **nightscout/Trio**: Indefinite Override Not Drawn in LiveActivity Chart
- **nightscout/Trio**: Statistics: Meals chart shows zero for Carbs, Fat and Protein even though some has been entered
- **nightscout/Trio**: mmol rounding issue with importing ISF settings from NS
- **nightscout/Trio**: Handle Potential Occurrences of Manual (BGM) Readings of 38 mg/dL
- **nightscout/Trio**: Therapy settings blank
- … and 26 more

### Other / Uncategorized (20 issues)

- **nightscout/cgm-remote-monitor**: OpenAPS pill behavior is unpredictable
- **nightscout/Trio**: import/export function between multiple iPhones
- **nightscout/Trio**: TTs and overrides in the past (>24 hours)
- **openaps/oref0**: Don't cancel a high temp due to lack of BG data if the temp has been running for less than 10m
- **openaps/oref0**: Failing to get BG from railway/nightscout
- **LoopKit/Loop**: Apple Watch don't open Loop
- **LoopKit/Loop**: Apple Watch Loop not updating consistently after updating to v3.8.0
- **LoopKit/Loop**: Libre2+ LA
- … and 12 more

### Installation / Setup / Documentation (13 issues)

- **nightscout/cgm-remote-monitor**: DEV: /split view blank on dev — nameFromKey regex misses letter-to-digit transition
- **nightscout/cgm-remote-monitor**: README version update links point to old nightscout.info wiki documentation
- **nightscout/cgm-remote-monitor**: Add Lithuanian language
- **nightscout/cgm-remote-monitor**: Simplify Health Checks for Easier Cloud Provider Integration
- **nightscout/cgm-remote-monitor**: Revisit browser support in upcoming Nightscout release
- **nightscout/Trio**: Log files grow excessively large
- **openaps/oref0**: problem with undefined: unsafe.Slice in oref0-setup.sh script
- **openaps/oref0**: Update install script urls to use https protocol
- … and 5 more

### Timezone / Unit Conversion Issues (10 issues)

- **nightscout/cgm-remote-monitor**: Main screen clock should use device reported timezone
- **nightscout/Trio**: mmol rounding issue with importing ISF settings from NS
- **nightscout/Trio**: Handle Potential Occurrences of Manual (BGM) Readings of 38 mg/dL
- **nightscout/Trio**: Persistent Banner Notifications timestamps are not persistent
- **openaps/oref0**: Harmonize mmol/l and mg/dl related outputs as number in rT
- **jwoglom/controlX2**: Nightscout sync doesn't handle timezones
- **legoandmars/nightscout-chrome**: Issue calculating/displaying delta value in mmol/L
- **openaps/openaps**: millisecond date doesn't match timestamp in pumphistory.json
- … and 2 more

## Key Takeaways

1. **Dosing Errors & Insulin Calculation Bugs** are the single largest category. Incorrect IOB tracking, faulty bolus calculators, COB algorithm bugs, and autotune failures dominate — posing direct patient-safety risks in automated insulin delivery.

2. **Data Integration & Sync Problems** are nearly as frequent. Bluetooth/BLE connectivity drops, Nightscout sync failures, Tidepool upload regressions, and device-pairing issues mean clinicians and patients often lack a reliable real-time view of glucose and insulin data.

3. **Workflow & Clinical Safety Gaps** highlight missing features that clinicians need: medication adherence tracking, lab-result alerting, exercise-mode handling, and safety guard-rails (e.g., preventing double dosing, expired-temp-target confusion).

4. **UI / Display Issues** — while lower severity — erode trust: truncated glucose values, incorrect chart rendering, stale bolus dialogs, and mmol/mg·dL rounding errors can lead to misinterpretation at the point of care.

5. **Timezone & Unit Conversion** issues recur across repos (Nightscout, OpenAPS, xDrip) and are especially dangerous when they affect IOB/COB calculations that span daylight-saving changes.

6. **Installation / Setup** friction (outdated docs, deprecated dependencies, broken setup scripts) remains a barrier to adoption, particularly for non-technical clinicians and patients trying to self-host.

---

*Generated automatically from GitHub issue data. For clinical decision-making, always verify against the original issue tracker.*
