# Eii.Ecopath.MergeSplitGroupsPlugin

Utility plug-in for EwE to merge and split functional groups

## Package

- **Package ID:** `Eii.Ecopath.MergeSplitGroupsPlugin`
- **License:** EUPL-1.2
- **Icon:** `EII_plain_128x128.png`

The package automatically places `EwEMergeSplitGroupsPlugin.dll` and its accompanying symbols and XML documentation (when copied) in `Plugins\MergeSplitGroupsPlugin\` beneath the consuming project's build output. SDK-style publish output uses the same layout, including publishing with `--no-build`. PackageReference consumers also inherit these rules through transitive package references.

Dependencies keep their normal output locations. The host must load the plugin from this subdirectory; installing the package does not configure assembly probing. The NuGet cache layout is unchanged.

## Build

Build the solution on Windows with the .NET SDK and .NET Framework 4.8 targeting pack:

``powershell
dotnet build .\Eii.Ecopath.MergeSplitGroupsPlugin.slnx --configuration Release
``

Packages are versioned by GitVersion in CI. The `Eii.*` dependencies require access to the Ecopath International Initiative GitHub Packages feed.

## CI/CD

The `master` branch is protected and requires pull requests to merge. Pull requests must pass the build check. Merges to `master` publish the NuGet package.