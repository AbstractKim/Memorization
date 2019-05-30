## The Command Pattern

**'The Command Pattern'** encapsulates a request as an object, thereby letting you parameterize other objects with different requests, queue or log requests and support undoable operations

- Client (RemoteLoader)
- Invoker (RemoteController)
  - onCommands
  - offCommands
  - setCommand()
  - onButtonWasPushed()
  - offButtonWasPushed()
- Receiver (Light)
  - on()
  - off()
- Command << interface >>
  - execute()
- ConcreteCommand


#### More Example
- Queuing requests
- Logging request

[참고 wikipedia](https://en.wikipedia.org/wiki/Command_pattern)
