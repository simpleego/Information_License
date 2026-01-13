🙂 XrML은 XML 기반 언어라서 실제 문서 형태는 **태그 구조**로 되어 있습니다.  
간단한 예시를 들어, 어떤 전자책을 특정 사용자만 읽을 수 있도록 권한을 표현하는 XrML 문서를 보여드릴게요.

---

## 📄 XrML 예시

```xml
<?xml version="1.0"?>
<license xmlns="http://www.xrml.org/schema">
  <grant>
    <!-- 누구에게 권한을 주는지 -->
    <principal>
      <name>User123</name>
    </principal>

    <!-- 어떤 리소스에 대한 권한인지 -->
    <resource>
      <name>ebook_ABC.pdf</name>
    </resource>

    <!-- 어떤 권한을 주는지 -->
    <right>read</right>

    <!-- 권한의 조건 -->
    <condition>
      <validity>
        <start>2026-01-01</start>
        <end>2026-12-31</end>
      </validity>
    </condition>
  </grant>
</license>
```

---

## 🧾 설명
- `<principal>`: 권한을 받는 주체(사용자, 그룹 등)  
- `<resource>`: 권한이 적용되는 대상(전자책, 음악 파일 등)  
- `<right>`: 허용되는 행위(읽기, 복사, 인쇄 등)  
- `<condition>`: 권한의 조건(기간 제한, 횟수 제한 등)  

---

👉 위 예시는 “User123이 ebook_ABC.pdf 파일을 2026년 1월 1일부터 12월 31일까지 읽을 수 있다”라는 규칙을 표현한 것입니다.  
실제 DRM 시스템에서는 이런 XrML 문서를 기반으로 콘텐츠 접근을 제어합니다.  
