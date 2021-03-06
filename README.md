# slack-juggler

슬랙에서 비서 노릇하는 봇 입니다. *— 비서를 비하한 건 아닙니다. 봇 비하입니다.*  
KBS 드라마 `저글러스`의 의미를 빌려 비서를 비유적으로 표현했습니다.
> Jugglers!  
  양손과 양발로 수십 가지 일을 하면서도 보스의 가려운 부분을 긁어줄 줄 아는 저글링 능력자 언니들을 아는가?  
  어디선가, 보스에게, 무슨 일이 생기면 반드시 나타나는 오피스 히로인즈!  
  그 이름하야, 저글러스!
  
## Features

현재 만들어진 기능은 다음과 같아요 *— 언제든지 pullRequest는 환영입니다*  

### `JiraInformationService`
대화내용에 이슈번호를 찾아 이슈의 기본적인 정보를 제공합니다

### `PlantUmlService`
`plantuml` 기능을 사용해 대화내용에 plantuml 구문을 인식하여 UML을 만들어 줍니다

### coming soon

## How to use it?
### Add slack bot in user workspace.
* [Bots](https://slack.com/apps/A0F7YS25R-bots)를 사용하고자 하는 워크스페이스에 설치하세요

### Edit properties
* `src/main/resources`에 위치한 `application.yml.dist` 를 참고하여 `application.yml`를 만드세요
* `api token`정보를 `application.yml`의 `slack.config.token` 정보을 넣으세요

### Work on slack! Enjoy slack-juggler's features!

### Customize
* `config/SlackConfig` 에서 봇의 모양을 바꿀 수 있어요
* 나만의 추가 기능을 구현하고자 하는 경우 `JugglerService`를 상속받아 `isTrigger()`와 `execute()` 를 구현하고
  `io.kindler.slack.listener`의 알맞은 이벤트 리스너에 등록하세요

## Thanks for ... (depend on)
 * SpringBoot [site](https://projects.spring.io/spring-boot/)
 * lombok [site](https://projectlombok.org/) [repository](https://github.com/rzwitserloot/lombok)
 * simple-slack-api [repository](https://github.com/Ullink/simple-slack-api)