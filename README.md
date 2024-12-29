# ZFS Project

This repository contains custom code, documentation, and scripts related to ZFS.

## Structure
- src/: Source code
- docs/: Documentation
- scripts/: Utility scripts
- tests/: Test files
- rpm/: RPM spec files and sources
- build/: Build artifacts (not tracked in git)

## Development Environment
This project uses an Incus container for development. The script for setting up this container can be found in the [scripts repository](https://github.com/YourUsername/scripts-repo) as `create-incus-container.sh`.

## Building and Installing ZFS RPMs

The Incus container created by the setup script already includes all necessary dependencies for building ZFS RPMs.

To build the ZFS RPMs in your Incus container:

1. Clone this repository in your home directory:
   git clone https://github.com/MelAneeHannah-git/zfs-project.git

2. Copy the spec file to your rpmbuild directory:
   cp ~/zfs-project/rpm/SPECS/zfs.spec ~/rpmbuild/SPECS/

3. Build the RPMs:
   rpmbuild -ba ~/rpmbuild/SPECS/zfs.spec

4. Once built, the RPMs will be in the RPMS directory. To install them:
   sudo dnf install ~/rpmbuild/RPMS/x86_64/zfs-*.rpm

Note: You may need to adjust the architecture (x86_64) if you're building for a different architecture.

## Contributing
Please read CONTRIBUTING.md for details on our code of conduct and the process for submitting pull requests.
