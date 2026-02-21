# Tauri 26
This is the latest version of Tauri v2 but merged with (https://github.com/tauri-apps/tauri/pull/14671)[this PR].

It adds support for MacOS Tahoe 26.X Themed icons such as Clear, and DarkMode I didn't make the original PR it was made by someone else I just merged them for Zeo and other future Tauri Projects.

To use this just clone the source
```
git clone https://github.com/Discomfit/tauri-26.git
```

Then use pnpm to download the correct dependencies and build it.
```
pnpm install
pnpm build
```

Lastly in your Tauri app in the src-tauri/Cargo.toml add this at the bottom
```
[patch.crates-io]
tauri = { path = "/Users/{Your User}/PATHTO/tauri-26/crates/tauri" }
tauri-build = { path = "/Users/{Your User}/PATHTO/tauri-26/crates/tauri-build" }
tauri-bundler = { path = "/Users/{Your User}/PATHTO/tauri-26/crates/tauri-bundler" }
```

When you go to test your tauri app with this it wont show the icon if you run
```
package-manager tauri dev
```

It will only show when the application is built
```
package-manager tauri build
```
