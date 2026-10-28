# SecondSource — 公開裁決帳 / Public Verdict Record

SecondSource 是一份追蹤 AI 產業的研究通訊(中/英/日;https://secondsource.io)。這個 repo 是它的
公開存證面:我們對 AI 產業說法做出的判斷,在**查核日之前**就逐條寫在這裡——每一條都帶
一個查核日、一組事先講好的判準,以及任何人都能逐次比對的版本紀錄。
*SecondSource is a research newsletter covering the AI industry (https://secondsource.io). This repo is its
public record: calls we make about the AI industry, written down here **before** they can be
settled — each with a check date, a test agreed in advance, and a version history anyone can diff.*

目前 60 條在帳上。｜*60 calls currently on the record.*
官網 / Site: https://secondsource.io

---

## 你正在看的是什麼 / What you're looking at

每一個 `V-YYYY-MM-DD-NN.md` 檔是**一條判斷**。檔裡有:我們的判斷、什麼情況算我們對、
什麼情況算我們錯、哪一天開獎、開獎時要去查哪個來源。中英雙語同檔。

檔案進來之後就留著,對的錯的都留著。**每個檔的 git 歷史記下它何時進來、之後改過什麼**,
任何人都能逐次比對;但 Git 的時間由提交的一方寫入,不是獨立的第三方時間證明。
結果與之後的更正以站上的卡片為準,這裡的同步可能落後。

*Each `V-YYYY-MM-DD-NN.md` file is one call: what we think, what would count as us being right,
what would count as us being wrong, the date it gets settled, and the source to check on that
date. Chinese and English in the same file. Calls stay in, right or wrong. **Each file's git
history shows when it arrived and every change since**, so anyone can compare versions; git
times are written by whoever commits, so they are not independent third-party proof of time.
Results and later corrections live on the site's cards; this mirror may lag behind them.*

## 怎麼用它查我們 / How to audit us

1. **挑任何一個檔,看它的 git 歷史** — `git log --follow V-2026-07-31-01.md`。判準在查核日
   之前改過什麼,每一次都留成一個 commit,看歷史就知道。
2. **挑一個開獎日快到的,自己去查** — 檔裡的 *Source of record* 寫的是我們開獎時要查的那個
   來源。你可以比我們先去查,然後看我們認不認帳。
3. **拿它跟站上那張卡對照** — 每個檔都連回 `https://secondsource.io/cards/` 的對應頁。判斷與判準兩邊
   應該一樣;結果與更正以站上為準(這裡的同步可能落後)。

*1. Pick any file and read its git history (`git log --follow <file>`) — every change to the
test before its check date is a commit you can read. 2. Pick one whose check date is close and
check the *Source of record* yourself, before we do, then see whether we own the result.
3. Cross-check it against the same call on the site — the call and the test should match; for
results and corrections the site is the record (this mirror may lag).*

## 為什麼有這個東西 / Why this exists

任何人都能在事後說「我早就講過」。事前寫好的判準,加上公開、可比對的版本紀錄,讓「判斷」
和「事後聰明」分得開。我們把這條線畫在自己身上,讓每一次改動都看得到。

*Anyone can say "I called it" afterwards. A test written in advance, plus a public version
history anyone can diff, keeps a judgment apart from hindsight. We are drawing that line on
ourselves, so that every change is visible.*

## 去哪讀全文 / Where to read the full call

**站上是讀的,GitHub 是查的。** 這裡是存證面:判準原文、時戳、可 diff。
站上 `https://secondsource.io/cards/` 是閱讀面:背景、利害關係、白話收據、為什麼這條值得吵。
方法論(我們怎麼做出這些判斷):`https://secondsource.io/methodology/`

*The site is for reading, GitHub is for auditing. This surface carries the text of record, the
timestamps, and a diffable history. The site carries the background, the stakes, and why the
call is worth arguing about. Method: https://secondsource.io/methodology/ (also in English at
https://secondsource.io/en/methodology/).*

## 這裡**沒有**什麼 / What is **not** here

誠實邊界比範圍宣告重要,所以先講沒有的:

- **不是全部的判斷。** 一條判斷要在**還沒開獎時**進來,而且判準經得起照字面結算,才在這裡。
  判準寫得太鬆、天生無法結算、缺必要欄位、還沒檢查過判準能不能照字面結算,或開獎前沒進來的,
  都不在(站上與這裡收錄範圍的差別,見下一段)。進來之後就留著:開獎了,那一檔的狀態列改寫成
  結果與結算日,檔不刪。這個 repo 是判準的公開帳,不是完整檔案庫。
- **沒有任何成績彙總或準確度統計。** 一個數字都沒有——不是因為難看(第一條要 2026-09-01
  才開獎),是因為「展示成績」與「揭露判準」是兩件不同的事,我們在這裡只做後者。
- **沒有推薦、沒有目標價、沒有買賣建議。** 這是產業分析,不是投資建議。
- **判斷句的英文是編輯重寫的,不是機器翻譯的。** 少數新進條目可能暫時只有中文判斷句 +
  完整英文 reference;那種情況檔內會直說,不會假裝。

*What is not here: not every call we make (only calls that came in before they were settled and
whose test can actually be settled as written; once in, a call stays, and when it settles its
status line shows the result and the settlement date); no accuracy figures or performance summaries of any kind; no recommendations, price
targets or buy/sell advice — this is industry analysis, not investment advice; and English
judgment text is editorially rewritten, never machine-translated, so a newly added call may
briefly carry Chinese judgment text with a full English reference section, which the file will
say plainly rather than disguise.*

## 為什麼這裡和站上的清單對不齊 / Why this list and the site's don't match

站上的卡(https://secondsource.io/cards/)與這裡的檔是兩份清單,收錄規則不同:

- **這裡**:只收還沒開獎時進來、判準能照字面結算的判斷(規則見上一段)。判準要靠語意解讀、天生
  無法結算、缺必要欄位、還沒檢查過判準能不能照字面結算,或開獎前沒進來的判斷,不在這裡,照樣在
  站上公開。
- **站上一條判斷有沒有自己的頁**,看它進過卡片列表、或被日報連到過沒有。列表一次列一批:已過查核日
  或已結算的排第一,其次是帶深度解剖的,再其次是查核日最近的;出過的頁不撤。所以這裡有些檔寫著
  「站上還沒有自己的頁」,連到卡片總表。

同一條判斷兩邊都有時,判斷與判準應該一樣;結果與更正以站上為準。

*The cards on the site (https://secondsource.io/cards/) and the files here are two lists with different entry
rules. **Here:** only calls that came in before they were settled and whose test can be settled as
written. Calls whose test turns on interpretation, that can't be settled at all, that are missing a
required field, that haven't yet been checked for whether their test can be settled as written, or
that weren't in before they settled are not here, and are still public on the site. **On the site,**
a call gets its own page once it has been in the card list or linked from a daily issue. The list
shows one batch at a time: calls past their check date or already settled first, then calls with an
in-depth report, then those with the nearest check dates; a page, once published, stays up. That is
why some files here say the call does not have its own page on the site yet and link to the card
index. Where a call is in both places, the call and its test should match; for results and
corrections the site is the record.*

---

本頁僅供對答案時間戳與方法論核驗,不構成績效揭露或招攬。
This page exists to timestamp a call and expose the test that settles it. It is not a performance disclosure and not a solicitation.
