# Damage Range Pseudocode

```text
function estimate_damage_range(base_amount, personalization_factor, reductions):
    low = base_amount
    high = base_amount * (1 + personalization_factor)

    for reduction in reductions:
        low = low * (1 - reduction)
        high = high * (1 - reduction)

    return [low, high]
```

This pseudocode is not a production formula and does not represent legal advice.
