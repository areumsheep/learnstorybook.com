---
title: '결론'
tocTitle: '결론'
description: '시각적 버그에 안녕을'
---

개발자들은 [21%](https://ieeexplore.ieee.org/document/895984)의 시간을 버그를 고치는 데 쓴다고 합니다. UI 겉모습을 디버깅하는 건 특히 좌절스럽습니다. 재현하려면 서로 다른 브라우저 사이를 왔다갔다 해야하고, 앱을 올바른 상태로 만들고, DOM 사이를 터덜터덜 돌아다녀야 합니다. 걸린 이득과 손실도 큰데- QA에서 잡히지 않은 버그를 수정하는 비용은 프로덕션에서 [5-10x](https://www.cs.umd.edu/projects/SoftEng/ESEG/papers/82.78.pdf)배는 더 오랜 시간이 걸린다고 합니다.
<!--
Developers spend [21%](https://ieeexplore.ieee.org/document/895984) of their time fixing bugs. Debugging UI appearance can be especially frustrating. Reproductions require you to spin up different browsers, get your app into the right state, and trudge through DOM. The stakes are higher too; uncaught bugs cost [5-10x](https://www.cs.umd.edu/projects/SoftEng/ESEG/papers/82.78.pdf) more time to fix in production than in QA.
-->

수 천 프런트엔드 팀들이 스토리북을 이용해 시각적 테스트를 한다는 건 이제 상식입니다. 스토리북은 컴포넌트를 **구축**할 뿐만 아니라, **시각적 테스트**를 작성하게 도와줍니다. 컴포넌트 수준에서 테스트한다면 버그의 근본 원인을 집어낼 수 있을 겁니다. 이미지 스냅샷을 찍으면 **회귀 에러**를 자동으로 잡을 수 있게 도와줍니다. UI를 몰래 끼어든 버그들을 걱정할 필요 없이 전달할 수 있게 됩니다.
<!--
It's common sense then that thousands of frontend teams visual test using Storybook. Storybook helps you **build** components and write **visual tests**. Running tests at the component level allows you to pinpoint the root cause of a bug. Taking image snapshots helps you catch **regressions** automatically. That means folks can ship UIs without worrying about stowaway bugs.
-->

이 가이드를 통해 시각적 테스팅의 기본을 소개했습니다. Tom과 나는 여러분이 이번에 배운 걸 이용해 자신만의 프로젝트를 만들어보길 희망합니다. Storybook 메일링 리스트에 가입하셔서 더 유용한 글과 가이드 소식을 받아보세요.
<!--
This guide introduced you to the basics of visual testing. Tom and I hope you can build upon these learnings in your own projects. Join the Storybook mailing list to get notified of more helpful articles and guides like this.
-->

<!--
<iframe style="height:400px;width:100%;max-width:800px;margin:0px auto;" src="https://upscri.be/d42fc0?as_embed"></iframe>
-->

<!--
## Sample code for this tutorial
-->
## 이 튜토리얼의 예시 코드

지금까지 잘 따라왔다면, 당신의 저장소와 배포한 스토리북은 다음과 같이 보여야 합니다.
<!-- 
If you've been following along, your repository and deployed Storybook should look like this:
-->

- 📕 [**GitHub repository**](https://github.com/chromaui/learnstorybook-visual-testing-code)
- 🌎 [**Deployed Storybook**](https://6070d9288779ab00214a9831-oymqxvbejc.chromatic.com/?path=/story/commentlist--paginated)

## 더 많은 자료

더 깊게 빠져들길 원하나요? 여기 몇몇 유용한 추가 자료들이 있습니다.
<!--
Want to dive deeper? Here are some additional helpful resources:
-->
- [**Official Storybook docs**](https://storybook.js.org/docs/react/get-started/introduction) 에는 API 문서와, 예시들, 그리고 애드온 갤러리가 있습니다.
- [**How to actually test UIs**](https://storybook.js.org/blog/how-to-actually-test-uis/) 에서는 Shopify, Adobe, Twilio와 같은 회사들이 사용하는 실용적인 UI 테스팅 전략을 요약했습니다. 

- [**Discord chat**](https://discord.gg/UUt2PJb) 스토리북 커뮤니티와 메인테이너들과 연락을 유지하세요.

- [**Blog**](https://medium.com/storybookjs) 최신 릴리즈와 기능들을 보여주고, 당신의 UI 개발 작업흐름을 최신으로 유지하게 도와줍니다.

<!--
- [**Official Storybook docs**](https://storybook.js.org/docs/react/get-started/introduction) has API documentation, examples, and the addon gallery.
- [**How to actually test UIs**](https://storybook.js.org/blog/how-to-actually-test-uis/) is a summary of practical UI testing strategies from Shopify, Adobe, Twilio, and more.

- [**Discord chat**](https://discord.gg/UUt2PJb) puts you in contact with the Storybook community and maintainers.

- [**Blog**](https://medium.com/storybookjs) showcases the latest releases and features to streamline your UI development workflow.
-->
