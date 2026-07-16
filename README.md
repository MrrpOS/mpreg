# mpreg

`mpreg`, the MrrpOS Package REGistrar is the official community package manager for MrrpOS. For any query regarding usage of `mpreg` or about how to publish your programs for MrrpOS, kindly contact the developer.

## Links

[Package Maker's Guide](https://mrrpos.gattodev.tech/docs/mpreg-pmg.html)  
[Packages Repo](https://mrrpos.gattodev.tech)  

## CLI Commands

### Viewing & Searching
* `mpreg list-pkgs` - Displays all available packages in the repository.
* `mpreg list-misc` - Displays available miscellaneous files (drivers, wallpapers, etc.).
* `mpreg view-pkg <id>` - Shows detailed metadata for a specific package.

### Managing Software
* `mpreg install <id>` - Downloads and installs a package and its dependencies. If the package is already installed but a new version exists on the server, it will update it.
* `mpreg uninstall <id>` - Removes a package from your system.
* `mpreg update` - Forces a refresh of the local package and misc caches.

### Developer Commands
* `mpreg pack <file>` - Takes a raw binary and compresses it into an `.mpreg` (tar + zstd level 19) archive ready for the repo.

### System Hygiene
* `mpreg cache-clear` - Empties the download cache located at `/mrrpos/mpreg/cache`.
* `mpreg check` - Verifies the SHA256 hashes of all installed packages against the registry to detect tampering.
