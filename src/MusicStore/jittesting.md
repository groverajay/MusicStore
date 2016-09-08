Instructions for JIT testing:

`git clone <music store repo>`
`git checkout jitbench`
`cd src\MusicStore`
`dotnet restore`
`dotnet publish –c Release –f netcoreapp10`
`cd bin\Release\netcoreapp1.0\publish`
`.\crossgen-publish.ps1`
`dotnet MusicStore.dll`

Currently the CoreCLR package and version are hardcoded to win7-x64 and 1.0.2.
To change the platform or version, $platform, $coreclrversion and $clrjitversion needs to change accordingly in src/MusicStore/get-crossgen.ps1. 