# Questionnaire implementation

- questionnaire.html: public 8-question reflection; no direct identifiers, storage or network submission.
- intake.html: 30-question preparation flow, including 6 basic personal fields and 2 topic-specific questions. No patient-facing clinical interpretation. Adult use only.
- questionnaire-review.html: public local-file reader, no account, no stored patient records. Import only files provided to you. No remote upload.
- The browser processes answers in memory. Download is explicit; transfer to the therapist is manual. Default export omits name, age, phone and town; free text can still identify a person and must be reviewed.
- Rule-based summaries are interview prompts, not validated scores or diagnoses. Session counts are not inferred.
- Run: node --test tests/questionnaire.test.cjs

Browser QA: completed public anxiety/avoidance flow, completed preparation flow with fictional data, observed download and explicit not-sent status. Browser-generated file bytes reside on a separate host and were not independently read. Unit tests cover exported payload and identifier omission. Responsive CSS implemented; no mobile viewport emulation performed.
