# 시작하기 — 내 Supabase 로 독립 운영 (build-2611-13)

이 묶음은 **내 Supabase 프로젝트 값이 이미 들어 있는 판**입니다. 카카오 로그인은 빼고 이메일 가입만 씁니다.

- Project URL: `https://trimmmnkwsyajzdcadih.supabase.co`
- 키: Publishable(공개용) 키가 `js/auth-config.js` 에 들어 있습니다.

## 남은 일은 네 가지입니다

1. **SQL 세 개 실행** — Supabase 의 「SQL Editor」에서 `supabase/auth.sql` → `supabase/board.sql` → `supabase/site.sql` 순서로 내용을 붙여 넣고 Run. 여러 번 실행해도 안전합니다. `supabase/verify.sql` 로 결과를 확인할 수 있습니다(표 이름은 모두 `build261113_` 로 시작).
2. **주소 등록** — 「Authentication → URL Configuration」의 Site URL 과 Redirect URLs 에 내 사이트 주소를 넣습니다. 예: `https://내아이디.github.io/build-2611-13/` 과 `https://내아이디.github.io/build-2611-13/**`
   - 「Authentication → Sign In / Providers → Email」의 「Confirm email」을 꺼 두면 가입 뒤 바로 로그인됩니다. 켜 두면 메일의 확인 링크를 눌러야 합니다.
3. **내 깃허브에 올리기** — 새 저장소를 만들고 이 폴더의 파일을 모두 올린 뒤 「Settings → Pages」에서 `main` · `/ (root)` 를 고릅니다.
4. **첫 관리자 되기** — 내 사이트에서 「시작하기」로 가입하고 로그인하면 「첫 관리자 되기」 단추가 보입니다(관리자가 한 명도 없을 때만). 그 뒤 동료가 가입하면 「관리」에서 승인합니다.

## 알아 둘 것

- 업무 자료는 지금처럼 쓰는 사람의 브라우저에만 저장됩니다. Supabase 에는 「누가 쓸 수 있는가」와 게시판 글만 있습니다.
- 과정 중에 쓰던 주소(`https://build-2611-13.jobability.co.kr/`)의 가입 정보는 넘어오지 않습니다. 새 주소에서 다시 가입합니다.
- 카카오 로그인을 쓰려면 카카오 개발자 설정과 Supabase 의 Kakao Provider 설정이 따로 필요합니다. 설정한 뒤 `js/auth-config.js` 의 `kakao` 를 `true` 로 바꿉니다.
- **secret · service_role 키, DB 비밀번호는 어디에도 넣지 않습니다.** 이 도구는 공개용 키만 씁니다.
- 자세한 안내: `docs/내_깃허브로_옮기기.md` · `supabase/README.md`
