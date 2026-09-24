# ArcPad

A spatial app launcher for Mac. Your apps live in circles, not a grid.

This repository publishes **official binaries** only. Source is private.

## Download

Install from the Mac App Store when the listing is live, or from [GitHub Releases](https://github.com/nguyenvu/arcpad-release/releases).

Latest file name: `ArcPad-1.0.3.dmg`

After you attach a release asset, verify it:

```bash
shasum -a 256 ArcPad-1.0.3.dmg
```

Do not commit the `.dmg` to this repo. Attach it to the release.

## Homebrew (tap later)

```ruby
cask "arcpad" do
  version "1.0.3"
  sha256 "REPLACE_AFTER_RELEASE"

  url "https://github.com/nguyenvu/arcpad-release/releases/download/#{version}/ArcPad-#{version}.dmg"
  name "ArcPad"
  desc "Spatial app launcher for Mac"
  homepage "https://github.com/nguyenvu/arcpad-release"

  app "ArcPad.app"

  zap trash: [
    "~/Library/Preferences/com.voq.no.ArcPad.plist",
  ]
end
```

## What’s new in 1.0.3

- Installed name is ArcPad
- All Apps in a bubble layout
- Hover zooms the apps closest to the pointer
- All Apps in the category bar and next to ⌘F
- Distinct icons for All Apps and Other

## License

See [LICENSE](LICENSE). All rights reserved.
