
>Fee payer partial sign flow

@startuml
!define LIGHTORANGE
!$FONTNAME = "Meiryo"
!includeurl https://raw.githubusercontent.com/Drakemor/RedDress-PlantUML/master/style.puml
autonumber

actor "Client/User" as client
collections "Solana Suite" as sdk
hnote over client : Action before\n any transfer
client -> sdk : 
activate sdk
client <- sdk : hello
deactivate sdk
|||
client -> Server : send hexInstruction
|||
sdk <- Server : hello
activate sdk
sdk -> Server : aaaa
deactivate sdk
@enduml


```
Caution: 
    * This flow omits the originally required security measures for readability. 
    * Please note that the following is a list of the security measures that are required.
```

