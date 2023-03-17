# node 15 install的module有問題。 只有偶數版的node有被長期維護(LTS)

- 錯誤：node不相容，只支援12/14/16，15不支援

```bash
error strip-css-comments@5.0.0: The engine "node" is incompatible with this module. Expected version "^12.20.0 || ^14.13.1 || >=16.0.0". Got "15.14.0"
error Found incompatible module.
```

### nvm基本指令

- 更新nvm

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

[極簡 nvm 使用指南 | 六小編 Editor Leon](https://editor.leonh.space/2021/nvm/)

- 更新npm

```bash
nvm install-latest-npm
```

- 列出目前有的node版本、現行的node版本(default指著的就是)

```bash
nvm ls
```

- LTS: long term support ，偶數版的node有被長期維護

## 列出可安裝的 Node.js LTS 版本

```
nvm ls-remote --lts

```

偶數的 LTS 版本們有著更長的維護期：

![https://editor.leonh.space/2021/nvm/schedule.svg](https://editor.leonh.space/2021/nvm/schedule.svg)

來源：[Node.js](https://nodejs.org/zh-tw/about/releases/)

看看那短小的奇數版 Node.js 17…建議都使用偶數的 [LTS](https://nodejs.org/zh-tw/about/releases/) 版本，避免追著版號跑的窘境發生。

## 為專案指定 Node.js 版本

在專案的資料夾內，放一個 .nvmrc 檔案，在裡面寫下該專案的 Node.js 版號，例如某專案要用 16.13：

```
16.13

```

進入該專案資料夾後，執行 `nvm use` 即會自動切換成 .nvmrc 指定的版本。

如果在安裝 nvm 時，有設定好與 shell 的整合的話，應該會自動幫我們做 `nvm use` 的動作。

