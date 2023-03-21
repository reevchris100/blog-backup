---
title: "Important Excel Formulas and Commands we need to know"
seoTitle: "Must Know Excel commands and formulas for daily use"
seoDescription: "Important and must know excel commands and formulas for daily use."
datePublished: Tue Mar 21 2023 10:27:52 GMT+0000 (Coordinated Universal Time)
cuid: clfi43wnx000709mh3han75ml
slug: important-excel-formulas-and-commands-we-need-to-know
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679393253536/d051a589-6358-4680-97f7-aea7696f5fb0.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679394427845/820628fc-59df-4851-80ca-cbc09653e741.jpeg
tags: excel, vlookup, commmands

---

Some of the important Excel formulas and commands are as follows:

### Column to comma-separated values

```plaintext
=TEXTJOIN(",", TRUE, A:A)
```

### Select entire column

```plaintext
Ctrl + Space
```

### Look for value from a column in table or list

```plaintext
=VLOOKUP($A1, list2, 2, false)
=VLOOKUP(A2, G:G, 1, 0)
=VLOOKUP(A2, J:K, 1, 0)
```

### Conditional IF

```plaintext
=IF(A2<>A1,"LAST","")
=IF(E2="Override", $B2,"")
```

### Return count of cells equal to a specific value

```plaintext
=COUNTIF(range, value)
=COUNTIF(A3:A12, "blue")
```

### Sum of values in column

```plaintext
SUM(A:A)
```

### Count unique values

```plaintext
=COUNTA(UNIQUE(A1:A12))
```