# Security

Please report security problems privately through
[GitHub's private vulnerability reporting](https://github.com/agilkatakam/kora/security/advisories/new), not in a
public issue.

Include the Kora version (Settings → About), what an attacker could do, and the steps to reproduce it. You'll get an
answer as soon as possible, and fixes ship through Kora's automatic updates.

Every Kora release is signed with an Apple Developer ID and notarized by Apple. To check the copy on your Mac:

```bash
spctl --assess --verbose /Applications/Kora.app
```

It should say `accepted` and `source=Notarized Developer ID`.
