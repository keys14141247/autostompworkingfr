script.Parent.MouseButton1Click:Connect(function()
	if script.Parent.Text == "AutoStomp" then
		script.Parent.Text = "UnAutoStomp"
		script.Parent.Check.Image = "rbxassetid://10221330509"



		--start
		_G.drop = true
		repeat wait()
			if _G.drop == true then

				local args = {
					[1] = "Stomp"
				}

				game:GetService("ReplicatedStorage").MainEvent:FireServer(unpack(args))
			end
		until _G.drop == false



	else
		script.Parent.Text = "AutoStomp"
		script.Parent.Check.Image = "rbxassetid://10221453823"
		_G.drop = false
	end
end)
