# INAIL Differential Damage Pseudocode

```text
function estimate_differential_damage(civil_damage, inail_indemnity, homogeneous_scope):
    if responsibility_not_assessed:
        return "professional review required"

    comparable_inail = select_homogeneous_items(inail_indemnity, homogeneous_scope)
    differential = civil_damage - comparable_inail

    if differential < 0:
        differential = 0

    return differential
```

## Notes

This simplified pseudocode documents the public concept of comparing homogeneous items. It does not reproduce CalcuLegal’s production logic.
