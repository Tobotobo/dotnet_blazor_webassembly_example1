# dotnet_blazor_webassembly_example1

[ASP.NET Core Blazor プログレッシブ Web アプリケーション (PWA)](https://learn.microsoft.com/ja-jp/aspnet/core/blazor/progressive-web-app?view=aspnetcore-8.0&tabs=visual-studio-code)

[Blazor WebAssembly アプリの GitHub Pages への発行を、より楽にする](https://qiita.com/jsakamoto/items/0be0005d9b30acbfe1e4)

[Nuget - PublishSPAforGitHubPages.Build](https://www.nuget.org/packages/PublishSPAforGitHubPages.Build/)

[GitHub - jsakamoto/PublishSPAforGitHubPages.Build](https://github.com/jsakamoto/PublishSPAforGitHubPages.Build)

[Blazor wasmがiOSで動かない時の解決方法](https://qiita.com/Lemon73/items/9ef83c579f8d6eaa55b3)
index.html の `<script src="_framework/blazor.webassembly.js"></script>` の前に `<script>var Module;</script>` を入れる


```
dotnet new blazorwasm --pwa
dotnet add package PublishSPAforGitHubPages.Build --version 2.2.0
```

```
dotnet publish -c:Release -p:GHPages=true -p:GHPagesBase=/
```
`bin/Release/net8.0/publish/wwwroot`