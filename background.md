# Kalundborg outbreak investigation

The local epidemiology team is investigating an outbreak of gastrointestinal illness in Kalundborg, Denmark. The municipality leads the response, with support from Statens Serum Institut (SSI) from 17 December 2025. The team aims to establish what happened and when, assess whether tap water was a source of illness and brief the municipal incident team.

The [incident records](incident-records/) contain the initial community reports, clinical alert, municipal briefing and water utility reply. This background summarises the investigation through the start of the survey analysis. Use the dated records for evidence and the section IDs below for context.

## B1. 13 December | First reports

- **09:10.** The manager of day-care centre **DC-01** reports that several children have gastrointestinal symptoms. The manager has no case count or onset dates to share. Local public health plans to call back for the number of children affected, their onset dates and the number attending.
- **10:25.** A resident of apartment building **APT-01** reports gastrointestinal illness among residents to the water utility. The ticket gives no count or onset dates. Customer service refers the report to network operations.

Sources: Public health duty log **PH-1213-01** and water utility service ticket **WU-1213-04**.

## B2. 14–15 December | Clinical alert and initial response

- On 15 December, the out-of-hours clinician reports **17 patients** with gastrointestinal illness from the same area across 14 and 15 December. Reported symptoms include watery diarrhoea. Nine patients had vomiting and eight had fever. Most recovered in less than two days.
- The clinician describes the number as higher than usual. The alert gives no comparable baseline, individual onset dates or means of checking overlap with either community report.
- On 15 December, the municipality receives a preliminary report of elevated *E. coli* and coliform counts in water samples from APT-01. A boil-water notice goes out. Day-care facilities and restaurants in the affected area close as a precaution.
- On 16 December, the municipality advises residents in the affected area to stop using tap water and arranges an alternative supply.

Sources: Clinical alert, 15 December at 12:20. Municipal incident briefing, 17 December at 08:40.

## B3. 17 December | Utility records and coordination

The utility reports several pressure drops during pipe replacement on the night of **11–12 December**. The reply, sent on **17 December**, identifies a main supplying the affected area. At the time of the reply, the utility has yet to confirm from its network drawing whether DC-01 and APT-01 were served by the same section of main.

The municipality continues to coordinate the response and brings in SSI to support the investigation.

Sources: Utility operations reply, 17 December at 09:15.

## B4. 17–19 December | Environmental investigation

The water laboratory reports results by sampling point and collection date. For example, it reports **1 cfu/100 mL of E. coli** at point B in a sample collected on 14 December and **2 cfu/100 mL** at point D in a sample collected on 15 December. The lab reports **less than 1 cfu/100 mL** at point F. These are indicator measurements at specific points. Determining what each site received still requires the network information.

On 19 December, investigators receive the inspection findings. The utility found a leaking sewer above the affected water main near the pipe works. Repairs followed that day. The location and timing support the working hypothesis that contaminated tap water contributed to the illness cluster.

Sources: Laboratory records **WQ-KAL-251217-B**, **WQ-KAL-251217-D** and **WQ-KAL-251217-F**.

## B5. 20 December | Clinical laboratory findings

SSI reports norovirus genogroup II in **16 of 17** specimens from symptomatic residents. The findings support norovirus as the likely cause of illness. The specimens came from symptomatic people. Whether drinking tap water increased the risk of illness remains a separate question for the survey analysis.

## B6. 20 December onward | Case finding and household survey

The team defines a case as a resident of the affected area who developed diarrhoea, vomiting, abdominal pain or nausea from **10 December through the end of the month**. Any one of the four symptoms qualifies.

Investigators distribute questionnaires door to door to **368 households** in the affected area. The survey asks about symptoms and onset, residence, respondent characteristics, tap-water consumption and travel. The team needs responses from people who became ill and people who stayed well to compare risks.

## B7. At the start of the analysis

The municipal team has the household survey extract. Drinking tap water is the exposure under study. The affected supply area defines the population from which the survey respondents came. Each row of `cohort_line_list.csv` represents one respondent. The `case_status` field gives the case classification and `tap_water` records reported consumption where known.

The team wants to assess the association between reported tap-water consumption and illness. The survey and the incident records answer different questions. Later onsets could also reflect secondary transmission or other exposures, which the group should consider when interpreting the comparison.

