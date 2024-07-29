# auto-approval-poc

## Auto Approval Plan
To achieve auto approval on Altera PR requests to Inventory, we can either utilize an Action or Webhook that would be setup on the inventory repo.
The webhook/action would be listening to the "PR opened event" which would trigger the webhook event or github action that would then evaluate the PR and check if:
* the branch name follows this name scheme 'user/altera-approver/**'
* the PR was opened by an Altera team member
* and any other further validation needed...

## Actions Auto-Approaval Implementation
Here is the github actions altera github actions implementation [HERE](https://github.com/jaron-bauers/auto-approval-poc/blob/main/.github/workflows/poc-2.yml). 

`NOTE: The webhook could be implemented the same exact way, but instead of an event listener it would be a webhook and the create a review api call would be a curl command within a script on a VM that the webhook payload is being sent to.`
