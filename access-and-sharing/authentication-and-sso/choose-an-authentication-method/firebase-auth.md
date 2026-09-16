# Firebase Auth

Use the Firebase Auth option when Firebase is the identity system for your app's audience.

## Start configuration

1. Open **More → Authentication**.
2. Under **External Authentication**, select **Add External Authentication**.
3. Choose **Firebase Auth**.
4. Complete the settings requested by the current provider form using your Firebase project's configuration.
5. Check any app or domain values against the environment you intend to use.

The provider selector identifies Firebase Auth as available on All plans. Confirm any additional requirements shown in your app when configuring it.

## Prepare a test

Use a Firebase test account intended for this app. Verify that sign-in resolves to the expected person, that membership and team assignment are correct, and that the published app grants only the intended access.

Keep provider secrets out of screenshots, client-side app code, and support messages. The fields and setup requirements depend on the provider form; do not copy another application's configuration.

If sign-in fails, record the time and visible error, check [System logs](../../audit-logs-privacy-and-security/investigate-system-logs.md), and follow [the sign-in troubleshooting checklist](../troubleshoot-sign-in.md).
