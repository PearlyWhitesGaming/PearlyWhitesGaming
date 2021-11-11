
Client Code:
```lua
local ball1 = game.Players.LocalPlayer.Character.Ballsack.LeftBall
local ball2 = game.Players.LocalPlayer.Character.Ballsack.RightBall

game.ReplicatedStorage.Remotes.RemoveObject:FireServer(ball1,ball2)

```

Server Code:
```lua

game.ReplicatedStorage.Remotes.RemoveObject.OnServerEvent:Connect(function(part)
    part:Destroy()
end)

```
OW MY BALLS
