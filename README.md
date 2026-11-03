# Examulator

Free practice-exam program for ISC2, ISACA, CompTIA and EC-Council certifications, by
Certification Tool and Die, Ltd. Examulator delivers practice exams in linear and computerized
adaptive (CAT) modes, scores them and tracks your readiness by domain.

This repository holds the program downloads. Question pools are published separately: the app
downloads them for you (Select Exam), or see
[ctdltd/Examulator-Pools-v2](https://github.com/ctdltd/Examulator-Pools-v2).

## Downloads

Get the files from the [latest release](https://github.com/ctdltd/Examulator/releases/latest).

| File | For |
|---|---|
| `Examulator-Program-win_x64-{version}.zip` | Windows 10/11 (x64; also runs on Windows on Arm) |
| `Examulator-Program-osx_arm64-{version}.zip` | macOS on Apple Silicon |
| `Examulator-Program-osx_x64-{version}.zip` | macOS on Intel |
| `Examulator-Program-linux_x64-{version}.zip` | Linux (x64) |
| `Examulator-{version}.apk` | Android, for side-loading (the same app is on Google Play) |
| `Examulator-Diagnostics-{platform}-{version}.zip` | Support tool for reading diagnostic exports (not needed to use the app) |
| `SHA256SUMS.txt` | Checksums for every file in the release |

## Installing

- **PC:** unzip the program zip into a folder of your choice and run `Examulator` (Windows:
  `Examulator.exe`). It opens in your web browser. Your results and question pools are kept in your
  user profile, so installing a newer version into a new folder keeps them.
- **Updates:** the app tells you when a newer version is available and can install it for you.
- **Android:** install from Google Play, or allow installs from unknown sources and open the APK.

## Checking a download

Compare the file's SHA-256 with `SHA256SUMS.txt` (GitHub also shows each file's SHA-256 on the
release page):

- Windows (PowerShell): `Get-FileHash .\Examulator-Program-win_x64-....zip -Algorithm SHA256`
- macOS / Linux: `shasum -a 256 Examulator-Program-....zip`

## Versions

Versions are `YYDDD.HHmmss`: the year and day of the year, then the time of the release
(26304.153000 = 31 October 2026, 15:30:00). Releases up to 26300.01 used `YYDDD.VV` instead.

## Changelog

Newest first.

<!-- changelog -->

### 26306.1521 - 2026-11-02

**Programs:** Examulator (PC) · Examulator (Android) · Examulator3 (PC) · Examulator3 (Android) · Examulator Diagnostics

- Examulator3, the next generation of Examulator, is now available for testing: the PC program for Windows, Linux and macOS, and the Android app as an APK for side-loading. It installs alongside Examulator and keeps its own exams and results.
- Program and question-bank updates now download from the public GitHub releases first, with Google Drive as a fallback. Every download is still checked against a published checksum.
- New version numbers: a release is numbered by the date and time it was published.
- The question review after an exam labels every answer A to D, as in the exam, and the answers you didn't pick no longer blend in with the explanations.
- Question banks updated more than once a day are offered as updates, and a question bank copied by hand into the program's data folder is installed at the next start if it is newer.
- A question bank meant for the other generation of Examulator is refused with a clear message instead of loading with blank explanations.
- Help and the Select Exam screen now explain installing exams from inside the app.

### 26300.01 - 2026-10-27

- Question pool updates published under the newer, longer revision numbers appear in the update list again (the previous release skipped them).
- The PC diagnostic tool finds the app's data again without extra options.
- Internal restructuring; no other visible changes.

### 26298.01 - 2026-10-25

- PC: your results and question pools now live in your user profile. Existing data is copied (never moved) and checked on first start before it is used.
- Timed-out Linear exams are now scored, with unanswered questions counted as wrong. CAT results now appear in the Score Progression and Readiness reports, and ability estimates are more accurate.
- Question pool and program downloads without a published checksum are now refused instead of being installed unchecked.
- Android: the update prompt no longer loops and the restart waits for you and for the exam to end; the exam clock stops while the abort dialog is open or the app is in the background; starting a new exam asks before discarding one in progress; leaving a page cancels its download.
- PDF export works again.
- Faster question selection, plus reliability and security improvements to the PC app and the updater.

### 26297.01 - 2026-10-24

- New: when ExamAdvantage is installed, the results and history review screens show "Study these topics" and per-question "Study" links that open the matching ExamAdvantage topic.
- New: Objective Practice. ExamAdvantage can open a focused practice set of 5 to 50 questions on one objective, and Examulator downloads the question pool automatically if it is missing.
- New (beta, phone app): the interface in seven languages (Chinese Simplified, Spanish, Japanese, German, Portuguese Brazil, French, Korean), and optional question translation using Apple's on-device translation (iOS 26 and later) or your own Google or Microsoft Azure key. The default is "Menus only", which leaves questions in English.
- Exam editions: different editions of an exam (for example CISSP 2024 and CISSP 2027) can be installed side by side, each with its own history. Existing pools and results are upgraded automatically.
- Update checks list the download folders directly and verify downloads, and the app reads the new compact question pools, about a quarter of the size. A "Rate Examulator" link was added to Help > Support on the phone app.
- Fixed a "no such column: uploadedAt" error in History and Upload on older results databases.

### 26286.01 - 2026-10-13

- Fixed "All Domains" quizzes including unscored pretest questions.
- Quizzes covering more than one domain now follow the exam outline's domain weights instead of how the question bank happens to be built. If a domain runs short, the quiz is topped up from the other selected domains.
- Fixed domain weights stored with a "%" sign being treated as zero, which dropped that domain from exams and quizzes.

### 26284.01 - 2026-10-11

- Fixed "Install Update" failing on Windows with a "file is being used by another process" error when installing or updating a question pool.
- The installer now retries briefly if another program, such as antivirus or a search indexer, is briefly using the file.

### 26283.01 - 2026-10-10

- Fixed ISACA quizzes showing a score above the maximum (for example 920/800). ISACA quizzes now use the 200 to 800 scale with the 450 pass line; already recorded results keep their stored score.
- Installed exam cards on Select Exam now show the installed question pool version.
- Phone app: when a newer pool is available, the exam card shows "Update available" and a long-press installs the update in the app.

### 26281.03 - 2026-10-08

- Android: the app icon shows the Examulator logo again instead of a generic "E".
- The "Question Bank Updates" dialog at launch now installs updates inside the app instead of opening a Google sign-in page or reporting an unsupported file type.
- Android: Google Play in-app update prompts.

### 26281.02 - 2026-10-08

- New Support section in Help listing the ways to reach us: Reddit message to u/mikedn02908, the r/ctdltd subreddit, or support@certificationtoolanddie.com, with tips on what to include in a bug report.
- PC: the separate bug-report FAQ entry was merged into the Support section.

### 26281.01 - 2026-10-08

- Android: fixed "File picker error: This platform does not support this file type" when importing an exam database from a file.
- ISACA exam databases are now accepted on import.
- Finished updating the remaining help text and messages to the ISC2 name.
- Build optimizations for Google Play.

### 26280.01 - 2026-10-07

- First production release.
- ISACA exams are supported (CISM, CISA, CRISC, CDPSE, CGEIT, CCOA, AAIA, AAIR, AAISM, plus CCA and CCP), with ISC2 and ISACA tabs on Select Exam. ISACA exams are Linear only and scored on a 200 to 800 scale with a 450 pass line, an approximation noted in results and reports.
- Difficulty levels are standardized to four bands for all exams: Easy, Moderate, Difficult and Expert. The quiz difficulty filter now has four options; scoring is unchanged.
- The app now uses ISC2's current name throughout, and Select Exam shows a trademark notice.
- PC: fixed Help sections not expanding, and fixed the install and update buttons missing on Select Exam.

### 26274.01-rc1 - 2026-10-01

- iOS: fixed a crash on launch on iOS 27.
- iOS: fixes to app icons, version number and splash screen for the App Store.

### 26272.01-rc1 - 2026-09-29

- Fixed the CAT Ability Trajectory report showing no CAT sessions, and other reports wrongly saying "not enough data" for users who mostly take CAT exams.
- PC: the Exam History row menu now stays on screen when the page is scrolled.
- CPE Report: fixed the missing recipient name on Android and the report not generating on Windows.
- New: the update screens show what has changed since your version before you install.

### 26258.02-rc1 - 2026-09-15

- New report: CAT Ability Trajectory, which plots your ability estimate and its confidence range question by question through a CAT session.
- New report: CPE Report, a PDF certificate of study time for CPE credit submissions.
- Twelve named color themes in Accessibility settings, with readability fixes for the light theme and dropdown lists. PC: fixed theme selection having no visible effect.
- Fixed an error when opening the quiz configuration screen.
- Program update downloads can be verified against a published checksum.
- Android: the top bar no longer sits behind the status bar on edge-to-edge devices, and taps respond without delay.

### 26247.01-rc1 - 2026-09-04

- Android: fixed the app showing a generic system icon on some launchers.
- Early groundwork for an iOS version.

### 26232.01-rc1 - 2026-08-20

- New Raw Question Review report (Study Tools): review questions from several sessions, filtered by answered correctly, answered incorrectly or flagged for review, with PDF export.
- Released to Google Play Early Access (open testing).
- Internal build fixes.

### 26228.01-closed - 2026-08-16

- New: Contribute Results, an optional, opt-in way to send anonymous result data that helps refine question difficulty. It is off by default.
- New Accessibility settings: themes, font size, reading fonts, reduced motion, stronger focus outlines, hide timer, larger tap targets, extended time (1.5x or 2x, with the score marked as not comparable), and notes on flagged questions. Screen reader support improved, including data tables for report charts.
- New Reports: Single Exam Report, Domain Trends and Comprehensive Analysis, with interactive charts and PDF export. Exam History is now reached from the Reports catalog.
- Row menus on the Single Exam Report screen and the session detail view offer View, Export PDF, Delete and Export diagnostic.
- The splash screen shows the build time, PC Help sections can be collapsed, wide screens get a two-column splash layout, and text contrast is improved.
- Many bug fixes.

### 26226.01-closed - 2026-08-14

- Export a diagnostic file for any session from Exam History (on Android through the share sheet).
- Exam History rows have a menu with View, Print, Delete and Export diagnostic.
- New print preview page, with the option to leave out the question review. On Android it uses the system print service, including Save as PDF.
- Abort Exam: click or tap the exam name during an exam to discard it. The timer pauses while the dialog is open.
- PC: the browser now asks before leaving an exam through Back, closing the tab or refreshing, and no longer shows that warning wrongly when clicking Next in a timed quiz.

### 26223.02-closed - 2026-08-11

- Android: fixed the Abandon Exam button not responding.
- The splash screen shows the version number.
- Corrected the Help, About and FAQ wording on data sharing and on how CAT mode compares with the real exams.

### 26220.06-alpha - 2026-08-08

- Fixed the quiz question history filter when unanswered and answered questions are selected together.
- Internal improvements.

### 26216.02-alpha - 2026-08-04

- Quiz difficulty filter to limit questions to selected difficulty levels.
- Question history filters: unanswered only, include incorrect, include correct, include marked for review.
- Android: the question count is now set with a slider in steps of 5.

### 26216.01-alpha - 2026-08-04

- Exam History detail page: tap a session to review it question by question, with answers and explanations.
- Android: an exam in progress is saved after every answer and restored if the app is closed.

### 26182.01-alpha - 2026-07-01

- New CAT mode: an adaptive exam that adjusts to your answers and ends when your result is clear, the question limit is reached or time runs out.
- New Linear mode: questions drawn across domains by the published exam weights, balanced by difficulty.

### 26167.01-alpha - 2026-06-16

- New Quiz mode, untimed or timed, with immediate answer reveal, Mark for Review, feedback flags and going back through answered questions.
- Download and install exam question pools from inside the app, with progress shown, on PC and Android.

### 26160.01-alpha - 2026-06-09

- First Android version of the app.
- The Android app shares its screens with the PC app.

### 26155.01-alpha - 2026-06-04

- Initial alpha release of the PC app: choose an exam and a mode (CAT, Linear or Quiz) and take the exam.
- Results screen and Exam History, with scoring based on Item Response Theory.
