# KafKaPractice
KafKa 활용하기


## Intro
### 방법 1. KafKa + SpringBoot(Websocket)
==> 
  a. kafka 의 구성요서
    a-1 Event
        kafka 에서 Producer 와 Consumer 가 데이터르 주고 받는 단위
    a-2 Producer
        kafka 에 이벤트를 게시하는 클라이언트
    a-3 Consumer
        Topic으 구독하고 이로부터 얻어내 이벤트를 처리하는 클라이언트
    a-4 Topic
        이벤트가 실제로 쓰이는 곳. Producer는 Topic에 이벤트를 게시한다. 그리고 Consumer는 Topic으로 부터 이벤트를 가져와 처리한다. Topic = 폴더, Event = 파일 로 구분하면 쉬움
    
### 방법 2. ReactiveStream + MongoDB + SpringBoot
==>
