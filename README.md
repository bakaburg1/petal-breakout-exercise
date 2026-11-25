# PETAL breakout exercise in Codespaces

[Open in GitHub Codespaces](https://codespaces.new/bakaburg1/petal-breakout-exercise)

Choose one reporter per group. The reporter opens the Codespace in the browser, shares their screen and directs Copilot with the group. If VS Code opens in Restricted Mode, select **Trust Folder & Continue** for this exercise workspace. R is included. Open the terminal and run `Rscript --version` to check it. If Copilot asks you to sign in or activate access, use your own GitHub account.

1. Open Copilot Chat. Start a chat called **Facilitator** and paste the contents of [facilitator-prompt.md](facilitator-prompt.md).
2. Start a second chat called **Work** in the same workspace and paste this prompt:

   > Create a short AGENTS.md in the project root for our simulated Kalundborg outbreak investigation. Use background.md for context. Include instructions to preserve source files, cite evidence, record assumptions and make the analysis reproducible. Show me the file for review. Once I approve it, follow it in this chat for the rest of the exercise.

3. Work through the three tasks below. After each task, switch to **Facilitator**, name the task and ask for a review of the saved files. Make any requested corrections in **Work** and ask for another review.

## Tasks

1. **Review the evidence.** Use [background.md](background.md) to write `evidence-note.md` with one cited finding and one open question.
2. **Analyse the cohort.** Use [cohort_line_list.csv](cohort_line_list.csv) to write and run a standalone base R script, `analysis.R`. Save `results.csv` with cases, non-cases, denominators and attack rates by known exposure, the risk ratio and the number of missing exposures. Show one numerical check.
3. **Write the briefing.** Save a half-page `briefing.md` with the result, one uncertainty and one next action. Check one factual claim against the background and one figure against the results.

See [README.html](README.html) for the full instructions and hints. Download and open the HTML in a browser to see it rendered.
