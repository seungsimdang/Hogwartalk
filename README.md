# 호그와톡

## 💁 프로젝트 정보

> 주어진 API와 소켓을 활용한 채팅앱 제작 프로젝트입니다. <br>
> 호그와트 학생 체험을 할 수 있도록 구성하였습니다. <br>
> 개발기간: 2023.11.06 ~ 2023.11.16
> <br>

<br>

## 🌐 배포 주소

> 배포 주소: https://hogwartalk.vercel.app/ <br>
> 테스트 계정 : ID : dumbledore / Password : dumbledore
> <br>

<br>

## 🚖 개발 팀 소개

|                          어승준                           |                           이승연                           |                          이승현                           |                           배경규                           |                          장문용                           |
| :-------------------------------------------------------: | :--------------------------------------------------------: | :-------------------------------------------------------: | :--------------------------------------------------------: | :-------------------------------------------------------: |
|      [@seungjun222](https://github.com/seungjun222)       |          [@ewinkite](https://github.com/ewinkite)          |     [@seungsimdang](https://github.com/seungsimdang)      |       [@kyungkyuBae](https://github.com/kyungkyuBae)       |          [@moonyah](https://github.com/moonyah)           |
| ![](https://avatars.githubusercontent.com/u/39702832?v=4) | ![](https://avatars.githubusercontent.com/u/139189610?v=4) | ![](https://avatars.githubusercontent.com/u/93538221?v=4) | ![](https://avatars.githubusercontent.com/u/131759810?v=4) | ![](https://avatars.githubusercontent.com/u/51106050?v=4) |
|                         채팅 기능                         |                퀴즈, 클럽 페이지 관련 기능                 |                         채팅 기능                         |                   로그인/ 회원가입 기능                    |        공통 컴포넌트(헤더 - 마이페이지, 친구 목록)        |

<br>

## 💻 개발 스택

### 환경

`VSC` `GIT` `GITHUB`

### 개발

`Next.js` `REACT` `FIREBASE` `TYPESCRIPT` `Recoil`

### 🌙 이슈 관리 및 소통

`JIRA` `SLACK` `NOTION`

<br/>

## 🤝 협업 방식

커밋 컨벤션, 코딩 컨벤션, 깃허브 규칙 등의 내용은 아래의 노션 페이지를 참고해주세요! </br>

### [🔗 노션 페이지](https://www.notion.so/I-am-2-bb6a5448abf64a9bb941c8e98bef31f2?pvs=4) </br>

<br/>
<br/>

## 🤝 요구사항 반영 여부

### 필수 구현 사항

✅ `useState`, `useReducer`를 활용한 상태 관리 구현 <br/>
✅ `Sass` 또는 `styled-component`를 활용한 스타일 구현 <br/>
✅ `react` 상태를 통한 CRUD 구현 <br/>
✅ 상태에 따라 달라지는 스타일 구현 <br/>
✅ `custom hook`을 통한 비동기 처리 구현 <br/>
✅ 유저인증 시스템(로그인, 회원가입) 구현 <br/>
✅ `jwt`등의 유저 인증 시스템 (로그인, 회원가입 기능) <br/>
✅ 소켓을 이용한 채팅 구현 <br/>

### 선택 구현 사항

✅ `Next.js`를 활용한 서버 사이드 렌더링 구현 <br/>
✅ `typescript`를 활용한 앱 구현

<br/>
<br/>

## 🔍 팀원별 세부 구현 사항

<details>
<summary style="font-size: 18px">어승준: 💬 채팅</summary>
<div markdown="1">

![image](https://github.com/KDT1-FE/Y_FE_Toy2/assets/39702832/13264393-9f03-4f52-b7ec-a4a65d8f1817)

### 1. 실시간 채팅

```
💡 소켓 연결을 통해 실시간 채팅을 할 수 있습니다. 클라이언트 화면 높이를 계산해 스크롤 맨 밑으로 이동 가능합니다.
```

### 2. 클럽 채팅방 생성 동적라우팅

```
💡 Next.js 동적라우팅을 통해 클럽 채팅방 생성 시, id, name값을 쿼리파라미터로 넘겨 정보에 맞게 페이지 렌더링을 시켜줍니다.
```

### 3. 내가 참여중인 대화방

```
💡 내가 참여중인 대화방을 보여줍니다. Polling 방식을 통해 latestMessages를 5초마다 업데이트 해줍니다.
```

</div>
</details>

<br>

<details>
<summary style="font-size: 18px"> 이승연: 🌐 퀴즈, 클럽, 공통</summary>
<div markdown="1">

### 1. 기숙사 배정 퀴즈 페이지 (회원가입)

#### 시나리오에 따른 기숙사 배정 로직 구현

![1퀴즈](https://github.com/Iam2Jo/Hogwartalk/assets/139189610/700a2eda-905e-4e08-9921-4085c59fcc94)

```
💡 시나리오에 따라 답변을 클릭하면 점수가 누적되며, 이에 따른 기숙사 배정이 이루어집니다.
문항별 선택한 답변 정보를 저장하여 이전/다음 이동시에도 답변이 유지됩니다.
```

### 2. 클럽 페이지

#### 채팅방 목록 조회

![3채팅방목록조회](https://github.com/Iam2Jo/Hogwartalk/assets/139189610/e5757be6-5b08-4240-95ac-4ae671b0a504)

```
💡 네 개의 기숙사 채팅방을 제외한 모든 채팅방을 불러옵니다.
이때 update 일시를 기준, 최신순으로 정렬되어 노출됩니다.
로그인한 사용자가 참여중인 채팅방의 경우 개별적으로 표기합니다.
```

#### 채팅방 생성

![4채팅방생성](https://github.com/Iam2Jo/Hogwartalk/assets/139189610/39f42276-9339-496e-88a1-794f95097996)

```
💡 새로운 채팅방을 생성하며, 생성이 완료되면 해당되는 채팅방으로 이동합니다.
제목은 필수값이며 채팅방 공개 여부 설정에 따라 목록 조회가 업데이트 됩니다.
```

#### 채팅방 참여

![5채팅방참여](https://github.com/Iam2Jo/Hogwartalk/assets/139189610/dee4cf96-696c-438d-9ca6-378a68096c93)

```
💡 현재 참여중인 채팅방의 경우 바로 해당되는 채팅방으로 이동하며,
참여중이지 않은 채팅방의 경우 참여 여부를 묻는 다이얼로그가 노출됩니다.
```

### 3. 공통

#### 로딩 페이지

![2클럽로딩](https://github.com/Iam2Jo/Hogwartalk/assets/139189610/d592854e-93a4-4f67-908d-e11e740f0bc3)

```
💡 API 호출 중 로딩 페이지가 노출됩니다.
```

#### BGM(헤더)

![6BGM](https://github.com/Iam2Jo/Hogwartalk/assets/139189610/9ad95e5a-1ee6-4a75-b7a0-640e478cb3cb)

```
💡 홈페이지 최초 진입 후 특정 영역을 클릭시 BGM이 재생됩니다.
헤더에서 아이콘을 통해 제어가 가능하며, 경로 이동되어도 재생 상태가 유지됩니다.
```

</div>
</details>

<br>

<details>
<summary style="font-size: 18px">이승현: 💬 채팅</summary>
<div markdown="1">

### 1. 기숙사 선택 페이지

![image](https://github.com/Iam2Jo/Hogwartalk/assets/93538221/793c46ea-0812-427b-87fb-049892a3e15a)

```
💡 로그인 후에 처음으로 표시되는 페이지입니다.
사용자가 배정받은 기숙사 채팅방만 입장할 수 있으며, 가운데의 클럽 로고를 누르면 클럽 페이지로 이동합니다.
```

### 2. 채팅방

#### 채팅방 헤더

![image](https://github.com/Iam2Jo/Hogwartalk/assets/93538221/655c3117-7a5d-4ade-8119-7d71b21ad953)

```
💡 채팅방에 참여, 초대를 받아 현재 채팅방의 제목과 인원수가 표시됩니다.
노란 뱃지를 눌러 사용자를 초대할 수 있으며 더보기 버튼을 눌러 채팅방 정보를 보거나 채팅방에서 나갈 수 있습니다.
```

### 채팅방 초대 모달

![image](https://github.com/Iam2Jo/Hogwartalk/assets/93538221/7537f8f5-7b24-4890-8a85-325839aa3869)

```
💡 기숙사 채팅방을 제외한 모든 클럽 채팅방에서 사용자를 초대할 수 있습니다.
현재 채팅방에 참여하고있는 사람을 제외한 모든 사용자가 보여지며, 사용자의 프로필 사진, 닉네임, 기숙사 정보가 표시됩니다.
```

### 채팅방 정보 모달

![image](https://github.com/Iam2Jo/Hogwartalk/assets/93538221/24e8b607-a11c-477b-82da-8f0d1c0b6322)

```
💡 현재 채팅방의 정보를 보여줍니다.
채팅방 제목, 인원수, 호스트 이름, 채팅방 개설일, 참여자 목록을 확인할 수 있습니다.
```

</div>
</details>

<br>

<details>
<summary style="font-size: 18px">배경규: 🔑 로그인/ 회원가입</summary>
<div markdown="1">

### 로그인시 Jwt토큰 발급하여 쿠키에 저장

![login__token](https://github.com/Iam2Jo/Hogwartalk/assets/131759810/1189bbec-8ef0-4503-80df-065f3bcebb4f)

```
토큰은 액세스 토큰,리프레시 토큰
```

### 회원가입

![signup](https://github.com/Iam2Jo/Hogwartalk/assets/131759810/1636bc0c-e2f4-4fc8-9569-410d1a858f15)

```
제공된 api의 이미지 용량이슈 때문에 타db를 사용하여 이미지를 저장하고 url사용
회원가입시 빈칸 있는지 유효성 검사
중복된 아이디가 있는지 체크
퀴즈를 보러가도 회원가입 폼 상태저장
```

### 모든 페이지에서 액세스 토큰 만료시 재발급

![Retoken](https://github.com/Iam2Jo/Hogwartalk/assets/131759810/c6ff8f25-a3e8-4316-a310-9a415e0feb94)

```
모든 페이지에서 액세스토큰 만료시 axios 요청 가로채서 인터셉터로 액세스토큰을 재발급 하는 로직구현
```

### 권한 없을 시(리프레시 토큰x) 로그인 페이지 유도

![로그인페이지유도](https://github.com/Iam2Jo/Hogwartalk/assets/131759810/69885ba8-189e-41e6-908b-0ebaccacdc68)

```
로그인 페이지 유도
```

</div>
</details>

<br>

<details>
<summary style="font-size: 18px">장문용: 📑 공통 컴포넌트</summary>
<div markdown="1">

### 1. 헤더 제작

![header](https://github.com/Iam2Jo/Hogwartalk/assets/51106050/f4dd96b1-1981-4f11-bd17-e5cf37d43263)

```
💡각 아이콘은 클릭 및 토글 상태에 따라 스타일이 변합니다.
```

### 2. 마이페이지 토글

> `MyPageToggle` 컴포넌트는 사용자의 프로필 정보를 표시하고 편집하는 기능을 제공하는 사이드바입니다.

#### 로그인된 사용자 정보 표시

![mypage_1](https://github.com/Iam2Jo/Hogwartalk/assets/51106050/41119e59-e530-48f9-9682-391e1f02f35b)

```
💡쿠키에 저장된 accessToken을 사용해 이름을 가져오고 Firebase Storage에서 프로필 이미지, Firebase Database에서 기숙사 정보를 가져옵니다.
```

#### 로그인된 사용자 정보 편집하기

![mypage_2](https://github.com/Iam2Jo/Hogwartalk/assets/51106050/96977b8c-3e4a-4c19-9431-04d58921d70d)

```
💡사용자가 편집 모드로 전환하면 이름, 기숙사, 프로필 이미지를 변경할 수 있습니다. 각 변경 사항은 제공된 서버와 Firebase에 업데이트됩니다.
```

### 3. 친구목록 토글

> `FriendSearchToggle` 컴포넌트는 친구를 검색하고 확인하는 역할을 하는 사이드바입니다.

#### 사용자 목록 출력 (이름, 기숙사 정보, 접속 유무 표시)

![userlist](https://github.com/Iam2Jo/Hogwartalk/assets/51106050/d17fc752-577b-4aa6-b4d5-c85530dd742b)

```
💡 서버와 소켓 통신을 통해 전체 유저와 접속 중인 유저 정보를 가져와, 각 사용자의 접속 상태를 실시간으로 표시합니다. Firebase 데이터베이스에서는 사용자의 기숙사 정보를 가져옵니다.

화면에는 각 사용자의 프로필 이미지, 이름, 학급, 그리고 실시간으로 변하는 접속 상태가 표시됩니다. 사용자의 기숙사 정보도 표시되며, 데이터는 계속해서 업데이트되어 화면에 실시간으로 반영됩니다.
```

### 4. 로그아웃

#### 페이지 이동 & 쿠키 삭제

![logout](https://github.com/Iam2Jo/Hogwartalk/assets/51106050/096e3ecc-ff3c-44c8-ab73-a65667a4bd48)

```
💡로그아웃 버튼을 누르면 로그인 페이지로 이동하고 js-cookie 라이브러리를 사용하여 'accessToken'과 'refreshToken' 쿠키를 삭제하여 로그아웃을 수행합니다.
```

</div>
</details>

<br>

## 기본 데이터 구조
### user
```ts
interface User {
  id: string;
  password: string;
  name: string;
  picture: string;
  chats: string[]; // chat id만 속합니다.
}
```
### chat
```ts
interface Chat {
  id: string;
  name: string;
  isPrivate: boolean;
  users: string[];
  messages: Message[]; // message 객체가 속합니다.
  
  updatedAt: Date;
}
```
### message
```ts
interface Message {
  id: string;
  text: string;
  userId: string;

  createdAt: Date;
}
```
## 회원

### 회원가입

사용자가 `id`에 종속되어 회원가입합니다.

- 사용자 비밀번호는 암호화해 저장합니다.
- 프로필 이미지는 url or base64 형식이어야 합니다.
- 프로필 이미지는 1MB 이하여야 합니다.

```curl
curl https://fastcampus-chat.net/signup
  \ -X 'POST'
```

요청 데이터 타입 및 예시:

```ts
interface RequestBody {
  id: string // 사용자 아이디 (필수!, 영어와 숫자만)
  password: string // 사용자 비밀번호, 5자 이상 (필수!)
  name: string // 사용자 이름, 20자 이하 (필수!)
  picture?: string // 사용자 이미지(url or base64, under 1MB)
}
```

```json
{
  "id": "abcd",
  "password": "********",
  "name": "GyoHeon",
  "picture": "https://avatars.githubusercontent.com/u/66263916?v=4"
}
```

응답 데이터 타입 및 예시:

```ts
interface ResponseValue {
  message: title
}
```

```json
{
  "message": "User created"
}
```

### id 중복 체크

`id` 중복 체크를 합니다.

```curl
curl https://fastcampus-chat.net/check/id
  \ -X 'POST'
```

요청 데이터 타입 및 예시:

```ts
interface RequestBody {
  id: string // 사용자 아이디 (필수!, 영어와 숫자만)
}
```

```json
{
  "id": "abcd",
}
```

응답 데이터 타입 및 예시:

```ts
interface ResponseValue {
  isDuplicated: boolean
}
```

```json
{
  "isDuplicated": false
}
```

### 로그인

- 발급된 `accessToken`은 7일 후 만료됩니다.

```curl
curl https://fastcampus-chat.net/login
  \ -X 'POST'
```

요청 데이터 타입 및 예시:

```ts
interface RequestBody {
  id: string // 사용자 아이디 (필수!)
  password: string // 사용자 비밀번호 (필수!)
}
```

```json
{
  "id": "abcd",
  "password": "********"
}
```

응답 데이터 타입 및 예시:

```ts
interface ResponseValue {
  accessToken: string // 사용자 접근 토큰
  refreshToken: string // access token 발급용 토큰
}
```

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjlQS3I...(생략)",
  "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjlQS3I...(생략)"
}
```

### 인증 확인

`id` 중복 체크를 합니다.

```curl
curl https://fastcampus-chat.net/auth/me
  \ -X 'GET'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
- 없음

응답 데이터 타입 및 예시:

```ts
interface ResponseValue {
  auth: boolean;
  user?: User;
}

interface User {
  id: string;
  name: string;
  picture: string;
}
```

```json
{
  "auth": true,
  "user": {
    "id": "test1",
    "name": "abcde",
    "picture": "https://avatars.githubusercontent.com/u/42333366?v=4"    
  }
}
```

### 토큰 재발급

```curl
curl https://fastcampus-chat.net/refresh
  \ -X 'POST'
```

요청 데이터 타입 및 예시:

```ts
interface RequestBody {
  refreshToken: string // access token 발급용 토큰
}
```

```json
{
  "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjlQS3I...(생략)"
}
```

응답 데이터 타입 및 예시:

```ts
interface ResponseValue {
  accessToken: string // 사용자 접근 토큰
}
```

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjlQS3I...(생략)",
}
```

### 사용자 정보 수정

- 프로필 이미지는 url or base64 형식이어야 합니다.
- 프로필 이미지는 1MB 이하여야 합니다.

```curl
curl https://fastcampus-chat.net/user
  \ -X 'PATCH'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:

```ts
interface RequestBody {
  name?: string // 새로운 표시 이름
  picture?: string // 사용자 프로필 이미지(url or base64)
}
```

```json
{
  "name": "abcde",
  "picture": "https://avatars.githubusercontent.com/u/42333366?v=4"
}
```

응답 데이터 타입 및 예시:

```ts
interface ResponseValue {
  messgae: string
}
```

```json
{
  "message": "User updated"
}
```

## 채팅
### 특정 유저 조회
- 특정 유저를 조회합니다.
```curl
curl https://fastcampus-chat.net/user?userId=${userId}
  \ -X 'GET'
  \ -H 'Authorization: Bearer <accessToken>'
```
요청 데이터 타입 및 예시:
- 없음
- 조회하고 싶은 id는 query string으로 사용합니다.

응답 데이터 타입 및 예시:
```ts
type ResponseValue = {
  user: User;
}

interface User {
  id: string;
  name: string;
  picture: string;
}
```

```json
{
  "user": {
    "id": "user1",
    "name": "lgh",
    "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
  }
}
```

### 모든 유저 조회
- 현재 존재하는 모든 유저를 조회합니다.
```curl
curl https://fastcampus-chat.net/users
  \ -X 'GET'
  \ -H 'Authorization: Bearer <accessToken>'
```
요청 데이터 타입 및 예시:
- 없음

응답 데이터 타입 및 예시:
```ts
type ResponseValue = User[]

interface User {
  id: string;
  name: string;
  picture: string;
}
```

```json
[
  {
    "id": "user1",
    "name": "lgh",
    "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
  },
  {
    "id": "user2",
    "name": "ldj",
    "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
   }
]
```

### 채팅 생성하기

```curl
curl https://fastcampus-chat.net/chat
  \ -X 'POST'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
```ts
interface RequestBody{
  name: string, // chat 이름
  users: string[], // 참가자들 id(자신 미포함)
  isPrivate?: boolean // 공개 비공개
}
```

```json
{
  "name": "test chat",
  "users": ["user1", "user2"]
}
```

응답 데이터 타입 및 예시:
```ts
interface ResponseValue {
  id: string,
  name: string,
  users: User[], // 자신을 포함한 참가자들 정보
  isPrivate: boolean,
  updatedAt: Date
}

interface User {
  id: string;
  name: string;
  picture: string;
}
```

```json
{
  "id": "fasgadsfdsghssdlsdafasd",
  "name": "test chat",
  "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
     }
  ],
  "isPrivate": false,
  "updatedAt": "2023-11-01T08:23:39.850Z"
}
```

### 특정 채팅 조회
- 특정 id의 채팅을 조회합니다.
- isPrivate: true인 채팅방은 해당 채팅방 참가자만 볼 수 있습니다.

```curl
curl https://fastcampus-chat.net/chat/only?chatId=${chatId}
  \ -X 'GET'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
- 없음

응답 데이터 타입 및 예시:
```ts
interface ResponseValue {
  chat: Chat;
}

interface Chat {
  id: string;
  name: string;
  users: User[]; // 속한 유저 정보
  isPrivate: boolean;
  latestMessage: Message | null;
  updatedAt: Date;
}

interface User {
  id: string;
  name: string;
  picture: string;
}

interface Message {
  id: string;
  text: string;
  userId: string;
  createAt: Date;
}
```

```json
{
  chat: {
    "id": "f189ab25-5644-4d72-bd7c-0170ee9c8ede",
    "name": "chat room 1",
    "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
    }
    ],
    "isPrivate": false,
    "updatedAt": "2023-10-31T13:18:38.216Z",
    "latestMessage": null
  }
}
```

### 모든 채팅 조회
- 현재 존재하는 모든 채팅을 조회합니다.
- isPrivate: true인 채팅방은 보이지 않습니다.

```curl
curl https://fastcampus-chat.net/chat/all
  \ -X 'GET'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
- 없음

응답 데이터 타입 및 예시:
```ts
type ResponseValue = Chat[]

interface Chat {
  id: string;
  name: string;
  users: User[]; // 속한 유저 정보
  isPrivate: boolean;
  latestMessage: Message | null;
  updatedAt: Date;
}

interface User {
  id: string;
  name: string;
  picture: string;
}

interface Message {
  id: string;
  text: string;
  userId: string;
  createAt: Date;
}
```

```json
[
  {
    "id": "f189ab25-5644-4d72-bd7c-0170ee9c8ede",
    "name": "chat room 1",
    "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
    }
  ],
    "isPrivate": false,
    "updatedAt": "2023-10-31T13:18:38.216Z",
    "latestMessage": null
  },
  {
    "id": "f189ab25-5644-4d72-bd7c-0170ee9c8edj",
    "name": "chat room 2",
    "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
    }
  ],
    "isPrivate": false,
    "updatedAt": "2023-10-31T15:18:38.216Z",
    "latestMessage": {
      "id": "8f7f67bb-f1ab-4792-9678-0b8546adcb6f",
      "text": "testtest444",
      "userId": "test:test6",
      "createdAt": "2023-11-06T11:15:50.588+00:00"
    }
  }
]
```

### 나의 채팅 조회
```curl
curl https://fastcampus-chat.net/chat
  \ -X 'GET'
  \ -H 'Authorization: Bearer <accessToken>'
```
- 내가 속한 모든 채팅을 조회합니다.
- isPrivate: true인 채팅방도 모두 보이게 됩니다.

요청 데이터 타입 및 예시:
- 없음

응답 데이터 타입 및 예시:
```ts
type ResponseValue = Chat[]

interface Chat {
  id: string;
  name: string;
  users: User[]; // 속한 유저 id
  isPrivate: boolean;
  latestMessage: Message | null;
  updatedAt: Date;
}

interface User {
  id: string;
  name: string;
  picture: string;
}

interface Message {
  id: string;
  text: string;
  userId: string;
  createAt: Date;
}
```

```json
[
  {
    "id": "f189ab25-5644-4d72-bd7c-0170ee9c8ede",
    "name": "chat room 1",
    "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
    }
  ],
    "isPrivate": true,
    "updatedAt": "2023-10-31T13:18:38.216Z",
    "latestMessage": null
  },
  {
    "id": "f189ab25-5644-4d72-bd7c-0170ee9c8edj",
    "name": "chat room 2",
    "users": [
      {
        "id": "user1",
        "name": "lgh",
        "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
      },
      {
        "id": "user2",
        "name": "ldj",
        "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
      }
    ],
    "isPrivate": false,
    "updatedAt": "2023-10-31T15:18:38.216Z",
    "latestMessage": {
      "id": "8f7f67bb-f1ab-4792-9678-0b8546adcb6f",
      "text": "testtest444",
      "userId": "test:test6",
      "createdAt": "2023-11-06T11:15:50.588+00:00"
    }
  }
]
```

## 채팅 참여하기

```curl
curl https://fastcampus-chat.net/chat/participate
  \ -X 'PATCH'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
```ts
interface RequestBody {
  chatId: string;
}
```

```json
{
  "chatId": "f189ab25-5644-4d72-bd7c-0170ee9c8ede"
}
```

응답 데이터 타입 및 예시:
```ts
interface ResponseValue{
  id: string;
  name: string;
  users: User[]; // 속한 유저 id
  isPrivate: boolean;
  updatedAt: Date;
}

interface User {
  id: string;
  name: string;
  picture: string;
}
```

```json
{
  "id": "f189ab25-5644-4d72-bd7c-0170ee9c8ede",
  "name": "chat room 1",
  "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
    }
  ],
  "isPrivate": true,
  "updatedAt": "2023-10-31T13:18:38.216Z"
}
```

## 채팅 나가기

```curl
curl https://fastcampus-chat.net/chat/leave
  \ -X 'PATCH'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
```ts
interface RequestBody {
  chatId: string;
}
```

```json
{
  "chatId": "f189ab25-5644-4d72-bd7c-0170ee9c8ede"
}
```

응답 데이터 타입 및 예시:
```ts
interface ResponseValue {
  message: string;
}
```

```json
{
  "message": "Leave success"
}
```

## 채팅 초대하기

```curl
curl https://fastcampus-chat.net/chat/invite
  \ -X 'PATCH'
  \ -H 'Authorization: Bearer <accessToken>'
```

요청 데이터 타입 및 예시:
```ts
interface RequestBody {
  chatId: string;
  users: string[]; // 초대할 유저 id
}
```

```json
{
  "chatId": "f189ab25-5644-4d72-bd7c-0170ee9c8ede",
  "users": ["user1", "user2"]
}
```

응답 데이터 타입 및 예시:
```ts
interface ResponseValue{
  id: string;
  name: string;
  users: User[]; // 속한 유저 정보
  isPrivate: boolean;
  updatedAt: Date;
}

interface User {
  id: string;
  name: string;
  picture: string;
}
```

```json
{
  "id": "f189ab25-5644-4d72-bd7c-0170ee9c8ede",
  "name": "chat room 1",
  "users": [
    {
      "id": "user1",
      "name": "lgh",
      "picture": "https://gravatar.com/avatar/c274467c5ef4fe381b154a20c5e7ce26?s=200&d=retro"
    },
    {
      "id": "user2",
      "name": "ldj",
      "picture": "https://gravatar.com/avatar/d94869409b4e94903723612a4f93a6f9?s=200&d=retro"
    }
  ],
  "isPrivate": true,
  "updatedAt": "2023-10-31T13:18:38.216Z"
}
```

# Socket
- socket.io 의 사용을 추천드립니다.
- Socket 연결시에도 headers는 유지해야 합니다.
## 기본 연결
```ts
io(`https://fastcampus-chat.net/chat?chatId=${chatId}`,
  {
    extraHeaders: {
      Authorization: "Bearer <accessToken>",
      serverId: "test",
    },
  })
```

## emit Event(client -> server)
### example
```ts
socket.emit('message-to-server', text)
```
### message-to-server
- 같은 방에 있는 사람들에게 메세지를 전달합니다.

요청 데이터
```ts
type RequestData: string;
```
### fetch-messages
- 이전 대화 목록을 불러옵니다.
- `messages-to-client`로 데이터를 받을 수 있습니다.

요청 데이터
- 없음
### users
- 접속 상태인 유저 목록을 불러옵니다.
- `users-to-client`로 데이터를 받을 수 있습니다.

요청 데이터
- 없음 

## on Event(server -> client)
### example
```ts
socket.on('message-to-client', (messageObject) => {
  console.log(messageObject);
})
```
### message-to-client
- 같은 방에 있는 사람들에게 메세지를 전달합니다.

응답 데이터
```ts
interface ResponseData {
  id: string;
  text: string;
  userId: string; // 메세지를 보낸 사람의 id
  createdAt: Date;
}
```
### messages-to-client
- 이전 대화 목록을 불러옵니다.

응답 데이터
```ts
interface Message {
  id: string;
  text: string;
  userId: string; // 메세지를 보낸 사람의 id
  createdAt: Date;
}

interface ResponseData {
  messages: Message[];
}
```
### join
- 같은 방에 새로운 사람이 들어오면 모든 유저의 정보를 다시 받습니다.

응답 데이터
```ts
interface ResponseData {
  users: string[]; // 참여자들 id
  joiners: string[]; // 새로운 참여자 id
}
```
### leave
- 같은 방에 사람이 나가면 모든 유저의 정보를 다시 받습니다.

응답 데이터
```ts
interface ResponseData {
  users: string[]; // 참여자들 id
  leaver: string; // 나간 사용자 id
}
```

### users-to-client
- 접속 상태인 유저 목록을 불러옵니다.

응답 데이터
```ts
interface ResponseData {
  user: string[]; // 참가자들 id
}
```

## server 연결
```ts
io(`https://fastcampus-chat.net/server`,
  {
    extraHeaders: {
      Authorization: "Bearer <accessToken>",
      serverId: "test",
    },
  })
```

## emit Event(client -> server)
### example
```ts
socket.emit('users-server')
```
### users-server
- 같은 serverId를 사용하는 online 사용자를 불러옵니다.
- `users-server-to-client`로 데이터를 받을 수 있습니다.

요청 데이터
- 없음

## on Event(server -> client)
### example
```ts
socket.on('message-to-client', (messageObject) => {
  console.log(messageObject);
})
```

### users-server-to-client
- 같은 serverId를 사용하는 접속 상태인 유저 목록을 불러옵니다.

응답 데이터
```ts
interface ResponseData {
  user: string[]; // 참가자들 id
}
```

### invite
- 새로운 채팅방 생성시 해당 채팅방 유저에게 채팅방 정보를 전송합니다.
- 기존 채팅방에 유저 초대시 초대된 유저에게 채팅방 정보를 전송합니다.

응답 데이터
```ts
interface ResponseData {
  id: string;
  name: string;
  users: string[]; // 참여자들 id
  isPrivate: boolean;
  updatedAt: Date;
}
```

### new-chat
- 새로운 대화방이 생긴 경우 (not private) 서버(팀에서 사용하는 serverId)의 참여자들에게 이를 전달합니다.

응답 데이터
```ts
interface ResponseData {
  id: string;
  name: string;
  users: string[]; // 참여자들 id
  isPrivate: boolean;
  updatedAt: Date;
}
```
