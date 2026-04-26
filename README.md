# Blox
Fruits
for i, v in pairs(game.Players:GetPlayers()) do
		if game.ReplicatedStorage.PlayerInGame:FindFirstChild(v.Name) then
			v.PlayerGui.Core.LoadingFrame.Visible = true
			v.PlayerGui.Core.Settings.Visible = false
			v.PlayerGui.Core.Menu.Visible = false
			for i, c in pairs(game.Workspace.MapFolder:GetChildren()) do
			v.Character.Torso.CFrame = CFrame.new(c.Spawn.Tele.Position)
			end
			game.ReplicatedStorage.Bindables.LoadingStop:FireClient(v)
		wait(1)
			timer()
		else
			print("a")
		end
		end
