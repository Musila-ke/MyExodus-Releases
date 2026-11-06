# MyExodus Releases

This repository holds published MyExodus release artifacts and the signed update policy only.
It never contains application source code.

- `artifact-v<versionCode>` releases are prereleases holding the exact signed APK for that
  version. They are published once and never modified.
- `policy-<sequence>` releases hold the signed `update-manifest.json` policy and are marked
  latest. Rollout changes and halts are always new, higher-sequence releases.

The app discovers updates through:

https://github.com/Musila-ke/MyExodus-Releases/releases/latest/download/update-manifest.json

Every policy envelope and APK is verified against keys pinned inside the installed app before
anything is downloaded or installed. A manual install must use the exact APK referenced by the
latest signed policy.
