# docker-environment

# dockerを用いた環境構築

docker+Laravel+reactの環境を構築
参考文献：https://sagara.ink/article/app/204/

laravelの最新バージョンであると、laravel MixからViteへ移行されているため修正する必要あり
https://readouble.com/laravel/9.x/ja/vite.html

以下を参考にlaravel Mixへと修正
https://github.com/laravel/vite-plugin/blob/main/UPGRADE.md#migrating-from-vite-to-laravel-mix

そこからさらに
```
Support for the experimental syntax 'jsx' isn't currently enabled
```
このようなエラーが出たため、ルートディレクトリに .babelrc を作成し、以下を追加
```
{
  "presets": ["@babel/preset-env", "@babel/preset-react"]
}
```
