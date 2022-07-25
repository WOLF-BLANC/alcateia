# ajudante pessoal
ajudar


on: [pull_request_target, issues]

jobs:
  greeting:
    runs-on: ubuntu-latest
    permissions:
      issues: write
      pull-requests: write
    steps:
    - uses: actions/first-interaction@v1
      with:
        repo-token: ${{ secrets.GITHUB_TOKEN }}
        issue-message: "agradecemos se você avaliar nosso projeto"
        pr-message: "espero que possamos ajudar melhor você"

