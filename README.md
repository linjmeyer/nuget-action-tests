# Example workflow for Nuget and Github Actions

* All push and pull-requests events trigger a build
* `git push --tags` triggers `dotnet pack` and `dotnet nuget push`
* When `dotnet nuget push` is successful, a GitHub release is created
* Tags should be in format `v1.0.0` and `v1.0.0-alpha`
* GitHub Releases are correctly marked as pre-release when a tag contains a dash (follows Nuget spec)