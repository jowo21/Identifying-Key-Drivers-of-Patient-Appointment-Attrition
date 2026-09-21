# Identifying-Key-Drivers-of-Patient-Appointment-Attrition

## Problem Statement

Healthcare organizations lose valuable clinical capacity when patients fail to attend scheduled appointments without prior cancellation. High appointment no-show rates can lead to **unused provider time, longer patient wait times, reduced access to care, and inefficient resource utilization**.

The Clinic Operations Manager of a group of local clinics has requested to analyze historical patient appointment data to identify the **key factors associated with appointment no-shows** and determine which patient groups, neighborhoods, scheduling patterns, and communication methods have the highest risk of missing appointments.  The manager also wants to find key metrics and solutions for the Patient Scheduling Manager and the Patient Care Coordination Team to work towards a system wide approach.



## Project Objective and North Star Metrics

### The primary objective is to:

> **Identify the factors driving patient appointment no-shows and develop data-driven recommendations to improve attendance and healthcare resource utilization.**
> 

### Secondary objectives:

1. Establish a baseline appointment no-show rate.
2. Identify high-risk patient and appointment segments.
3. Evaluate the effectiveness of SMS reminders.
4. Analyze the impact of appointment lead time.
5. Identify neighborhoods with unusually high or low attendance rates.
6. Examine attendance patterns by day of week.
7. Understand whether patient health and socioeconomic characteristics are associated with attendance.
8. Provide recommendations for improving appointment scheduling and reminder strategies.

## Executive Summary

This analysis covers over 110,000 individual patient appointment encounters to determine the major factors that contribute to high patient No-Show rates.

### **Key Contributing factors**

- The base No-Show rate is 20.2% which is mostly determined by the Lead Time between the patient’s scheduling of their appointment and the actual appointment day.  This can be used to establish a measurable starting point for future operational improvement initiatives.
- No-show rates vary by neighborhood and shows as a useful operational indicator, with the highest reported rate at Santos Dumont (28.9%). Location-level patterns may help identify where access barriers, scheduling practices, or transportation challenges warrant further investigation.
- Appointments recorded as receiving an SMS reminder had a 27.6% no-show rate, compared with 16.7% among appointments without a recorded SMS reminder. This unexpected direction means reminder effectiveness cannot be established from the current comparison alone.
- However, various demographic metrics had little to no impact on No-Show rates.  Demographics such as: Age, Sex, various diagnoses, and number of disabilities a patient has.  These findings support targeted investigation rather than broad demographic assumptions.

 

### Initial Recommendation:

I have created the following dashboard for the Clinical Operations Manager to monitor various high-risk patient criteria.  This will allow to filter the variables that contribute the most to missed appointments and allows for rescheduling and redirection of resources as appropriate:
<img width="1402" height="862" alt="image" src="https://github.com/user-attachments/assets/2c512bb7-ccdc-40b1-a6eb-faba68f3659c" />

## Additional Insights

### Insight 1: Appointment lead time is a key opportunity for intervention

Priority: Highest

As the largest determining factor of No-Show rate, the Lead Time (time between the day the appointment was scheduled and the actual appointment date) gives us our clearest picture of a massive 18% increase in rates  between same day appointments and a 1 to 3 day Lead Time range.
<img width="733" height="1121" alt="image" src="https://github.com/user-attachments/assets/0672f467-d5a2-4cae-a6d7-2ef23b1c7eb4" />
### Why this matters operationally

- Longer intervals between booking and appointment dates may create more opportunities for patients' schedules, transportation arrangements, or other circumstances to change.
- Appointments booked further in advance may benefit from earlier confirmation and additional opportunities to reschedule.
- Short-notice appointments may have different attendance patterns and should be evaluated separately from appointments booked in advance.
- Scheduling teams may be able to reduce avoidable missed appointments by improving how they manage appointments as the appointment date approaches.

### Insight 2: SMS reminders require a deeper effectiveness analysis

Priority: High

The metric that had the second highest variance on the No-Show Rate was if the patient received an SMS reminder of their appointment or not with a 10% difference.

| SMS Received | Total Appointments | No-Show Rate |
| --- | --- | --- |
| No | 75045 | 16.7% |
| Yes | 35482 | 27.6% |

This is an important finding, but it does not establish that SMS reminders increase no-shows or that reminders are ineffective.

One possible explanation is that reminders are preferentially sent to patients or appointments already considered higher risk. Other possibilities include differences in lead time, appointment type, patient contact information, or the timing and delivery of messages.

