# ikakao-images

[ikakao.kr](https://www.ikakao.kr) 본문 이미지 호스팅용 저장소.

Blogger 에디터에 이미지를 올리는 대신 여기에 커밋하고 글에서 URL 로 참조한다.
Blogger 업로드는 원본 파일명과 크기를 보존하지 않고, 글을 지우면 이미지도 같이
사라진다. 여기 두면 파일이 어느 글에 붙은 것인지 경로로 남는다.

## 경로 규칙

```
posts/{slug}/{name}.{ext}
```

`{slug}` 는 블로그 저장소의 `_workspace/posts/{lang}/{category}/{slug}.md` 와 같은 값을 쓴다.
글 하나의 이미지는 반드시 그 글의 slug 폴더 안에 둔다.

## 참조 URL

```
https://raw.githubusercontent.com/goldtagworks/ikakao-images/main/posts/{slug}/{name}.png
```

마크다운 본문에서는 이렇게 쓴다.

```markdown
![대체 텍스트](https://raw.githubusercontent.com/goldtagworks/ikakao-images/main/posts/{slug}/{name}.png)
```

## 파일 규칙

- 파일명은 영문 kebab-case. 한글·공백·대문자를 쓰지 않는다 (URL 인코딩이 붙는다)
- 스크린샷은 PNG, 사진은 JPG, 도식은 가능하면 SVG
- 가로 1600px 을 넘기지 않는다. 본문 폭이 그보다 좁다
- 원본이 필요하면 같은 폴더에 `{name}-original.{ext}` 로 같이 둔다

## 넣지 않는 것

- 개인 식별 정보가 찍힌 스크린샷 (계정 이메일, 토큰, 실명, 사내 URL)
- 회사 내부 화면
- 라이선스가 불분명한 남의 이미지

이 저장소는 public 이다. 올리는 순간 되돌릴 수 없다고 보고 넣는다.
