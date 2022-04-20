# Send

## `packet_send`

Dispatches before you send a packet.

```lua
this:registerCallback("events", function(event)
    if(event:getName() == "packet_send")
        if(event:is("ChatMessageC2SPacket") then
            print(event:getPacket():getChatMessage())
        end
    end
end)
```
