# Cordango — Scoop bucket

The `cordango` command line, for Windows.

```powershell
scoop bucket add cordango https://github.com/cordango/scoop-bucket
scoop install cordango
cordango --help
```

## What you get

One self-contained binary. It carries its own .NET runtime, so there is no SDK to install and
nothing else to restore.

`cordango` compiles an App Definition into a complete application you own: ASP.NET Core with MVC
controllers, EF Core against PostgreSQL, and Vue 3 on the front. Nothing it generates depends on
Cordango at run time.

Both x64 and arm64 are published, and Scoop picks the one that matches the machine.

## Updating

```powershell
scoop update cordango
```

The manifest carries `checkver` and `autoupdate`, so this bucket keeps itself current: a scheduled
job asks GitHub for the latest release, rewrites the version and the two hashes, and commits. A
manifest updated by hand is a manifest that is a release behind — which is worse than having no
channel, because somebody installs it and reports a bug that was fixed a month ago.

## Where this comes from

The manifest is generated from [cordango/cordango](https://github.com/cordango/cordango) —
`packaging/scoop/cordango.json`. Report anything wrong with the tool there; this repository is the
delivery channel.

## Documentation

**[docs.cordango.com](https://docs.cordango.com)** — the [quickstart](https://docs.cordango.com/quickstart),
every [CLI command](https://docs.cordango.com/cli/install), and the
[concepts](https://docs.cordango.com/concepts) behind the language.

## Other ways to install

```powershell
dotnet tool install -g Cordango.Cli    # if you already have the .NET SDK
```

Or download a binary directly from the
[releases](https://github.com/cordango/cordango/releases).

## License

Apache-2.0.
