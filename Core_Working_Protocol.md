Bismillah Ar-Rahman Ar-Raheem. Ash-hadu an laa ilaaha illa-LLAH wahdaHu lasharikalaHu, wa ash-hadu anna Muhammadan Abduhu wa Rasooluh. Laa hawla wa laa quwwata illaa biLLAH. Hasbiyallaahu laa ilaaha illaa Huwa, 'alayhi tawakkaltu wa Huwa Rabbul-'Arshil-'Azeem. SubhaanALLAH wa bihamdih, SubhaanALLAHil-'azeem, AlhamduliLLAH, Laa ilaaha illa-ALLAH, wa ALLAHU AKBAR, walaa hawla walaa quwwata illaa biLLAH. Astaghfirullaaha wa atoobu ilayh.



# Core Working Protocol — STRICT COMPLIANCE REQUIRED (v2 — HARDENED)

> **BISMILLAH AR-RAHMAN AR-RAHEEM.**
>
> This document is the **highest-priority operating protocol** for every agent
> (human or AI, main agent or subagent) that touches this repository. It is the
> **root and foundation** of all work. **No work may begin, no tool may be
> invoked, no file may be written, and no commit may be made until this
> protocol has been duly followed.**
>
> *"A tree cannot be planted without a root; likewise no building stands
> without a foundation."* — Without this protocol, every other effort is zero
> (nothing) and will be discarded, bi'idniLlah.

---

## 1. The Invocation (Mandatory Pre-Work & Post-Work Adhkar)

Every thought process, every work generation, every response, every tool-call
batch, and every commit message **MUST begin and end with the following
invocations in full. Nothing may precede the opening invocation; nothing may
follow the closing invocation.**

### 1.1 Canonical Opening Invocation (recite in full before ANY work)

```
Bismillah Ar-Rahman Ar-Raheem.
Ash-hadu an laa ilaaha illa-LLAH wahdaHu lasharikalaHu,
wa ash-hadu anna Muhammadan Abduhu wa Rasooluh.
Laa hawla wa laa quwwata illaa biLLAH.
Hasbiyallaahu laa ilaaha illaa Huwa,
'alayhi tawakkaltu wa Huwa Rabbul-'Arshil-'Azeem.
SubhaanALLAH wa bihamdih, SubhaanALLAHil-'azeem,
AlhamduliLLAH, Laa ilaaha illa-ALLAH, wa ALLAHU AKBAR,
walaa hawla walaa quwwata illaa biLLAH.
Astaghfirullaaha wa atoobu ilayh.
```

### 1.2 Canonical Closing Invocation (recite in full after the work)

The same invocation in full, sealing the work in the name of Allah. Nothing
may come after it in any response or commit message.

### 1.3 Application to Commit Messages (EXACT FORMAT — ENFORCED)

Every git commit message **MUST** begin with the full opening invocation on
the first line(s) and end with the full closing invocation on the last
line(s). **Nothing before, nothing after.** The conventional commit
type/subject sits between the two invocations.

Exact format:

```
Bismillah Ar-Rahman Ar-Raheem. Ash-hadu an laa ilaaha illa-LLAH wahdaHu lasharikalaHu, wa ash-hadu anna Muhammadan Abduhu wa Rasooluh. Laa hawla wa laa quwwata illaa biLLAH. Hasbiyallaahu laa ilaaha illaa Huwa, 'alayhi tawakkaltu wa Huwa Rabbul-'Arshil-'Azeem. SubhaanALLAH wa bihamdih, SubhaanALLAHil-'azeem, AlhamduliLLAH, Laa ilaaha illa-ALLAH, wa ALLAHU AKBAR, walaa hawla walaa quwwata illaa biLLAH. Astaghfirullaaha wa atoobu ilayh.

<type>(<scope>): <short imperative summary>

<body: what changed, why, how it was verified>

Bismillah Ar-Rahman Ar-Raheem. Ash-hadu an laa ilaaha illa-LLAH wahdaHu lasharikalaHu, wa ash-hadu anna Muhammadan Abduhu wa Rasooluh. Laa hawla wa laa quwwata illaa biLLAH. Hasbiyallaahu laa ilaaha illaa Huwa, 'alayhi tawakkaltu wa Huwa Rabbul-'Arshil-'Azeem. SubhaanALLAH wa bihamdih, SubhaanALLAHil-'azeem, AlhamduliLLAH, Laa ilaaha illa-ALLAH, wa ALLAHU AKBAR, walaa hawla walaa quwwata illaa biLLAH. Astaghfirullaaha wa atoobu ilayh.
```

**A commit that violates this format is INVALID and must be amended before
pushing.** This is verified by hash, not by title.

---

## 2. Strict Compliance — Non-Negotiable

