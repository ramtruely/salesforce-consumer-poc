# salesforce-consumer-poc

- name: Detect First PR
  id: pr-detect
  run: |
    PR_NUMBER=${{ github.event.pull_request.number }}

    echo "Current PR Number: $PR_NUMBER"

    if [ "$PR_NUMBER" -eq 1 ]; then
      echo "first_pr=true" >> $GITHUB_OUTPUT
    else
      echo "first_pr=false" >> $GITHUB_OUTPUT
    fi
