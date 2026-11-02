## Reproduction

Run:

```bash
npm install
```

## Actual result

Installation fails with `ERESOLVE` because `@auth/core@0.41.3`
requires the optional peer dependency `nodemailer@"^7.0.7 || ^8.0.5"`,
while this project specifies `nodemailer@10.3.1`.

## Expected result

Auth.js validates compatibility with Nodemailer 10 and updates its
peer dependency ranges to permit supported security releases.

This reproduces an installation conflict, not a runtime incompatibility.
