# PETAL breakout exercise in Codespaces

Prepare a short update for the Kalundborg municipal incident team. You have 40 minutes.

[Open in GitHub Codespaces](https://codespaces.new/bakaburg1/petal-breakout-exercise)

## Start here

In Codespaces, select **Open as Preview** in the README toolbar to follow this guide and expand the hints.

Choose one reporter per group. The reporter opens the Codespace in the browser, shares their screen and directs Copilot with the group. If VS Code opens in Restricted Mode, select **Trust Folder & Continue** for this exercise workspace. R is included. Open the terminal and run `Rscript --version` to check it. If Copilot asks you to sign in or activate access, use your own GitHub account.

1. Open Copilot Chat. Start a chat called **Facilitator** and paste the contents of [facilitator-prompt.md](facilitator-prompt.md).
2. Start a second chat called **Work** in the same workspace and paste this prompt:

   > Create a short AGENTS.md in the project root for our simulated Kalundborg outbreak investigation. Use background.md for context. Include instructions to preserve source files, cite evidence, record assumptions and make the analysis reproducible. Show me the file for review. Once I approve it, follow it in this chat for the rest of the exercise.

3. Keep all investigation work in **Work**. After each task, switch to **Facilitator**, name the task and ask for a review. For example, “I’ve finished ‘Review the evidence’. Please review it.” Make any required corrections in **Work** and request another review.

## Tasks

Save the files in your project folder. For each review, tell **Facilitator** the task name and share the saved file names. Paste a check or excerpt if the facilitator asks for it.

### 1. Review the evidence

Use **Work** to ask questions about the investigation in [`background.md`](background.md). Save a short evidence note.

#### Expected outcomes

- `evidence-note.md` contains one finding and a reference to the section or record that supports it.
- The note identifies one question that still matters for the investigation.

<details>
<summary>Practical hints for task 1</summary>

1. Pick one event or decision, such as the change in water advice. Ask **Work** “What did the team know when it made this decision? Give me the event date and the background section.”
2. Open the cited section yourself. Check whether it confirms the claim and whether the event date differs from the date it was reported.
3. Write your note under two short headings, **Finding** and **Open question**. Say why answering the question could change what the team does next.

</details>

### 2. Analyse the cohort

Use base R and [`cohort_line_list.csv`](cohort_line_list.csv) to compare the risk of illness among respondents who drank tap water with those who did not.

#### Expected outcomes

- `analysis.R` runs from the project folder with the supplied CSV and base R.
- `results.csv` shows cases, non-cases, denominators and attack rates for both known exposure groups. It reports the risk ratio for drinkers compared with non-drinkers and the number of respondents with missing exposure.
- The group can show one numerical check it performed.

<details>
<summary>Practical hints for task 2</summary>

1. Ask **Work** “Read the supplied CSV. Check the respondent IDs and exposure values before writing the analysis. Show me how you will handle blanks.” Use the [field definitions](#data-fields) below.
2. Build the counts for the two known exposure groups first. For each group, divide cases by cases plus non-cases. Divide the drinkers’ rate by the non-drinkers’ rate for the risk ratio. Count blank exposure separately.
3. Ask **Work** to run `Rscript analysis.R` from the project folder and show the run result. If the file cannot be found, check the working folder and the CSV name.
4. Try a manual check. Recalculate one rate from the table or add both group totals and the missing-exposure count and compare the sum with the CSV row count. Record what you checked in **Work**.

</details>

### 3. Write the briefing

Use your evidence note and reviewed results to prepare a half-page update for the municipal incident team.

#### Expected outcomes

- `briefing.md` states the main result and who was compared, identifies one uncertainty and proposes one next action.
- The wording describes the association and links factual claims to their sources.
- The group can show one factual claim checked against the background and one figure checked against the results table.

<details>
<summary>Practical hints for task 3</summary>

1. Ask **Work** to draft under three short headings, **Finding**, **Uncertainty** and **Next action**. Point it to your reviewed output files.
2. Read the result sentence beside the results table. Check the number, which group had the higher risk and which group is the reference.
3. Trace one sentence about the investigation to its cited section. Choose a next action that would address the uncertainty you named, and describe it as a proposal.

</details>

## Data fields

- `respondent_id` identifies one synthetic survey respondent.
- `case_status` is `1` for a case and `0` for a non-case.
- `tap_water` is `drank`, `did_not_drink` or blank if exposure is unknown.

## Report back

The reporter shows what the group produced and explains how the exercise went.

