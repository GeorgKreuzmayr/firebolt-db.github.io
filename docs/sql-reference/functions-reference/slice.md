---
layout: default
title: SLICE
description: Reference material for SLICE function
parent: SQL functions
---

# SLICE

Returns a slice of the array based on the indicated offset and length.

## Syntax
{: .no_toc}

```sql
SLICE(<array>, <start>[, <length>])
```
## Parameters
{: .no_toc}

| Parameter  | Description                            | Supported input types | 
| :---------- | :------------------------------------ | :-------- | 
| `<array>`    | The array of data to be sliced               | `ARRAY` | 
| `<start>` | Indicates starting point of the array slice | `INTEGER` | 
| `<length>` | The length of the required slice | `INTEGER` | 

## Return Type
`ARRAY` of the same type as input array 

## Example
{: .no_toc}

The following example slices the `levels` array to a different length: 
```sql
SELECT
	SLICE([ 1, 2, 3, 4, 5 ], 1, 3) AS levels;
```

**Returns**: `[1, 2, 3]`
