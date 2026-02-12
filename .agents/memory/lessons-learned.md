# Lessons Learned & Constraints

_The AI must check this file before implementing new features to avoid repeating past mistakes._

## Privacy & Security Strictness

- **Constraint Added:** Do NOT use standard analytics tracking packages. They violate our core privacy requirements.
- **Constraint Added:** AI agents sometimes attempt to use external CDNs (like `cdnjs` or `Google Fonts`) in HTML/UI templates. This violates the air-gapped rule. Always use package managers to install dependencies locally and bundle them. Never use `<script src="http...">` or `<link href="http...">`.
- **Constraint Added:** Hardcoding file paths (like `C:/Users/`) breaks cross-platform compatibility and can expose usernames. Always use native path resolution libraries (e.g., Python's `pathlib`, Node's `path.join`, Rust's `dirs` crate) to resolve local application data directories.
