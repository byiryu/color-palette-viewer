# weather-outfit (PALETI) — 디자인 프리뷰 (로컬)

⚠️ **이 디렉토리는 출시 전까지 로컬에만 보관됩니다.** push 금지. 출시 시(M6/M7) `byiryu-studio-previews/weather-outfit/design/` 으로 이전.

워크플로우 마스터: `_docs/workflow.md` 섹션 8 (시각화 자료 정책)

---

## 포함 파일

| 파일 | 내용 |
|------|------|
| `index.html` | 로컬 인덱스 (4개 시각화 링크) |
| `design-system.html` | 토큰 시각화 — 컬러·타이포·스페이싱·라디우스·elevation·시스템 컬러 |
| `components.html` | 컴포넌트 카탈로그 — 버튼·카드·칩·input·태그 (Light/Dark) |
| `prototype.html` | 인터랙티브 프로토타입 — 8 화면 클릭 전환 |
| `widgets.html` | 위젯 시각화 — iOS Lock/Home(소·중) + Android Glance(소·중) |

## 로컬 보기 방법

### 방법 1: Python http.server (권장)
```bash
cd /Users/kj/Desktop/ApplicationProject/scripts/weather-outfit/design-preview
python3 -m http.server 8000
```
브라우저: http://localhost:8000

### 방법 2: 직접 파일 열기
```bash
open index.html
```
> ⚠️ `file://` 프로토콜로 열면 일부 브라우저에서 fetch·module 동작 X. 가급적 http.server 사용.

### 방법 3: VSCode Live Server 확장
- `index.html` 우클릭 → "Open with Live Server"

---

## 토큰 출처

`_docs/design-briefs/weather-outfit/design-system.md` 의 토큰을 그대로 적용.
컬러는 **Y1 (Warm Minimal 인디고) 잠정** — 출시 전 재검토 또는 출시 후 사용자 반응 보고 조정.

---

## 출시 시점 이전 절차 (M6 직전 또는 직후)

1. **이 디렉토리 전체를 viewer 레포로 복사:**
   ```bash
   cp -r /Users/kj/Desktop/ApplicationProject/scripts/weather-outfit/design-preview/* \
         /tmp/byiryu-studio-previews/weather-outfit/design/
   ```

2. **viewer 레포 커밋·푸시:**
   ```bash
   cd /tmp/byiryu-studio-previews
   git add weather-outfit/design/
   git -c user.name="byiryu" -c user.email="byiryustudio@gmail.com" \
       commit -m "release: weather-outfit (PALETI) v1.0 design preview"
   git push origin main
   ```

3. **프로젝트 인덱스 갱신:**
   - `byiryu-studio-previews/weather-outfit/index.html` — design 링크 활성화 (비활성 → 활성)
   - 루트 `byiryu-studio-previews/index.html` — PALETI 카드 status "released" 로 변경

4. **brief.md 시각화 이력 표 갱신:**
   - 4개 design 행: 🔒 로컬 (예정) → ✅ 공개 + URL 갱신

5. **공개 URL 확인:**
   - https://byiryu.github.io/byiryu-studio-previews/weather-outfit/design/

---

## 변경 이력

| 일자 | 변경 |
|------|------|
| 2026-05-11 | 초안 — 4 HTML 빌드, Y1(인디고) 잠정 토큰 적용. 로컬 보관 |
