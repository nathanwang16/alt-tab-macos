# AltTab

[![Screenshot](docs/public/demo/frontpage.jpg)](docs/public/demo/frontpage.jpg)

**AltTab** brings the power of Windows alt-tab to macOS

[Find out more on the official website](https://alt-tab-macos.netlify.app/)

# Building Reminders

Although from the Alt-tab [official website](https://alt-tab-macos.netlify.app/contributing) the instruction is given related to how to build the xcode project locally, some extra reminder is needed. The exact sentence is quoted below...

> scripts/codesign/setup_local.sh` to generate a local self-signed certificate, to avoid having to re-check the `System Preferences > Security & Privacy` permissions on every build



You cannot successfully save and use the generated certificate by simply run `scripts/codesign/setup_local.sh`, however the certificate is correctly generated.

You should modify the generate_certificate.sh file which is in the `scripts/codesign` directory by adding a `-legacy` option modifier.

The reason and solution is stressed clearly in [this stackoverflow response](https://stackoverflow.com/questions/70431528/mac-verification-failed-during-pkcs12-import-wrong-password-azure-devops). 



