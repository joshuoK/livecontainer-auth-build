# LiveContainer + SideStore: experimental authentication fix

**Tested and reported working by the repository owner on 15 October 2026, on an iPhone running iOS 18.7.8.** This report applies to **AuthFix v3**, including the Apple Account sign-in and verification-code flow. Testing on other devices and accounts is welcome.

This is a **personal, unofficial custom-build repository**. It is not an official LiveContainer or SideStore release, and this repository was created independently rather than through GitHub's Fork button. The application is based on the upstream projects linked below.

## Download

- [Successful v3 build and artifacts](https://github.com/joshuoK/livecontainer-auth-build/actions/runs/38779378139)
- [Download the v3 artifact ZIP without signing in to GitHub](https://nightly.link/joshuoK/livecontainer-auth-build/actions/artifacts/11996131138.zip)

Extract the ZIP and select **LiveContainer+SideStore-AuthFix-v3.ipa** in your signing installer. The IPA must be signed for your own device. The download also includes the source patches, upstream licenses, and provenance information. GitHub build artifacts are retained for 14 days; the workflow can be rerun after they expire.

IPA SHA-256:

```text
40c8187443bc6a90262d41fa1ae791f5cb52b693ddadf58c6486d67972feb798
```

## What changed

The official LiveContainer 3.8.10 host is packaged with its compatible SideStore source and experimental authentication changes adapted from [SideStore PR #1660](https://github.com/SideStore/SideStore/pull/1660). The custom build also preserves the selected Anisette mode and provisioning data for authentication resynchronization, and includes the newer handling for verification codes that Apple sends automatically.

The combined app retains the upstream `com.kdt.livecontainer` bundle identifier. The embedded SideStore build number for v3 is `20261015.3`.

## AI disclosure

**OpenAI Codex was used to inspect the source, adapt and integrate the patches, troubleshoot the custom build, prepare the GitHub Actions workflow, package and check the IPA, and write this documentation.** The repository owner performed the iPhone sign-in test and reported that it worked. AI assistance and a successful compilation do not replace device testing.

## Sources and credits

- [LiveContainer](https://github.com/LiveContainer/LiveContainer), host commit `4dbe0f9a626de801184a42c0be8d2cb105058e3d`.
- [LiveContainer-compatible SideStore](https://github.com/LiveContainer/SideStore), base commit `12a496ca1c766a102193634879823d16610bf1cd`.
- [SideStore](https://github.com/SideStore/SideStore) and [SideSign](https://github.com/SideStore/SideSign).
- [raj-sh-git's experimental authentication work](https://github.com/SideStore/SideStore/pull/1660), including SideSign commit `f4e8df8bd979cba11ddf7c4898e2a5d03ae00dab`.

The upstream projects and contributors retain their respective copyrights and licenses. This repository does not imply their endorsement of this custom build.
