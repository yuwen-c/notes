> 系統從原本電腦(m1)migrate 到新電腦(m2)，使用 timemachine，約 1h 搬完

- 系統轉移後，開專案的 terminal 出現此錯誤，git 也無法使用(不過`.git`檔案是在的)，還有一些 xcode 的錯誤訊息

```bash
[oh-my-zsh] Can't update: not a git repository.
```

- 開電腦的 terminal，也是一樣的錯誤

[參考](https://github.com/ohmyzsh/ohmyzsh/issues/10861)

重新安裝

```sh
xcode-select --install
```

- 需要跑 10min 左右

- 安裝完就 ok，也不用另外設 git
