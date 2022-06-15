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
    
## Apache Kafka 이해하기
  #1
  <br/><image src='https://user-images.githubusercontent.com/57661474/164008473-3e88ffc6-d866-49fa-a818-b568f38ca28d.jpeg'/>
  <br/><br/>#2
  <br/><image src='https://user-images.githubusercontent.com/57661474/164012906-3b2c8b61-1c37-4410-9553-f9d9399a1044.jpeg'/>
  <br/><br/><b>(1)Topic</b>
  <br/> Message가 관리되는 단위, 예를들어 카톡 단체방 A, B 가 있다면 A 방으로 보낸 메세지가 B방에 노출되며 안된다. A 방에서 생산된 메세지는 A방에 존재하는 사람들에게마 보여져야 한다.
  <br/> 따라서 각 생성되는 채팅방 마다 Topic을 다르게 설정해야 한다.
  <br/><br/><b>(2)broker</b>
  <br/> Broker 는 Kafka Server 를 의미한다. 한 클러스터 내에서 여러개의 kafka server 를 띄울수 있다. Topic 별로 메세지를 분류하여 쌓아 놓는다.
  <br/><br/><b>(3)Producer</b>
  <br/> Producer는 특정 Topic 의 메세지를 생성한 뒤 해당 메세지를 broker에 전달한다. 
  <br/><br/><b>(4)Consumer</b>
  <br/> Consumer들이 메세지를 가져가 처리한다
  <br/><br/><b>(5)Zookeeper</b>
  <br/> Zookeeper 는 Broker의 분산처리를 담당한다. 주키퍼는 분산 시스템의 일부분이기 때문에 동작을 멈춘다면 분산 시스템이 멈출수도 있다. 그래서 안정성을 확보하기 위해 클러스터로 구축한다.
  <br/> Watcher
  <br/>주키퍼를 사용하는 클라이언트 A가 ZooKeeper에게 Watcher 등록을 요청한다.
  <br/>주키퍼를 사용하는 클라이언트 B가 ZooKeeper에게 ZNode를 수정한다고 말한다.
  <br/>클라이언트 A에게 변경 이벤트를 전달한다.

### 사용한 모듈들
<b>1.docker</b>
<b>2.docker-compose</b>
<b>3.dockerize Kafka</b>


### Websocket을 이용하여 테스트 방법 찾아보기
<br/> 1. https://victorydntmd.tistory.com/348
 
<br/><br/>### 방법 2. ReactiveStream + MongoDB + SpringBoot
==>
