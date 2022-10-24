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

### engineFilesAlias

`@akashic/engine-files@v*` のエイリアス `engine-files-v*` の設定。

このルールは利用側で `@akashic/engine-files@v*` を `engine-files-v*` にエイリアスしていることを前提としています。

```json
"dependencies": {
  "engine-files-v3": "npm:@akashic/engine-files@3.x.x"
}
```

#### engineFilesAlias/update

*  `engine-files-v*` モジュールは即時に PullRequest を作成する

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/update"]
}
```

#### engineFilesAlias/automerge

* `engine-files-v*` の PullRequest を auto-merge する

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/automerge"]
}
```

#### engineFilesAlias/bump

* `engine-files-v*` の patch が更新されていれば package.json の patch version をすすめ、 minor が更新されていれば minor version をすすめる

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/bump"]
}
```

#### engineFilesAlias/default

* 以下を合わせたルールを利用する
  * `engineFilesAlias/update`
  * `engineFilesAlias/automerge`
  * `engineFilesAlias/bump`

```json
{
  "extends": ["github>akashic-games/renovate-config//engineFilesAlias/default"]
}
```
