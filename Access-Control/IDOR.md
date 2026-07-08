# Insecure Direct Object Reference (IDOR)

## What is IDOR?

An IDOR vulnerability occurs when an application allows a user to access another user's resources by changing an identifier.

---

## Example

A user visits:

/profile?id=10

Changing the ID to:

/profile?id=11

returns another user's profile because the server does not verify ownership.

---

## Why does it happen?

The application checks whether the object exists but does not verify whether the current user is authorized to access it.

---

## Prevention

- Perform server-side authorization checks.
- Never trust user-supplied object IDs.
- Use indirect references when appropriate.

---

## What I learned

Access control must always be enforced on the server, even if the client hides links or buttons.
