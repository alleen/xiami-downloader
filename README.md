# Xiami Music Preview Downloader

A simple tool for downloading music previews from [Xiami.com][1]

Note: this is a python script using python 2.

## Dependency

* Optionally depends on `mutagen` module for ID3 tag support.

## Usage

    python xiami.py [options]

## Options

* `-a <album id>` Adds all songs in an album to download list.
* `-p <playlist id>` Adds all songs in a playlist to download list.
* `-s <song id>` Adds a song to download list.
* `-f` Force mode. Overwrite existing files without prompt.
* `-t urllib2|wget` Change the download tool.
* `-h` Shows usage.
* `--no-tag` do not add tag.
* `--directory` save all downloads into the directory.
* `--name-template` Filename template.
* `-x <proxy_host:proxy_port>` Download file throw proxy.

`<song id>`, `<playlist id>` and `<album id>` can be retrived from URLs of Xiami.

Default download tool is the built-in urllib2 on Windows, others will be wget.

Filename template defaults to `{id} - {title} - {artist}`. The arguments are:

* `{id}` ID
* `{title}` Title of the track
* `{artist}` Artist of the track

## Example

To download the album _Mahōtsukai no Yoru OST_, first refer to the url <http://www.xiami.com/album/511682> to get album ID: __511682__. Then use the following command to download:

    python xiami.py -a 511682

## License

This software is distributed under the [MIT License][2].


---

# 虾米音乐试听下载器

从[虾米网][1]上下载音乐试听的小工具。

注：这是一个 Python 2 脚本

## 依赖

* 可选择依赖于 `mutagen` 模块，由其提供 ID3 支持。

## 使用方法

    python xiami.py [选项]

## 选项

* `-a <专辑ID>` 下载该专辑中的所有歌曲。
* `-p <精选集ID>` 下载该精选集中的所有歌曲。
* `-s <歌曲ID>` 下载该歌曲。
* `-f` 强制模式。不经确认直接覆盖重名文件。
* `-t urllib2|wget` 修改下载工具。
* `-h` 显示用法。
* `--no-tag` 不添加 ID3 Tag。
* `--directory` 将下载到的文件放入该文件夹中。
* `--name-template` 文件名模版。
* `-x <代理伺服器:代理伺服器埠>` 下載時透過代理伺服器下載

`<歌曲ID>`、`<精选集ID>` 及 `<专辑ID>` 都可以从对应虾米页面的 URL 中找出。

默认下载工具在 Windows 上是内置的 urllib2，其它平台则是 wget。

文件名模版默认值为 `{id} - {title} - {artist}`，可选参数如下：

* `{id}` 编号
* `{title}` 该音轨的标题
* `{artist}` 该音轨的作者

## 示例

例如要下载专辑《魔法使いの夜 オリジナルサウンドトラック》，首先从其 URL <http://www.xiami.com/album/511682> 中找出专辑 ID： __511682__。然后使用如下命令下载：

    python xiami.py -a 511682

## 许可

Xiami Music Preview Downloader 使用 [MIT License][2] 发布。

[1]: http://www.xiami.com "虾米"
[2]: http://opensource.org/licenses/MIT "The MIT License"
