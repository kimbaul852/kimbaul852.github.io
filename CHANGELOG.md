# 변경 이력 (Changelog)

KEYS — 키보드 피아노의 업데이트 기록입니다. / Update history for KEYS — Keyboard Piano.
형식은 [Keep a Changelog](https://keepachangelog.com/ko/)를 따릅니다. / Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

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
