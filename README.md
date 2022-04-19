# KafKaPractice
KafKa 활용하기


## Intro
### 방법 1. KafKa + SpringBoot(Websocket)
==> 
  <b>a. kafka 의 구성요소</b>
    <br/><br/>a-1 Event
        kafka 에서 Producer 와 Consumer 가 데이터르 주고 받는 단위
    <br/><br/>a-2 Producer
        kafka 에 이벤트를 게시하는 클라이언트
    <br/><br/>a-3 Consumer
        Topic으 구독하고 이로부터 얻어내 이벤트를 처리하는 클라이언트
    <br/><br/>a-4 Topic
        이벤트가 실제로 쓰이는 곳. Producer는 Topic에 이벤트를 게시한다. 그리고 Consumer는 Topic으로 부터 이벤트를 가져와 처리한다. Topic = 폴더, Event = 파일 로 구분하면 쉬움
 <br/><br/><b>b. 채팅서비스 만들기</b>
 <br/>Download 항목 : Zookeeper
 <br/>구성 : springBoot, Zookeeper(kafka cluster management clinet), websocket, mongoDB
 <br/><br/>보통 미들웨어 클라이언트는 2가지로 나뉜다.
    <br/>&emsp;1. MessageBroker - 미들웨어의 메세지를 컨트롤 (redis)
    <br/>&emsp;2. EventBroker - 미들웨어의 메세지 or 이벤트를 둘다 컨트롤할 수 있다. (kafka)
    
<b>Apache Kafka 이해하기</b>
  <br/>#1
  <br/><image src='https://user-images.githubusercontent.com/57661474/164008473-3e88ffc6-d866-49fa-a818-b568f38ca28d.jpeg'/>
  <br/>#2
  <br/><image src='https://user-images.githubusercontent.com/57661474/164008212-d17f9ae4-a2ac-4546-a87a-ca944cd49b69.jpeg'/>
    
### 사용한 모듈들
<b>1.docker</b>
<b>2.docker-compose</b>
<b>3.dockerize Kafka</b>
 
 
<br/><br/>### 방법 2. ReactiveStream + MongoDB + SpringBoot
==>
