# 01-pnpm-version-7

**Feature:** pnpm 7 support with lockfile version 5.4

## Setup

```bash
# Generate lockfile with pnpm 7
npx pnpm@7 install
```

## Snyk CLI Test

```bash
# Basic test
snyk test --org=$SNYK_ORG

# Monitor project
snyk monitor --org=$SNYK_ORG --project-name="FIX-1400-pnpm-v7"

# JSON output for analysis
snyk test --json --org=$SNYK_ORG > results.json
```

## Expected Results

- Snyk should successfully parse the lockfile v5.4 format
- Should detect `lodash` and `minimist` dependencies
- No vulnerabilities expected in these specific versions

## Verification Checklist

- [ ] `snyk test` completes without errors
- [ ] Dependency tree shows correct packages
- [ ] Lockfile version 5.4 is properly parsed
