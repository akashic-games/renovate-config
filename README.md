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
