# CLAUDE.md — secondsource-verdicts(org repo)行為總則

> 任何打開這個 folder 的 session 都讀這檔。
> 這是 org repo(`secondsource-ai/secondsource-verdicts`),身分邊界與本機其他 repo 不同。

## 身分邊界(違反 = bug)

- **這個 repo 一律以 `secondsource-devops` 身分推送。** 遠端只走 SSH 別名
  `github.com-ssbot`(`~/.ssh/config` 內的 Host 區塊,IdentityFile `~/.ssh/id_ss_bot`),
  origin URL 必須是 `git@github.com-ssbot:secondsource-ai/secondsource-verdicts.git`。
- repo 層級 git 身分(不加 `--global`):
  - `user.name` = `secondsource-devops`
  - `user.email` = `312676049+secondsource-devops@users.noreply.github.com`
- **禁止在本機跑 `gh auth login` 切帳號。** gh 的登入是全域狀態,切換會誤傷本機其他
  五個以 `michaelchen73092` 身分運作的 repo。本 repo 的認證完全由 SSH 別名承擔,
  不需要也不得動 gh 的帳號狀態。

## 憑證紀律

- **任何 token(PAT / ghp_ / github_pat_)不得寫進 remote URL 或任何入 git 的檔案。**
  判例:mvj-knowledge 的 `.git/config` 曾明文存 PAT。認證一律走 SSH 金鑰
  (`~/.ssh/id_ss_bot`),token 需要存放時放 repo 外且 chmod 600。

## commit 紀律

- **每完成一單位工作即 commit**(D-20260720-01,任一 repo 皆然),commit msg 標角色名。
- **commit 一律點名檔案,禁 `git add -A` / `git add .`**。

## pre-push 機械閘

- hooks 走版本化目錄:`core.hooksPath = .githooks`(`.git/hooks` 不會跟著 clone 走)。
- `.githooks/pre-push` 在每次 push 前做三項檢查,任一不過就擋下 push(exit 1):
  1. **(a) remote 檢查**:`git remote get-url origin` 必須以 `git@github.com-ssbot:` 開頭
     ——確保走的是 bot 金鑰,不是預設的 github.com(michaelchen73092)。
  2. **(b) email 檢查**:repo 的 `git config user.email` 必須等於
     `312676049+secondsource-devops@users.noreply.github.com`
     ——確保 commit 作者歸戶到 bot 帳號。
  3. **(c) token 防呆**:`.git/config` 內不得出現 `github_pat_` 或 `ghp_` 字樣
     ——防明文 token 入檔(見上方判例)。
- **hook 失敗怎麼判讀**:錯誤訊息會印出是 (a)/(b)/(c) 哪一項、實際值、修法一行。
  照修法修完再 push;**不得用 `--no-verify` 繞過**——閘紅著就 push 成功,代表身分
  或憑證已污染,先修再推。若 hook 完全沒觸發(push 前沒看到任何檢查輸出),先查
  `git config core.hooksPath` 是否還是 `.githooks`、hook 檔是否有執行權限。

## 記憶歸戶

- 本 repo 的 `memory/` 為判例記憶 SSoT(照 air 的 D-20260802 模式)。
  `michaelchen73092` 與 `secondsource-devops` 兩個 config_dir 的
  `projects/-Users-weicch-secondsource-verdicts/memory` 均 symlink 指向它,
  任何帳號讀寫的都是同一份。新帳號加入時照同模式補 symlink。
