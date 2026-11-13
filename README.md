# DSH Browser Bridge — public review downloads

This repository publishes narrowly scoped Browser Bridge review materials. It does **not** expose the private development repository or include anyone's DSH configuration, credentials, browser profile, model keys, or locally installed DSH/ASAR binaries.

## Download

[0.2.17 development-identity review preview](https://github.com/eranfu/dsh-browser-bridge-review/releases/tag/v0.2.17-review-preview)

This preview contains the Browser Bridge plugin/Native Messaging relay, a matching Interaction dependency, MIT notices, a read-only verifier, and English installation/reviewer/recovery instructions.

**It is not a standalone DSH installer or a Store-ready build.** The relay needs a running real DSH Host. The final Chrome Web Store Item ID/public key and matching Native allowed origin are still pending. Do not submit the development preview as an already published Store integration.

ZIP SHA-256:

~~~text
435a60f64c1ae66597f02241e5145bcec03fb4e2c31b75a79c02bac94d4d24a6
~~~

## Supported Host entry

Obtain DSH from [the official Harness site](https://www.deepseek.com/harness/) or the documented public npm entry. The preview instructions pin the publicly available package:

~~~powershell
npx.cmd @deepseek-ai/dsh@0.2.2-rc.1 web
~~~

This command is for an authorized reviewer on a clean review environment, with standalone Node >=24.9.0. It downloads and starts real DSH and creates local state. It was **not run** to prepare this package. Do not start a second Host against an existing profile.

Extract the ZIP, read its README, verify its checksums, then use the existing DSH Plugin Manager to install the supplied Interaction 0.2.16 and Browser Bridge 0.2.17 tarballs. No invented plugin CLI, fake Host, enterprise policy, copied token or copied browser profile is used.

Installation, activation, pairing, model access, browser actions and complete native teardown are separate checks. The preview has static/archive/syntax validation, **not clean-machine runtime acceptance**. Complete ownership-safe native uninstall is not provided in this baseline; use the documented review-environment teardown and retain unresolved work rather than deleting state to simulate success.

## Benign functional test page

[Browser Bridge Safe Demo](https://eranfu.github.io/dsh-browser-bridge-review/) is publicly accessible without an account. Its code only echoes sample input and increments an in-page counter; it does not persist or submit the input. The page also contains blank sensitive-field refusal fixtures—do not enter real credentials. GitHub Pages may record normal hosting access logs.

Public HTTP availability has been checked; this does not certify actual Bridge/DSH page actions. Complete the kit’s real pairing and functional checks in the review environment.

## Privacy and support

[Public privacy policy](https://gist.github.com/eranfu/65c245f132e326876c7faf13bac404ff)

Support and privacy contact: 1119369173@qq.com. Do not send passwords, tokens, cookies or private page contents.

The extension runs locally but its task results can be passed through DSH to the model/middleware selected by the user and to operated websites. It is not a promise that all task data stays on the machine.