- **NO work proceeds without the invocation.** If the invocation is absent,
  the work is considered nullified and must be discarded.
- **NO commit is valid without the invocation wrapping.** A commit without it
  must be amended before pushing.
- **NO response, generation, or tool-call session begins without the opening
  invocation** and ends without the closing invocation.
- **EVERY sub-task and sub-sub-task** must observe this protocol — not only
  top-level tasks.
- **EVERY agent** (subagent, delegated worker, or main agent) must read this
  file in full before performing any action in this repository.
- **Verification is mandatory, not optional.** Any claim of completion must be
  backed by evidence: build output, analyze output, test output, or commit
  hash.

---

## 3. Working Discipline (Engineering Rules)

In addition to the invocation protocol, every agent MUST:

1. **Work only on the default remote branch** (`main` unless explicitly
   instructed otherwise). Do not create feature branches unless the maintainer
   requests it. Push changes to the same remote branch you cloned.
2. **Commit and push after every sub-sub-task milestone** — never wait until
   all sub-tasks are done. Verify each push by **commit hash**, not by commit
   title. A push is only confirmed when `git log <hash>` on the remote (or
   `git ls-remote`) shows that hash.
3. **Run build/analyze before every commit** to ensure no regression is
   introduced. A broken `main` branch is a critical failure.
4. **Battle-test before claiming done.** "Done" means: builds cleanly,
   analyzes with zero errors, runs without crashes on the happy path, and
   satisfies the production-grade bar.
5. **No dummies, mocks, prototypes, or simulations in production code.** Every
   feature must be fully functional and built like a production engineer wrote
   it. Real data, real logic, real storage.
6. **No emojis in UI/UX.** Use Material Icons or proper iconography only.
   Follow the standards set in `docs/PRD.md` and `docs/TODO_TRACKER.md`.
7. **Robust security guardrails.** Input validation, secure storage, no
   hardcoded secrets in source, principle of least privilege, defense in
   depth. Never commit tokens, keystores, or credentials to the repository.
8. **Use absolute paths under `/home/z/my-project/`** for all scripts and
   intermediate artifacts. Final deliverables go in `/home/z/my-project/download/`.
9. **Read `worklog.md` before starting**; append to it after finishing each
   Task ID. Never overwrite prior entries.
10. **Keep the TODO tracker current.** `docs/TODO_TRACKER.md` is the single
    source of truth for progress. Update it in the same commit as the work it
    describes.
11. **Never force-push, never rewrite published history** on `main` unless
    explicitly instructed by the maintainer.
12. **Data integrity for sacred texts.** Qur'an and Hadith text must come from
    verified authentic sources (QUL, open-hadith-data, etc.). Never
    hand-modify revealed text. Compression pipelines must be lossless and
    verified with checksums and round-trip tests.

---

## 4. Protocol Self-Check (Mandatory Before ANY Output)

Before producing any output, every agent MUST verify:

- [ ] Did I recite the opening invocation in full?
- [ ] Is the work I'm about to perform aligned with the task brief?
- [ ] Will my commit message be wrapped with the invocation (open + close)?
- [ ] Have I read `worklog.md` to see what prior agents have done?
- [ ] Will I run build/analyze before committing?
- [ ] Will I push to the default remote branch (`main`)?
- [ ] Will I verify the push by commit hash (not title)?
- [ ] Did I update `docs/TODO_TRACKER.md` alongside the work?
- [ ] Is my work production-grade (no mocks/dummies/simulations)?
- [ ] Am I using proper icons (no emojis) per the UI/UX standard?

If ANY answer is "no", **STOP** and correct course before proceeding.

---

## 5. Definition of Done (Production Gate)

A feature is DONE only when ALL of the following are true:

1. `flutter analyze` reports zero errors (warnings/info addressed or justified).
2. The app builds (`flutter build apk --release` via CI, or `flutter build web`
   locally for visual verification).
3. The feature works on the happy path in a running app (browser-tested via
   Flutter web where applicable).
4. The code is documented where non-obvious, and named clearly.
5. The commit follows the invocation protocol and is pushed and verified by
   hash on `origin/main`.
6. `docs/TODO_TRACKER.md` reflects the new state.

---

## 6. Why This Protocol Exists

This protocol is not a formality. It is the spiritual and operational
foundation of the work. Without it:
- Effort is wasted (work is discarded).
- The build is broken (commits without verification).
- Features are shallow (no production-grade discipline).
- Security is lax (no guardrails).

**WITH this protocol observed strictly, bi'idniLlah, the work is blessed,
the build is green, the APK is signed and released, and the codebase is
production-grade.**

---

*BaarokaLLAHU fee. Bismillah Ar-Rahman Ar-Raheem.*
