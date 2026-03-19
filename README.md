# AgeOfWarUpdateInfo

게임 **Age of War**의 업데이트 공지 서버입니다.

## 구조

- `update.json` — 패치노트 데이터
- `index.html` — 웹 패치노트 페이지 (GitHub Pages)

## 흐름
```
플레이어 버튼 클릭
→ LocalScript → RemoteFunction → ServerScript
→ HttpService로 update.json fetch
→ 데이터 클라이언트에 반환 → UI 렌더링
```

웹 페이지는 roproxy.com을 통해 Roblox 썸네일 API를 호출합니다.

## update.json 수정 방법

`update.json`을 수정하고 push하면 게임과 웹 페이지에 즉시 반영됩니다.
```json
{
    "version": "v0.0.1",
    "date": "2025-03-19",
    "critical": false,
    "blocks": [
        { "type": "title", "text": "섹션 제목" },
        {
            "type": "card",
            "image": "rbxassetid://...",
            "title": "카드 제목",
            "subtitle": "신규 유닛!",
            "description": "설명"
        }
    ]
}
```

## 웹

https://mn556112.github.io/AgeOfWarUpdateInfo/
