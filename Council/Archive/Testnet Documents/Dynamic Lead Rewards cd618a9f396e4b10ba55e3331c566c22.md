# Dynamic Lead Rewards

Status: [Approved](https://dao.joystream.org/#/proposals/preview/154)

## **How to determine group budget**

Group budget `b` is a function of

- `w`: [group weight](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring#weights)
- `B`: total group budget
- `t`: total weight, sum of all weights (listed in council plan)

`b = B * w/t`

As formula: `round(multiply(59 / 33, prop("Weight")))`

## **How to determine earned budget**

Earned budget `e` is a function of

- `b`: group budget
- `s`: group score

`e = b * s`

## **How to adjust lead reward**

Lead reward `r` is a function of

- group budget `b`: published in council plan
- group score `s`: published [here](https://github.com/bwhm/founding-members/tree/new-incentives-grading/council-scoring-period-results)
- wg lead `bonus`: published in last report, based on [Lead Bonuses](../Lead%20Bonuses%2043ddd90f19bb4c9e8931cf3c1568d864.md)
- arbitrary factor `f`: percentage of earned budget paid to lead, here 10% (could be dynamic too)

`r = f * s * b + bonus`

# Examples

Based on [](https://www.notion.so/b9ea7c6923e74539941477d1a2e083a6?pvs=21) and [Lead Bonuses](../Lead%20Bonuses%2043ddd90f19bb4c9e8931cf3c1568d864.md) 

## Council 9

[Untitled](Dynamic%20Lead%20Rewards/Untitled%206c45d973e0684237a8790e4425294b6b.csv)

## Council 8

[Scores 7](Dynamic%20Lead%20Rewards/Scores%207%20bfe67dca33db4973855104d23d65d0f9.csv)

[Scores 8](Dynamic%20Lead%20Rewards/Scores%208%20a90e7c676404456e8b00dbee6e93a0f0.csv)

## Council 6

[Scores 5](Dynamic%20Lead%20Rewards/Scores%205%2070cc15adab704f7e8abd005125baaec9.csv)

## Council 5

This uses weights and scores for [round 4](https://github.com/bwhm/founding-members/blob/new-incentives-grading/council-scoring-period-results/4.md) to calculate hypothetical lead rewards for round 5.

[Scores 4](Dynamic%20Lead%20Rewards/Scores%204%2052abe1f775aa47c0bd63e86b94050e1c.csv)

[Formulas](https://www.notion.so/help/formulas)