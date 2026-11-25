# PETAL breakout exercise

Prepare a short update for the Kalundborg municipal incident team. You have 40 minutes.

## Start here

Choose one reporter per group. The reporter shares their screen and works through the exercise with the group.

### Work locally with the ChatGPT desktop app (preferred)

1. [Download the exercise files as a ZIP](https://github.com/bakaburg1/petal-breakout-exercise/archive/refs/heads/main.zip) and extract the folder.
2. [Download ChatGPT for desktop](https://chatgpt.com/download/) if needed. In the app, select **Codex**, create a project, add the extracted folder as its source folder and choose **This computer**.
3. If R is missing, ask Codex to install it.

### Work online with GitHub Codespaces

1. [Open the exercise in GitHub Codespaces](https://codespaces.new/bakaburg1/petal-breakout-exercise), sign in to GitHub and select **Create codespace**.
2. If prompted, select **Trust Folder & Continue**. The guide opens in the browser editor.
3. Open **Copilot Chat** and sign in if prompted. R and ggplot2 are included.

## Chats

1. In your project, start a chat called **Facilitator** and paste the [facilitator prompt](facilitator-prompt.md). The facilitator introduces the tasks, gives hints if you get stuck and reviews your work before you move on.
2. Start a chat called **Work** in the same project.
3. After each task, tell **Facilitator** which task you finished and ask for a review. Ask for a hint whenever the group gets stuck. Do any subsequent work in the **Work** chat.

## Tasks

### 1. Create project instructions

Read [`background.md`](background.md), then write your own prompt in the **Work** chat asking the agent to create `AGENTS.md`. Review the file it creates.

#### Expected outcome

An `AGENTS.md` file at the project root that:

- Explains that the team is investigating an ongoing outbreak of gastrointestinal illness in Kalundborg and describes the team's current objectives.
- Tells the agent to read `background.md` at the start of every new chat and identifies [`incident-records/`](incident-records/) as the source records.
- Tells the agent to preserve original inputs, cite evidence, record assumptions and make analyses reproducible.

<details>
<summary>Practical hints for task 1</summary>

- Identify what the agent needs to know about the investigation whenever a new chat starts.
- Decide which standing instructions belong in `AGENTS.md` and which case details can stay in `background.md`.

</details>

### 2. Review the case

In the **Work** chat, ask what files are available. Use [`background.md`](background.md) for context and ask the agent to explain how the files in [`incident-records/`](incident-records/) fit the investigation.

#### Expected outcomes

- The group can explain what happened so far and how the available records fit together.
- The group can point to a record that supports one finding and identify one open question.

<details>
<summary>Practical hints for task 2</summary>

- Ask for an overview of the investigation and which records support it.
- Pick one event or decision, such as a change in the water advice. Find the record and check the event date against the report date.
- Identify one point the records leave unresolved and why it matters.

</details>

### 3. Analyse the cohort

Start by exploring [`cohort_line_list.csv`](cohort_line_list.csv) in the **Work** chat. Find out what a row represents, what the columns describe and how missing values are recorded. Then compare the risk of illness among respondents who drank tap water with those who did not.

#### Expected outcomes

- The analysis results, including cases, non-cases, denominators and attack rates by exposure, the risk ratio and the missing-exposure count.
- An R file containing the analyses the group ran.
- An epidemic curve made with ggplot2, stratified by relevant risk factors such as tap-water consumption.
- A manual review of the generated R code. Check how it selects cases, handles missing exposures and calculates at least one result.

<details>
<summary>Practical hints for task 3</summary>

- Find out which columns identify respondents, classify cases and describe tap-water consumption. Check how the agent handles unknown exposure.
- Check who contributes to each denominator and which group is the reference for the risk ratio.
- Check which field records symptom onset and how much detail it supports. Consider how to show cases with unknown exposure without assigning them to a known group.
- Recalculate one rate from its counts or reconcile the group totals and missing exposures with the number of rows.

</details>

### 4. Write the briefing

Use the incident records and your reviewed results to prepare a half-page update for the Kalundborg municipal incident team.

#### Expected outcomes

- A Word document named `briefing.docx` that includes the analysis results and the epidemic curve. State the main finding and who was compared, identify one uncertainty and propose one next action.
- The wording describes the association and links factual claims to their sources.
- The group can show one factual claim checked against the records and one figure checked against the results.

<details>
<summary>Practical hints for task 4</summary>

- Plan the briefing around the finding, the uncertainty and the next action.
- Check the numbers in the briefing against the R analysis output. Check that the embedded curve matches the plot produced by the analysis.
- Trace one factual claim to a dated record or section of the background. Choose a next action that would address the uncertainty you named.

</details>

## Report back

The reporter shows what the group produced and explains how the exercise went.
