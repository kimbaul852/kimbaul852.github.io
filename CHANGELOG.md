# 변경 이력 (Changelog)

KEYS — 키보드 피아노의 업데이트 기록입니다. / Update history for KEYS — Keyboard Piano.
형식은 [Keep a Changelog](https://keepachangelog.com/ko/)를 따릅니다. / Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [19] - 2026-06-02
### 추가 / Added
- 🎵 **러닝 코드 모드(Chord Navigator)** — 앱바의 🎹/🎵 토글로 피아노 모드와 전환. ii–V–I 진행·차용·전위를 청음 학습하는 별도 앱을 격리된 iframe(`chord.html`)으로 탑재. 앱바(악보보기·설정·키보드)는 유지, 모드 선택은 자동 저장
  **Chord (러닝 코드) mode** — toggle between piano and the Chord Navigator via the 🎹/🎵 switch in the app bar. The ii–V–I / borrowing / inversion ear-training app is embedded as an isolated iframe (`chord.html`); the top bar (sheet view, settings, keyboard) stays, and the choice is remembered

## [18] - 2026-06-02
### 변경 / Changed
- 🎚️ 피아노 상단 바를 값/라벨 없는 **버튼 묶음**으로 정리: `« ‹ › »` (옥타브/창 이동) + `▲ ▼` (반음 벤딩, 누르는 동안). 모든 모드의 모든 건반에 적용
  Top bar is now a compact **button cluster** (no values/labels): `« ‹ › »` (octave / window shift) + `▲ ▼` (semitone bend, hold). Applies to all keys in every mode

## [17] - 2026-06-02
### 추가 / Added
- 🎚️ 피아노 상단 바에 **옥타브 −/+ 버튼**과 현재 옥타브 표시 추가 — 모든 모드에서 모든 건반을 한 옥타브씩 이동
  Added **octave −/+ buttons** (with current-octave readout) to the piano top bar — shifts all keys by an octave in every mode

## [16] - 2026-06-02
### 변경 / Changed
- 🔁 루프 마디 수 상한을 **8 → 16마디**로 확대
  Raised the loop length limit from **8 → 16 bars**

## [15] - 2026-06-02
### 추가 / Added
- 🎹 **엄지추가 모드** — 확장 모드의 위 피아노(흰 `Q~P` / 검은 `2~0`)만 사용하고, 홈row `A S D F G H J K L ;` 를 **같은 음의 복제 키**로 추가(A=Q, S=W … ;=P). 흰건반에 보조 라벨 표시. 설정의 레이아웃에서 선택
  **Thumb-add mode** — uses only the upper piano (white `Q~P` / black `2~0`) and adds the home row `A S D F G H J K L ;` as **duplicate keys for the same notes** (A=Q, S=W … ;=P), shown as a secondary label on each white key. Selectable in Settings → layout

## [14] - 2026-06-02
### 수정 / Fixed
- 📵 iOS 더블탭 확대 보강 — `touch-action`만으론 남던 확대를, **같은 위치 빠른 두 번째 탭만** JS로 취소(연주·단일 탭은 영향 없음)
  Hardened iOS double-tap zoom blocking — cancels only a quick **second tap at the same spot** in JS (fast playing / single taps unaffected)

## [13] - 2026-06-02
### 변경 / Changed
- ⌨️ 키보드 입력 ON 상태가 **다른 버튼을 눌러도 유지**되도록 — 포커스가 아니라 arm 버튼(또는 토글 키)으로만 꺼짐
  Keyboard-input ON now **stays on when you tap other buttons** — it turns off only via the arm button (or toggle key), not on focus loss

## [12] - 2026-06-02
### 변경 / Changed
- 🧹 메인 화면의 긴 단축키 안내 줄을 제거하고 **"단축키 보기" 버튼 하나**로 정리 (건반 라벨로 충분)
  Removed the long shortcut hint line from the main screen in favor of a single **"Shortcuts" button** (key labels already shown on the keys)
### 수정 / Fixed
- 🔊 다른 앱/탭에 갔다 돌아오면 소리가 안 나던 문제 — 복귀(visibility/focus)·터치 시 **AudioContext 자동 재개**(iOS suspended/interrupted 대응)
  No sound after returning from another app/tab — **AudioContext now auto-resumes** on visibility/focus/touch (handles iOS suspended/interrupted)
- 📵 화면 **더블탭 확대 방지** (`touch-action: manipulation`)
  Prevented **double-tap zoom** on the screen (`touch-action: manipulation`)

## [11] - 2026-06-02
### 변경 / Changed
- ⌨️ 녹음 토글 단축키를 **단독 스페이스 → Ctrl/⌘ + Enter** 두 키 조합으로 변경 (실수 입력 방지, iOS 시스템 단축키와 충돌 없음). 단독 스페이스는 더 이상 녹음을 토글하지 않음. 터치는 하단 REC 버튼 그대로
  Record toggle changed from **lone Space → Ctrl/⌘ + Enter** (prevents accidental triggers, avoids iOS system shortcuts). A lone Space no longer toggles recording; touch still uses the bottom REC button

## [10] - 2026-06-02
### 추가 / Added
- 🎼 **악보 보기 모드** — 악보 이미지를 업로드해 크게 보며 키보드 단축키로 연주 (앱바 악보 아이콘으로 토글)
  **Sheet music view** — upload a sheet image to read it large while playing via keyboard shortcuts (toggle with the sheet icon in the app bar)
  - 악보 모드에서는 온스크린 건반·연주 컨트롤·루퍼 패널을 숨겨 악보에 집중
    In sheet view the on-screen piano, performance controls, and looper panel are hidden to focus on the score
  - 확대/축소(50–300%), 제거 지원. 이미지는 자동 다운스케일 후 별도 키로 저장되어 새로고침해도 유지
    Zoom (50–300%) and remove; the image is auto-downscaled and saved under its own key so it persists across reloads

## [9] - 2026-06-02
### 변경 / Changed
- 🎛️ 연주 컨트롤 정리 — **Volume·Tone만 항상 노출**, Octave/Shift/Transpose는 **접이식 "고급" 패널**로 (기본 접힘)
  Performance controls tidied — **Volume·Tone always visible**; Octave/Shift/Transpose moved into a **collapsible "advanced" panel** (collapsed by default)
- 📱 **하단 고정 트랜스포트 바** — REC/PLAY/STOP을 화면 하단에 고정해 모바일에서 엄지로 누르기 쉽게
  **Fixed bottom transport bar** — REC/PLAY/STOP pinned to the bottom for easy thumb access on mobile

## [8] - 2026-06-02
### 추가 / Added
- 🥁 **퀀타이즈** — 녹음한 음을 1/4·1/8·1/16 그리드에 자동 정렬 (OFF 포함, 비파괴 방식)
  **Quantize** — snap recorded notes to a 1/4·1/8·1/16 grid (incl. OFF, non-destructive)
- ⏱️ **카운트인 ON/OFF + 마디 수(1–4) 선택** (설정 패널)
  **Count-in on/off + bar count (1–4)** selection (settings panel)
- 🎚️ **멀티 트랙(레이어)** — 녹음 패스마다 새 레이어 생성, 트랙별 **음색 전환·음소거·삭제**
  **Multi-track layers** — each recording pass becomes a layer with per-track **tone / mute / delete**
- ⬇ **WAV 내보내기** — 현재 루프(음소거 제외)를 오프라인 렌더링해 keys-loop.wav로 저장
  **WAV export** — offline-renders the current loop (excluding muted tracks) to keys-loop.wav
- ↩ **언두 / ↪ 리두** — 마지막 레이어 되돌리기/복원
  **Undo / Redo** — remove or restore the most recent layer
- 💾 **자동 저장(localStorage)** — BPM·박자·단축키·레이아웃·녹음 레이어를 새로고침 후에도 유지
  **Auto-save (localStorage)** — BPM, time signature, shortcuts, layout, and recorded layers persist across reloads

## [7] - 2026-06-02
### 변경 / Changed
- UI 재배치: 큰 제목/설명을 제거하고 상단 **앱바**(KEYS 브랜드 · 키보드 ON/OFF · 설정)로 정리 (PR #7)
  UI restructure: removed the large heading/description in favor of a top **app bar** (KEYS brand · keyboard on/off · settings) (PR #7)
### 추가 / Added
- ⚙ **설정 패널** — 키보드 레이아웃(기본/확장 2줄)과 단축키 매핑을 한곳에 모음
  ⚙ **Settings panel** — keyboard layout (basic/extended) and shortcut mapping in one place
### 수정 / Fixed
- 모바일에서 루퍼 버튼(메트로놈 등)이 화면 밖으로 넘치던 문제 — 버튼이 줄바꿈되도록 수정
  Looper buttons (e.g. metronome) overflowing off-screen on mobile — now wrap to the next line

## [4] - 2026-06-02
### 변경 / Changed
- 메트로놈이 카운트인 이후에도 **매 박마다 계속 소리**가 나도록 변경 (PR #4)
  Metronome now keeps **clicking on every beat** even after the count-in (PR #4)
  - 메트로놈 소리는 별도 보이스라 **루프 녹음에는 포함되지 않음**
    The metronome uses a separate voice, so it is **never included in the loop recording**
### 추가 / Added
- 🔊/🔇 **메트로놈 ON/OFF 토글 버튼** (기본 ON)
  🔊/🔇 **Metronome on/off toggle button** (on by default)

## [3] - 2026-06-02
### 추가 / Added
- ▶ **PLAY 버튼** — 정지 상태에서 녹음해둔 루프를 카운트인·재녹음 없이 바로 반복 재생 (PR #3)
  ▶ **PLAY button** — replays the recorded loop from a stopped state, with no count-in and no re-recording (PR #3)
  - 재생 중 SPACE를 누르면 그 위에 덧녹음(overdub) 가능
    Press SPACE during playback to overdub on top
  - 녹음된 음이 없거나 재생/녹음 중일 때는 PLAY 버튼 비활성
    PLAY is disabled when nothing is recorded or while playing/recording

## [2] - 2026-06-02
### 추가 / Added
- 🎹 **루프 레코더(looper)** (PR #2)
  🎹 **Loop recorder (looper)** (PR #2)
  - SPACE: 정지 → 메트로놈 카운트인 1마디 → 녹음 → 재생 → 덧녹음(overdub) 순환
    SPACE: stopped → one-bar metronome count-in → record → play → overdub, cycling
  - 카운트인만 메트로놈 소리, 이후 비트는 시각적 점으로 깜박(첫 박 강조)
    Metronome sounds only during count-in; afterwards the beat blinks visually (downbeat accented)
  - 피아노 연주음만 루프에 기록 (메트로놈 미포함, 재생음은 별도 보이스로 재녹음 안 됨)
    Only your piano notes are recorded into the loop (metronome excluded; playback uses separate voices so it is never re-recorded)
  - 노트 타이밍을 박(beat) 단위로 저장 → BPM을 바꿔도 자연스럽게 따라감
    Note timing is stored in beats, so changing the BPM rescales playback naturally
  - 컨트롤: BPM(40–240), 마디 BARS(1–8), 박자 BEAT(2–8), STOP / CLEAR
    Controls: BPM (40–240), bars (1–8), beats per bar (2–8), STOP / CLEAR
  - 키보드·마우스·터치 연주 모두 녹음
    Records playing from keyboard, mouse, and touch

## [1] - 2026-06-02
### 추가 / 변경 · Added / Changed
- KEYS 키보드 피아노 전면 개편 (PR #1)
  Full overhaul of the KEYS keyboard piano (PR #1)
  - **기본 모드**(1줄) + **확장 2줄 모드** 토글
    **Basic mode** (single row) + **extended two-row mode** toggle
  - **피치 벤드** (키를 누르는 동안 반음 휘어짐)
    **Pitch bend** (bends a semitone while the key is held)
  - 옥타브 / 창(window) 이동, 트랜스포즈
    Octave / window shifting, transpose
  - 음색 선택 (GRAND / ELEC / SYNTH)
    Tone selection (GRAND / ELEC / SYNTH)
  - 단축키 리매핑 모달, 키보드 입력 ON/OFF 토글
    Shortcut-remapping modal, keyboard-input on/off toggle
  - PWA 메타데이터 (모바일 홈 화면 추가 지원)
    PWA metadata (supports adding to the mobile home screen)

## [0] - 2026-05-28
- 최초 파일 업로드 / Initial file upload
