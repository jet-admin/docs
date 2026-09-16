# Published changes are missing

Use this sequence when a change appears in Preview but the audience sees an older or different app.

## Check the release path

1. Confirm that you are inspecting the intended app and environment.
2. Identify a specific visible change that should be in the release.
3. Open [Version History](../../ai-app-builder/test-and-publish/version-history.md) and note the version being previewed.
4. Confirm that the intended changes were published; Previewing now is not a published-version indicator.
5. Open the configured published address, rather than a builder or preview address.
6. Sign in as the intended user and check the same page and action.

The invitation dialog warns that non-builder users see the published app. A builder's successful preview does not establish that a release is available to those users.

## If the result still differs

Check whether the user is following an old bookmark, a different custom domain, or an embedded URL pointing to another app or environment. Compare the exact addresses.

Reload the published page after confirming the release. If only one user sees a difference, check their account, team, and record scope before attributing it to an outdated version.

Capture the version, address, user role, time, and publication result. Use [deployment diagnostics](resource-and-deployment-errors.md) for loading failures and [access troubleshooting](published-app-access-fails.md) for role-specific differences.

After correcting the cause, repeat [release verification](../publish-your-app/verify-a-release.md).
