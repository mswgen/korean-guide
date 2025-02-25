# Discord 봇 애플리케이션 만들기

## 봇 만들기

Node와 discord.js를 설치했고, 필요하다면 린터까지 설치하셨으면, 코딩할 준비가 거의 끝났어요! 다음 단계는 Discord 사이트에서 봇 애플리케이션을 만드는 것입니다.

만드는 것은 쉽습니다. 아래에 나온 것만 하면 끝이에요.

1. [Dicsord 개발자 포털](https://discord.com/developers/applications)을 열고 로그인합니다.
2. "New Application" 버튼을 클릭합니다.
3. 모달이 뜨면 봇 이름을 입력하고 "Create" 버튼을 클릭합니다.

아래와 같은 페이지를 보게 될 거에요:

![애플리케이션을 성공적으로 만들었어요.](./images/create-app.png)

여기서 봇의 이름, 아바타, 그리고 프로필에 "내 소개"에 뜰 내용을 설정할 수 있어요. 변경 사항을 저장했으면 왼쪽에서 Bot을 클릭해주세요.

![봇 만들기 UI](./images/create-bot.png)

오른쪽 위에 있는 "Add Bot" 버튼을 클릭한 다음 뜨는 모달에서 "Yes, do it!"을 누릅니다. 축하드려요! 방금 막 만들어진 봇의 자랑스러운 주인이 됐어요! 물론 아직 다 끝난 건 아니에요.

## 봇 토큰

::: danger
이 부분은 중요하므로 잘 보십시오. 여기서는 봇 토큰에 대한 설명과 봇 토큰의 보안 관련 내용을 설명합니다.
:::

봇을 만드면 아래와 같은 화면을 보게 됩니다:

![봇 애플리케이션](./images/created-bot.png)

여기에서 봇의 아바타, 닉네임을 설정할 수 있고 공개 여부를 설정할 수 있어요. 여기에서 봇의 토큰도 "Click to reveal"을 누르거나 "Copy"를 눌러서 얻을 수 있어요. 이 토큰을 어딘가에 복사하라고 하면 이 값을 사용하면 돼요. 언제든지 이 페이지에서 토큰을 다시 복사할 수 있으니 토큰을 잃어버렸다고 걱정하지 마세요.

### 그래서 토큰이 뭐죠?

토큰은 봇의 비밀번호입니다. 즉, 봇이 Discord에 로그인하는 데 사용하는 값입니다. 그러니, **절대 누구에게도 토큰을 일부로든 실수로든 어떤 이유로든 공유하지 마세요!**. 누군가가 봇 토큰을 얻게 되면, 그들이 이 봇으로 이상한 걸 할 수 있어요.

토큰은 이렇게 생겼어요: `NzkyNzE1NDU0MTk2MDg4ODQy.X-hvzA.Ovy4MCQywSkoMRRclStW4xAYK7I` (걱정 마세요. 여기에 토큰을 올리면서 토큰을 바꿨어요). 길이가 좀 더 짧고 이런 식이라면: `kxbsDRU5UfAaiO7ar9GFMHSlmTwYaIYn`, 토큰 말고 client secret을 복사했어요. 봇을 돌리고 싶다면 꼭 토큰을 복사하세요!

### 토큰이 유출된다면?

1000개 이상의 서버에 들어가 있는 봇을 소유하고 있는데 이렇게 되는 데 오랜 시간의 코딩과 참을성이 필요했다고 해 봅시다. 토큰이 어딘가에 유출되고, 누군가가 토큰을 얻게 됩니다. 그 사람은

* 봇이 들어가 있는 모든 서버에서 도배하거나
* 최대한 많은 유저들에게 DM으로 도배하거나
* 최대한 많은 채널을 지우거나
* 최대한 많은 서버 멤버를 추방/차단하거나
* 봇이 들어가 있는 모든 서버에서 나가거나
* 심지어 봇이 돌아가는 서버에 접근해서 망가뜨릴 수도 있어요!

이뿐만 아니라 훨씬 많은 것을 할 수 있어요. 무섭죠? 그러니 토큰을 최대한 안전하게 유지하세요!

가이드의 [초기 파일](/creating-your-bot/) 페이지에서 토큰을 설정 파일에 안전하게 저장하는 방법을 설명합니다.

::: danger
혹시 봇 토큰을 실수로 유출하게 된다면 (공개 레포에 커밋하거나 지원에 올리거나 등등), 혹은 그 외에도 봇에 문제가 생겼다면, 이 페이지로 돌아와서 "Regenerate"를 클릭해서 토큰을 바꾸세요. 이렇게 하면 기존 토큰은 무효가 돼요. 기존 토큰을 사용하던 모든 곳에서 새 토큰으로 바꾸는 것을 잊지 마세요!
:::
