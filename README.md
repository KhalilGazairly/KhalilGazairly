### Hi there 👋


**KhalilGazairly/KhalilGazairly** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on [Pinterest Clone](https://pinterest-iti.herokuapp.com/)
- 🌱 I’m currently learning Django Restframework, ReactJs
<!-- - 👯 I’m looking to collaborate on ... -->
- 🤔 I’m looking for help with Getting Job
<!-- - 💬 Ask me about ... -->
<!-- - 📫 How to reach me: ... -->
<!-- - 😄 Pronouns: ... -->
<!-- - ⚡ Fun fact: ... -->

# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: KhalilGazairly
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Africa/Cairo
