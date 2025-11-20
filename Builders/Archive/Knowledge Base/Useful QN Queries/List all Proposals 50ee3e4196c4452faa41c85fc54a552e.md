# List all Proposals

Created: January 6, 2023 3:32 AM
Description: List all proposals
Tags: Proposals

```jsx
query MyQuery {
  proposals(limit: 500, orderBy: exactExecutionBlock_DESC) {
    id
    councilApprovals
    creatorId
    description
    details {
      ... on SignalProposalDetails {
        __typename
      }
      ... on RuntimeUpgradeProposalDetails {
        __typename
      }
      ... on SetInitialInvitationCountProposalDetails {
        __typename
      }
      ... on SetInitialInvitationBalanceProposalDetails {
        __typename
      }
      ... on SetMembershipLeadInvitationQuotaProposalDetails {
        __typename
      }
      ... on SetReferralCutProposalDetails {
        __typename
      }
      ... on VetoProposalDetails {
        __typename
        proposal {
          id
        }
      }
      ... on FundingRequestProposalDetails {
        __typename
      }
      ... on SetMaxValidatorCountProposalDetails {
        __typename
        newMaxValidatorCount
      }
      ... on CreateWorkingGroupLeadOpeningProposalDetails {
        __typename
      }
      ... on FillWorkingGroupLeadOpeningProposalDetails {
        __typename
      }
      ... on UpdateWorkingGroupBudgetProposalDetails {
        __typename
      }
      ... on SlashWorkingGroupLeadProposalDetails {
        __typename
      }
      ... on DecreaseWorkingGroupLeadStakeProposalDetails {
        __typename
      }
      ... on SetWorkingGroupLeadRewardProposalDetails {
        __typename
      }
      ... on AmendConstitutionProposalDetails {
        __typename
      }
      ... on TerminateWorkingGroupLeadProposalDetails {
        slashingAmount
      }
      ... on SetMembershipPriceProposalDetails {
        __typename
      }
      ... on CancelWorkingGroupLeadOpeningProposalDetails {
        __typename
      }
      ... on SetCouncilorRewardProposalDetails {
        __typename
      }
      ... on SetCouncilBudgetIncrementProposalDetails {
        __typename
      }
    }
    status {
      ... on ProposalStatusCanceledByRuntime {
        __typename
      }
      ... on ProposalStatusCancelled {
        __typename
      }
      ... on ProposalStatusExpired {
        __typename
      }
      ... on ProposalStatusRejected {
        __typename
      }
      ... on ProposalStatusSlashed {
        __typename
      }
      ... on ProposalStatusExecuted {
        __typename
      }
      ... on ProposalStatusExecutionFailed {
        __typename
        errorMessage
      }
      ... on ProposalStatusDormant {
        __typename
      }
      ... on ProposalStatusVetoed {
        __typename
      }
      ... on ProposalStatusGracing {
        __typename
      }
      ... on ProposalStatusDeciding {
        __typename
      }
    }
    statusSetAtBlock
    title
  }
}
```