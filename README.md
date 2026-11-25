# PETAL breakout exercise

Prepare a short update for the Kalundborg municipal incident team. You have 40 minutes.

## Start here

Choose one reporter per group. The reporter shares their screen and works through the exercise with the group.

### Work locally with the desktop app (preferred)

1. [Download the exercise files as a ZIP](https://github.com/bakaburg1/petal-breakout-exercise/archive/refs/heads/main.zip) and extract the folder.
2. [Download ChatGPT for desktop](https://chatgpt.com/download/) if needed. In the app, select **Codex**, open the extracted folder and choose **This computer**.
3. Make sure R is installed on your computer.

### Work online with GitHub Codespaces

1. [Open the exercise in GitHub Codespaces](https://codespaces.new/bakaburg1/petal-breakout-exercise), sign in to GitHub and select **Create codespace**.
2. If prompted, select **Trust Folder & Continue**. The guide opens in the browser editor.
3. Open **Copilot Chat** and sign in if prompted. R and ggplot2 are included.

## Chats

1. In your project, start a chat called **Facilitator** and paste the [facilitator prompt](facilitator-prompt.md). The facilitator introduces the tasks, gives hints if you get stuck and reviews your work before you move on.
2. Start a chat called **Work** in the same project. Use it to investigate the case, analyse the data and prepare the briefing. Paste the prompt below, then review the file it creates.

   > Create a short AGENTS.md in the project root for our simulated Kalundborg outbreak investigation. Use background.md for context. Include instructions to preserve source files, cite evidence, record assumptions and make the analysis reproducible. Show me the file for review. Once I approve it, follow it in this chat for the rest of the exercise.

3. After each task, tell **Facilitator** which task you finished and ask for a review. Ask for a hint whenever the group gets stuck. Make any corrections in **Work**.

## Tasks

### 1. Review the case

Ask **Work** what files are available and what each one contains. Have it explain the case using the incident records in [`background.md`](background.md). Be ready to explain what happened, point to a record that supports one finding and name an open question.

<details>
<summary>Practical hints for task 1</summary>

- Ask for an overview of the investigation and which records support it.
- Pick one event or decision, such as a change in the water advice. Find the record and check the event date against the report date.
- Identify one point the records leave unresolved and why it matters.

</details>

### 2. Analyse the cohort

Start by exploring [`cohort_line_list.csv`](cohort_line_list.csv) with **Work**. Find out what a row represents, what the columns describe and how missing values are recorded. Then compare the risk of illness among respondents who drank tap water with those who did not.

#### Expected outcomes

- A reproducible R analysis that the agent has run on the supplied data. Choose the functions and packages that suit your analysis.
- A Markdown file with cases, non-cases, denominators and attack rates for both known exposure groups, the risk ratio and the number of respondents with missing exposure. Present the results in the layout you prefer.
- A plot made with **ggplot2** that helps explain a result. Include it in the Markdown file.
- One numerical check you can explain to the group.

<details>
<summary>Practical hints for task 2</summary>

- Find out which columns identify respondents, classify cases and describe tap-water consumption. Check how the agent handles unknown exposure.
- Check who contributes to each denominator and which group is the reference for the risk ratio.
- Choose a comparison the plot can clarify. Check the labels and whether the plotted values agree with the results.
- Recalculate one rate from its counts or reconcile the group totals and missing exposures with the number of rows.

</details>

### 3. Write the briefing

Use the incident records and your reviewed results to prepare a half-page update for the Kalundborg municipal incident team.

#### Expected outcomes

- A Word document named `briefing.docx` that states the main finding and who was compared, identifies one uncertainty and proposes one next action.
- The wording describes the association and links factual claims to their sources.
- The group can show one factual claim checked against the records and one figure checked against the results.

<details>
<summary>Practical hints for task 3</summary>

- Plan the briefing around the finding, the uncertainty and the next action.
- Read the result sentence beside the Markdown results. Check the number, the direction of the comparison and the reference group.
- Trace one factual claim to a dated record or section of the background. Choose a next action that would address the uncertainty you named.

</details>

## Report back

The reporter shows what the group produced and explains how the exercise went.
