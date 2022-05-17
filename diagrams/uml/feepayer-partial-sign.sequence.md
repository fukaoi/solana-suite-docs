@startuml

header: Fee payer partial signed transfer
title: This is a flow to perform a secure transfer \n without sending the feepayer's private key

autonumber

actor "Client/User" as client
collections "Solana Suite" as sdk
hnote over client : Action before\n SOL transfer

client -> sdk :  Call SolNative.feePayerPartialSignTransfer()
note right
  Create Hex data in a tranaction 
  signed only by the Client/User
end note
activate sdk
client <- sdk : Hex data(signed transaction by Client/User) 

deactivate sdk
|||

client -> Server : Send http reqest Hex data

note right
  Send Hex data to server in some way. In the traditional way, 
  http reqest would send <font color=red>"post method"</font> since the Hex data size is not fixed.

  [Recommended] Hex data itself be encrypted.
end note
activate Server
|||
sdk <- Server : Call new PartialSignInstruction().submit()

note right
  Sign the hex data received from Clinet/User with the private key of feePayer.
  Unlike the normal transfer action, <font color=red>"PartialSignInstruction"</font> object must be generated.
  After that, execute the submit() function in the same way.
end note

sdk -> Server : Result of sbumit(): Ok or Err
deactivate Server
@enduml


```
Caution: 
    * This flow omits the originally required security measures for readability. 
    * Please note that the following is a list of the security measures that are required.
```