There is also an important distinction between a reminder being sent, successfully delivered, and actually read by a patient.

### Insight 3: Neighborhood differences may reveal access barriers

Priority: High — investigate locally

The highest reported neighborhood no-show rates range from 22.3% to 28.9%, with Santos Dumont recording the highest rate among the listed neighborhoods.

Top 15 Neighborhoods by No-Show Rate

| Neighborhood | Appointment Count | No-Show rate | Risk Rank |
| --- | --- | --- | --- |
| Santos Dumont | 1276 | 28.9% | 1 |
| Santa Ceci’lia | 448 | 27.5% | 2 |
| Santa Clara | 506 | 26.5% | 3 |
| Itarare’ | 3514 | 26.3% | 4 |
| Jesus De Nazareth | 2853 | 24.4% | 5 |
| Horto | 175 | 24% | 6 |
| Ilha Do Pri’ncipe | 2266 | 23.5% | 7 |
| Caratoi’ra | 2565 | 23.0% | 8 |
| Andorinhas | 2262 | 23.0% | 9 |
| Praia Do Sua’ | 1288 | 22.8% | 10 |
| Gurigica | 2018 | 22.6% | 11 |
| Bento Ferreira | 858 | 22.5% | 12 |
| Parque Moscoso | 802 | 22.3% | 13 |
| Marui’pe | 1902 | 22.3% | 14 |
| Do Moscoso | 413 | 22.3% | 15 |

Neighborhood patterns can help the clinic identify locations where patients may be experiencing transportation difficulties, inconvenient appointment times, communication barriers, or other obstacles.

However, neighborhood should be treated as a signal for further investigation, not as a direct explanation for why a patient misses an appointment. A clinic location's no-show rate may also reflect its appointment mix, patient population, provider availability, or scheduling processes.


### Insight 4: Day of week has limited overall variation

Priority: Moderate

The analysis reports relatively little variation in no-show rates across appointment weekdays.

This suggests that day of week may be useful as a secondary scheduling variable, but it is unlikely to be the primary lever for reducing missed appointments across the entire clinic.

The proposal to move higher-risk appointments away from weekends should therefore be treated as a hypothesis to test, rather than an established intervention.
<img width="633" height="281" alt="image" src="https://github.com/user-attachments/assets/a16ef76e-698f-40fc-8693-153c87d29379" />

### Insight 4: Clinical and demographic variables have limited standalone predictive value

Priority: low to none

There was a bit more variance with patients that have higher numbers of disabilities versus those that have fewer.

| Number of Disabilities | Appointment Count | No-Show Rate |
| --- | --- | --- |
| 0 | 108286 | 20.2% |
| 1 | 2042 | 17.9% |
| 2 | 183 | 20.2% |
| 3 | 13 | 23.1% |
| 4 | 3 | 33.3% |

**Other Demographic Factors**

All demographics were analyzed to determine which had impact on No-show rates:

Age

| Age Bracket | Total Appointments | No-Show Rate |
| --- | --- | --- |
| Child (1 -12) | 21036 | 20.5% |
| Teen (13-19) | 9375 | 26% |
| Young Adult  (20-39) | 28870 | 23.1% |
| Adult (40-59) | 30072 | 18.8% |
| Senior (60+) | 21174 | 15.3% |

Gender

| Gender | Total Appointments | No-Show Rate |
| --- | --- | --- |
| Female | 71840 | 20.3% |
| Male | 28687 | 20.0% |

Disease States

| Hypertension | Total Appointments | No-Show Rate |
| --- | --- | --- |
| No | 88726 | 20.9% |
| Yes | 21801 | 17.3% |

| Diabetes | Total Appointments | No-Show Rate |
| --- | --- | --- |
| No | 102584 | 20.4% |
| Yes | 7943 | 18.0% |

| Alcoholism | Total Appointments | No-Show Rate |
| --- | --- | --- |
| No | 107167 | 20.2% |
| Yes | 3360 | 20.2% |


## Recommendations

### 1. Clinic Operations Manager

Establish a framework that converts the analysis into measurable improvements in attendance, capacity utilization, and patient access.

Recommended actions

**A. Establish a no-show performance monitoring system**

- Monitor no-show rates by clinic, neighborhood, appointment lead time, weekday, and appointment type.
- Track the absolute number of missed appointments alongside rates so that high-volume locations receive appropriate attention.
- Establish monthly performance reviews and investigate locations with persistent increases.

**B. Develop a targeted capacity management strategy**

- Identify appointment categories and locations with consistently elevated no-show rates.
- Develop a cancellation and waitlist process that allows available slots to be offered to patients who can attend sooner.

