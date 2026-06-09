# Privacy-Preserving Lead Transfer Pseudocode

```text
function prepare_user_controlled_transfer(user_data, recipient_public_key):
    if user_consent is false:
        stop

    selected_data = apply_user_share_level(user_data)
    symmetric_key = generate_random_symmetric_key()
    encrypted_payload = encrypt(selected_data, symmetric_key)
    encrypted_key = encrypt(symmetric_key, recipient_public_key)

    return {
        encrypted_payload,
        encrypted_key,
        minimal_metadata
    }
```

This pseudocode is conceptual only. It is not production cryptographic code.
