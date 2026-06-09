# Balthazard Pseudocode

```text
function combine_impairments(percentages):
    sort percentages descending
    combined = 0

    for p in percentages:
        combined = combined + p * (100 - combined) / 100

    return round(combined)
```

## Notes

This is simplified didactic pseudocode. Production implementations may include validation, rounding rules, source handling, jurisdiction-specific logic and edge-case treatment.
