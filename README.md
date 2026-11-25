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
2. Start a separate **Setup** chat for Task 1. Ask **Facilitator** for help or a review of `AGENTS.md`.
3. After **Facilitator** approves `AGENTS.md`, start a new **Work** chat in the same project. Use this chat for Tasks 2–4 and ask **Facilitator** to review each task before moving on.

## Tasks

<!-- When changing a task title or expected outcome, update the matching section of facilitator-prompt.md in the same edit. -->

### 1. Create project instructions

In the **Setup** chat, write your own prompt asking the agent to create `AGENTS.md`. Refer to [`background.md`](background.md) in your prompt so the agent uses it for context and includes a reference to it in `AGENTS.md`. Review the file it creates.

#### Expected outcome

An `AGENTS.md` file at the project root that:

- Explains that the team is investigating an ongoing outbreak of gastrointestinal illness in Kalundborg and describes the team's current objectives.
- Tells the agent to read `background.md` at the start of every new chat.
- Describes the relevant contents of the repository, including the source records in [`incident-records/`](incident-records/) and the cohort data in [`cohort_line_list.csv`](cohort_line_list.csv).
- Tells the agent to preserve original inputs, cite evidence, record assumptions and make analyses reproducible.

<details>
<summary>Practical hints for task 1</summary>

- Identify what the agent needs to know about the investigation whenever a new chat starts.
- Decide which standing instructions belong in `AGENTS.md` and which case details can stay in `background.md`.
- Keep exercise logistics and references to `README.md` and `facilitator-prompt.md` out of `AGENTS.md`.

</details>

### 2. Review the case

In your new **Work** chat, ask what files are available. Use [`background.md`](background.md) for context and ask the agent to explain how the files in [`incident-records/`](incident-records/) fit the investigation.

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
- An epidemic curve made with ggplot2, stratified by relevant risk factors such as tap-water consumption.
- An R file with the code that runs the analyses and creates the epidemic curve.
- A manual review of the generated R code. Check how it selects cases, handles missing exposures and calculates at least one result.

<details>
<summary>Practical hints for task 3</summary>

- Tell the agent which outputs you want to see and which R file should hold the analysis and plotting code.
- Specify how you want the epidemic curve drawn, such as bars or lines and the time interval on the horizontal axis.
- Tell the agent which risk factor to use and how to distinguish groups, for example with colours or separate panels. Ask to see the plot and tell the agent what to adjust.

</details>

### 4. Write the briefing

Use the incident records and your reviewed results to prepare a half-page update for the Kalundborg municipal incident team.

#### Expected outcomes

- A Word document named `briefing.docx` that includes a summary of the analysis results and the epidemic curve. State the main finding and who was compared, identify one uncertainty and propose one next action.
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