**C. Launch a cross-functional improvement initiative**

- Coordinate scheduling, care coordination, clinic managers, and analytics teams.
- Review progress monthly and adjust interventions based on measured outcomes.

Intended outcome: Reduced avoidable missed appointments, improved provider capacity utilization, more consistent clinic performance, and better access to care.

### 2. Patient Scheduling Manager

Use scheduling data to reduce avoidable appointment gaps, improve confirmation processes, and give patients greater flexibility in choosing appointment times.

Recommended actions

**A. Introduce lead-time-based scheduling workflows**

- Evaluate no-show rates for each category by clinic and appointment type.
- Prioritize earlier confirmation for appointments booked further in advance.
- Offer earlier openings to patients who prefer shorter lead times and are clinically appropriate for earlier scheduling.

**B. Improve appointment confirmation and rescheduling**

- Provide patients with clear appointment details and a straightforward way to confirm, cancel, or reschedule.
- Identify unconfirmed appointments before the appointment date.

**C. Evaluate SMS reminders**

- Validate the current reminder workflow and whether SMS is sent selectively to higher-risk appointments.
- Maintain alternative communication methods for patients who cannot or do not wish to receive SMS.

**D. Use location and weekday information appropriately**

- Offer alternative clinic locations when they are convenient and clinically suitable for the patient.
- Evaluate whether particular appointment times or clinic schedules create avoidable attendance barriers.
- Avoid moving patients to different days or locations without considering their preferences and access needs.

Intended outcome: More reliable appointment attendance, fewer unfilled appointment slots, more efficient scheduling operations, and improved patient flexibility.

### 3. Patient Outreach / Care Coordination Team

Use appointment information to identify patients who may benefit from additional support, while ensuring outreach is respectful, accessible, and responsive to individual needs.

Recommended actions

**A. Develop proactive patient outreach workflows**

- Prioritize outreach to patients whose appointments are approaching and remain unconfirmed.
- Offer assistance with rescheduling when patients indicate they cannot attend.
- Establish clear escalation procedures for appointments requiring additional coordination.

**B. Investigate transportation and access barriers**

- Ask patients whether transportation, appointment timing, location, or other logistical challenges affect attendance.
- Connect patients with available transportation assistance or other support programs when appropriate.
- Collaborate with clinic operations to identify recurring barriers affecting specific locations.

**C. Tailor communication to patient needs**

- Respect preferred communication channels and language preferences.
- Provide accessible appointment instructions and clear cancellation or rescheduling options.
- For pediatric appointments, coordinate with caregivers as appropriate.
- Avoid assuming that age, diagnosis, disability status, or neighborhood determines an individual's ability to attend.

**D. Close the loop after missed appointments**

- Follow up with patients after missed appointments to understand the circumstances.
- Support timely rescheduling, particularly where continuity of care is important.
- Distinguish patient-initiated cancellations from unexplained missed appointments.
- Share aggregated barrier information with scheduling and operations teams.

Intended outcome: Improved patient engagement, fewer preventable missed appointments, better continuity of care, and more responsive support for patients facing barriers.

To help these various stakeholders start the recommended improvement processes, I created the following dashboard that allows them to track the various metrics that contribute to No-show rates and allows them to filter these findings by Patient’s Risk Tier.

<img width="1402" height="862" alt="image" src="https://github.com/user-attachments/assets/d8f99b3f-e171-4866-adc3-79db06a2cf04" />

## Final Takeaway

This analysis establishes a meaningful opportunity to improve appointment attendance and clinical capacity management. The most actionable starting point is to strengthen scheduling and confirmation workflows, investigate differences in appointment lead time, and develop a more evidence-based reminder strategy.

Neighborhood and age patterns can help direct further investigation, while the limited differences across several demographic and clinical variables suggest that the clinic should avoid relying on broad patient characteristics as the primary basis for intervention.

A coordinated approach, led by Clinic Operations, implemented through Patient Scheduling, and supported by Patient Care Coordination, can turn the dashboard from a descriptive reporting tool into a practical system for improving attendance, recovering appointment capacity, and reducing barriers to care.

The ultimate measure of success is not merely a lower no-show rate. It is a healthcare system in which more patients receive timely care, available clinical resources are used effectively, and patients have the support and flexibility they need to attend their appointments.

## About the Dataset

Original Source of the dataset can be found [here](https://www.kaggle.com/datasets/joniarroba/noshowappointments/data)

Data Cleaning Steps and Complete Exploratory Data Analysis can be found here
