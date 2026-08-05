# SecondSource — 公開裁決帳 / Public Verdict Record

SecondSource 是一份追蹤 AI 產業的研究通訊(中/英/日;https://secondsource.io)。這個 repo 是它的
公開存證面:我們對 AI 產業說法做出的判斷,在**開獎之前**就逐條寫死在這裡——每一條都帶
一個開獎日、一組事先講好的判準,以及一個我們自己改不掉的時戳。
*SecondSource is a research newsletter covering the AI industry (https://secondsource.io). This repo is its
public record: calls we make about the AI industry, written down here **before** they can be
settled — each with a settlement date, a test agreed in advance, and a timestamp we cannot edit
after the fact.*

目前 36 條在帳上。｜*36 calls currently on the record.*
官網 / Site: https://secondsource.io

---

## 你正在看的是什麼 / What you're looking at

每一個 `V-YYYY-MM-DD-NN.md` 檔是**一條判斷**。檔裡有:我們的判斷、什麼情況算我們對、
什麼情況算我們錯、哪一天開獎、開獎時要去查哪個來源。中英雙語同檔。

這個 repo 是 append-only 的:檔案進來之後就留著,對的錯的都留著。**每個 commit 的 GitHub
側時間,就是那條判斷「不晚於此刻已經寫下」的第三方證明**——這是這個 repo 存在的唯一理由。
判斷寫在事前才叫判斷,寫在事後叫事後聰明,而兩者的差別只能靠時戳分辨。

*Each `V-YYYY-MM-DD-NN.md` file is one call: what we think, what would count as us being right,
what would count as us being wrong, the date it gets settled, and the source to check on that
date. Chinese and English in the same file. The repo is append-only — calls stay in, right or
wrong. **The GitHub-side commit time on each file is third-party proof that the call was written
down no later than that moment.** A judgment made before the fact and one made after are only
distinguishable by a timestamp; that is what this repo is for.*

## 怎麼用它查我們 / How to audit us

1. **挑任何一個檔,看它的 git 歷史** — `git log --follow V-2026-07-31-01.md`。判準有沒有在
   開獎日之前被動過手腳,你自己看得到,不必問我們。
2. **挑一個開獎日快到的,自己去查** — 檔裡的 *Source of record* 寫的是我們開獎時要查的那個
   來源。你可以比我們先去查,然後看我們認不認帳。
3. **拿它跟站上那張卡對照** — 每個檔都連回 `https://secondsource.io/cards/` 的對應頁。**同一條判斷,
   兩邊講的必須一樣**;不一樣就是我們的問題。

*1. Pick any file and read its git history (`git log --follow <file>`) — you can see for yourself
whether the test was altered before the settlement date. 2. Pick one whose settlement date is
close and check the *Source of record* yourself, before we do, then see whether we own the
result. 3. Cross-check it against the same call on the site — the two must say the same thing.*

## 為什麼有這個東西 / Why this exists

任何人都能在事後說「我早就講過」。事前判準加事前時戳,是「判斷」和「事後聰明」之間唯一
可驗證的分界線。我們把這條線畫在自己身上,而且畫在一個我們沒有寫入權限去改歷史的地方。

*Anyone can say "I called it" afterwards. A test fixed in advance plus a timestamp fixed in
advance is the only verifiable line between a judgment and hindsight. We are drawing that line
on ourselves, in a place where we cannot quietly rewrite the history.*

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

- **不是全部的判斷。** 只有**尚未開獎**且判準經得起機械結算的條目在這裡。判準寫得太鬆、
  無法結算、或已經結案的,都不在。這個 repo 是判準的公開帳,不是完整檔案庫。
- **沒有任何成績彙總或準確度統計。** 一個數字都沒有——不是因為難看(第一條要 2026-09-01
  才開獎),是因為「展示成績」與「揭露判準」是兩件不同的事,我們在這裡只做後者。
- **沒有推薦、沒有目標價、沒有買賣建議。** 這是產業分析,不是投資建議。
- **判斷句的英文是編輯重寫的,不是機器翻譯的。** 少數新進條目可能暫時只有中文判斷句 +
  完整英文 reference;那種情況檔內會直說,不會假裝。

*What is not here: not every call we make (only unsettled ones whose test can actually be
settled); no accuracy figures or performance summaries of any kind; no recommendations, price
targets or buy/sell advice — this is industry analysis, not investment advice; and English
judgment text is editorially rewritten, never machine-translated, so a newly added call may
briefly carry Chinese judgment text with a full English reference section, which the file will
say plainly rather than disguise.*

---

本頁僅供對答案時間戳與方法論核驗,不構成績效揭露或招攬。
This page exists to timestamp a call and expose the test that settles it. It is not a performance disclosure and not a solicitation.
