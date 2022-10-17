# renovate-config

Shareable config presets for akashic-games.

## usage

### default

* `@akashic` モジュールは即時に PullRequest を作成する
* それ以外のモジュールは業務時間外に PullRequest を作成する

```json
{
  "extends": ["github>akashic-games/renovate-config"]
}
```

### groupPatchMinor

* `@akashic` モジュール以外の patch, minor 更新をそれぞれ一つの PullRequest にまとめる

```json
{
  "extends": ["github>akashic-games/renovate-config:groupPatchMinor"]
}
```

### bumpAkashicPatch

* `@akashic` モジュール patch 更新時に package.json の patch version をすすめる

```json
{
  "extends": ["github>akashic-games/renovate-config:bumpAkashicPatch"]
}
```

### groupAll

* すべての依存を一つの PullRequest にまとめる

```json
{
  "extends": ["github>akashic-games/renovate-config:groupAll"]
}
```

### engineFilesAlias/update

* `@akashic/engine-files@v*` のエイリアス `aev*` を "at any time" で更新する

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/update"]
}
```

### engineFilesAlias/automerge

* `@akashic/engine-files@v*` のエイリアス `aev*` の PullRequest を auto-merge する

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/automerge"]
}
```

### engineFilesAlias/bump

* `@akashic/engine-files@v*` のエイリアス `aev*` の patch, minor 更新に応じて自身のバージョンをすすめる

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/bump"]
}
```

### engineFilesAlias/bump

* `engineFilesAlias/` 配下の `update`, `automerge`, `bump` を合わせたルール

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/default"]
}
```