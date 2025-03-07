# DMN compliant decision tables in Unicode

## Overview

```shell
$ dsntk --version
```

Output:

```text
0.2.0-dev
```

## Examples

### Rules as rows (horizontal)

#### No inputs

> [H_000010.uc](./H_000010.uc)

```text
 ┌───╥─────────────┐
 │ C ║             │
 ╞═══╬═════════════╡
 │ 1 ║  "Monday"   │
 ├───╫─────────────┤
 │ 2 ║  "Tuesday"  │
 ├───╫─────────────┤
 │ 3 ║ "Wednesday" │
 ├───╫─────────────┤
 │ 4 ║ "Thursday"  │
 ├───╫─────────────┤
 │ 5 ║  "Friday"   │
 ├───╫─────────────┤
 │ 6 ║ "Saturday"  │
 ├───╫─────────────┤
 │ 7 ║  "Sunday"   │
 └───╨─────────────┘
```

```shell
$ dsntk edt --unicode I_000010.ctx H_000010.uc
```

Output:

```text
["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
```

### Rules as columns (vertical)
