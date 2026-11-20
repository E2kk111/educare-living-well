# Educare Living Well — Integration Plan

## Architecture

Public website → assessment intake API → protected database → authorized outreach dashboard.

Living Well eLMS and aggregate outcome reporting will be separate modules with role-based access.

## Implementation phases

1. Reconstruct and version-control approved public site content and design.
2. Implement validated assessment submission, spam protection, consent language, and notifications.
3. Create an access-controlled facility/contact CRM with audit events.
4. Connect authorized staff dashboard to backend and replace browser-only CSV storage.
5. Add eLMS lessons and resident-centered aggregate pilot metrics.
6. Configure CI checks and GitHub-connected Vercel deployments.

## Security requirements

- No patient or resident-level sensitive data in public code, Git history, or client-side logs.
- Enforce server-side authorization for every dashboard/API request.
- Use managed secrets, encryption, least privilege, audit logging, backups, and retention rules.
- Assess HIPAA applicability before collecting any protected health information.
- Protect public forms against abuse; do not treat a draft-email CTA as a submitted assessment.

## Existing deployment limitations

The existing public assessment prepares an email draft rather than saving a record. The dashboard supports browser-local CSV workflows and is not a shared CRM. Do not advertise these as integrated capabilities until tested end-to-end.
