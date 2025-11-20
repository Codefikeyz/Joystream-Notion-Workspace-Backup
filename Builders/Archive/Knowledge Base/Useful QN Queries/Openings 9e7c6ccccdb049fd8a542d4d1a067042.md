# Openings

Created: June 17, 2022 10:46 PM
Description: new, filled, canceled openings
Tags: Working Groups (WGs)

Shows changes during a term if start and end are known:

```jsx
query {
  openingAddedEvents (where: {inBlock_gt: 1051200, inBlock_lt: 1152000 }, limit: 10000) { inBlock groupId openingId}
  openingFilledEvents (where: {inBlock_gt: 1051200, inBlock_lt: 1152000 }, limit: 10000) { inBlock groupId openingId }
  openingCanceledEvents (where: {inBlock_gt: 1051200, inBlock_lt: 1152000 }, limit: 10000) { inBlock groupId openingId }
}
```

Everything ever:

```jsx
query {
  openingAddedEvents (limit: 10000) { inBlock groupId openingId}
  openingFilledEvents (imit: 10000) { inBlock groupId openingId }
  openingCanceledEvents (imit: 10000) { inBlock groupId openingId }
}
```