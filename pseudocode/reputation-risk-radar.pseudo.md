# Reputation Risk Radar Pseudocode

```text
function reputation_risk_profile(inputs):
    visibility = classify_visibility(inputs.channel, inputs.audience)
    severity = classify_statement(inputs.content_type)
    evidence = classify_evidence(inputs.proofs)
    urgency = classify_urgency(inputs.persistence, inputs.virality, inputs.sensitive_data)

    return {
        visibility,
        severity,
        evidence,
        urgency,
        professional_review_recommended
    }
```

This simplified pseudocode does not include CalcuLegal’s production scoring model.
