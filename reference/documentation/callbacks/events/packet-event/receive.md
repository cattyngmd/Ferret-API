---
description: Packet Receive Event
---

# Receive

## `packet_receive`

Dispatches before you receive a packet.

```lua
this:registerCallback("events", function(event)
    if(event:getName() == "packet_receive")
        if(arg:is("GameMessageS2CPacket")) then
            print(event:getPacket():getMessage())
        end
    end
end)
```
