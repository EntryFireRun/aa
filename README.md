# 혹시 프로젝트 퍼갈 분에게 남기는 메시지
~~어짜피 퍼가는 사람 없지만~~  

이거 미완성입니다.  
그리고 이거 **작품테러 코드** 연구중이에요. 지금 이거 작동 시켜도 아누것도 안돼고 잘 수정하면  자신에게만 보이는 작품테러로 됩니다.<br><!--마지막엔 BR쓰는 센스(?)-->
> ~~아마 실제로 만들려면 내년쯔음에...~~

# 코드 필요한분은...
밑에 코드에 복사를 누르거나 인덱스.js파일을 찾으세요
___
```js
global.express = require('express');
global.axios = require('axios');//필요한 모듈 설치

express()
  .get('/', (req, res) => {
    res.send(`GMT ${new Date} Running!`);
  }).listen(3000);//24시간 작동을 위한 서버 열기
 axios.post("https://playentry.org/graphql",
    {"query":`mutation {signinByUsername (username: "korearun", password: "${process.env.pass}") {id username nickname}}`});//대상 계정으로 로그인
while(true){ //무한반복 요청
 axios.post("https://playentry.org/graphql",
 {"query":`mutation CREATE_PROJECT($name:String $speed: Int $objects: JSON $variables: JSON $messages: JSON $functions: JSON $tables: JSON $scenes: JSON $blockLog: JSON $lecture:ID $study:ID $discovery: ID $isForLecture:Boolean $isForStudy:Boolean $isForSubmit: Boolean $isPracticalCourse: Boolean $interface: JSON $aiUtilizeBlocks: JSON $expansionBlocks: JSON $description: String $description2: String $description3: String $thumb:String $isopen: Boolean $categoryCode: String $parent: ID $learning: String ) {createProject(name: $name speed: $speed objects: $objects variables: $variables messages: $messages functions: $functions tables: $tables scenes: $scenes blockLog: $blockLog lecture: $lecture study: $study discovery: $discovery isForLecture: $isForLecture isForStudy: $isForStudy isForSubmit: $isForSubmit isPracticalCourse: $isPracticalCourse interface: $interface aiUtilizeBlocks: $aiUtilizeBlocks expansionBlocks: $expansionBlocks description: $description description2: $description2 description3: $description3 thumb: $thumb isopen: $isopen categoryCode: $categoryCode parent: $parent learning:$learning){statusresult}}","variables":{"category":"기타","scenes":[{"id":"7dwq","name":"장면1"}],"variables":[{"name":"초시계","id":"brih","visible":false,"value":"0","variableType":"timer","isCloud":false,"isRealTime":false,"cloudDate":false,"object":null,"x":134,"y":-70},{"name":"대답","id":"1vu8","visible":false,"value":"0","variableType":"answer","isCloud":false,"isRealTime":false,"cloudDate":false,"object":null,"x":150,"y":-100}],"objects":[{"id":"7y0y","name":"엔트리봇","script":"[[{"id":"f5uu","x":50,"y":30,"type":"when_run_button_click","params":[null],"statements":[],"movable":null,"deletable":1,"emphasized":false,"readOnly":null,"copyable":true,"extensions":[]},{"id":"nu34","x":0,"y":0,"type":"repeat_basic","params":[{"id":"csq0","x":0,"y":0,"type":"number","params":[10],"statements":[],"movable":null,"deletable":1,"emphasized":false,"readOnly":null,"copyable":true,"extensions":[]},null],"statements":[[{"id":"r9j3","x":0,"y":0,"type":"move_direction","params":[{"id":"kufn","x":0,"y":0,"type":"number","params":[10],"statements":[],"movable":null,"deletable":1,"emphasized":false,"readOnly":null,"copyable":true,"extensions":[]},null],"statements":[],"movable":null,"deletable":1,"emphasized":false,"readOnly":null,"copyable":true,"extensions":[]}]],"movable":null,"deletable":1,"emphasized":false,"readOnly":null,"copyable":true,"extensions":[]}]]","objectType":"sprite","rotateMethod":"free","scene":"7dwq","sprite":{"pictures":[{"id":"vx80","dimension":{"width":284,"height":350},"fileurl":"/lib/entry-js/images/media/entrybot1.png","name":"엔트리봇_걷기1","scale":100,"imageType":"png"},{"id":"4t48","dimension":{"width":284,"height":350},"fileurl":"/lib/entry-js/images/media/entrybot2.png","name":"엔트리봇_걷기2","scale":100,"imageType":"png"}],"sounds":[{"duration":1.3,"ext":".mp3","id":"8el5","fileurl":"/lib/entry-js/images/media/bark.mp3","name":"강아지짖는소리"}]},"selectedPictureId":"vx80","lock":false,"entity":{"x":0,"y":0,"regX":142,"regY":175,"scaleX":0.3154574132492113,"scaleY":0.3154574132492113,"rotation":0,"direction":90,"width":284,"height":350,"font":"undefinedpx","visible":true}}],"expansionBlocks":[],"aiUtilizeBlocks":[],"speed":60,"name":"[비공식]엔트리시험작품","likeCnt":0,"visit":0,"isopen":false,"user":"609d9bf26c7d1f013ad5a1f2","messages":[],"functions":[],"tables":[],"interface":{"canvasWidth":324,"menuWidth":258,"object":"7y0y"},"externalModules":[],"isPracticalCourse":false,"blockLog":{"categories":["event","repeat","walk"],"when_run_button_click":1,"repeat_basic":1,"number":2,"move_direction":1}}`});/*작품 만들기 요청*/
}
```
___

Replit : replit.com/@FireRun/aa#README.md
Github : github.com/EntryFireRun/aa/blob/main/README.md
