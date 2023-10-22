# Minimal Reproduction Repo

If the configuration file has an invalid regex in the "allowedVersions" (e.g. not adding slashes at the edges) Renovate finishes normally, but does not create any merge requests.

There is an INFO level message printed about the problem, but if Renovate cannot continue in such an event it should be printed as ERROR and the application should exit immediately.

Running `renovate-config-validator --strict` does not report this problem.

The documentation does not emphasize enough that Regular Expressions have to begin and end with /. Maybe it can be added as a warning block or similar.
https://docs.renovatebot.com/configuration-options/#allowedversions



