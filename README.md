# auto-approval-poc

## Auto Approval Plan
To achieve auto approval on Altera PR requests to Inventory we can either utilize an action or webhook that would be setup on the inventory repo. The webhook/action would be listening to the "PR opened event" which would either trigger the webhook event or github action that would evaluate the opened PR and check if the branch name follows this name scheme 'user/altera-approver/**' and the PR was opened by an Altera team member. 

## Actions Auto-Approaval Implementation
Here is the github actions altera github actions implementation [HERE](https://github.com/jaron-bauers/auto-approval-poc/blob/main/.github/workflows/poc-2.yml). 

`NOTE: The webhook could be implemented the same exact way, but instead of an event listener it would be a webhook and the create a review api call would be a curl command within a script on a VM that the webhook payload is being sent to.`
