# Access cards

# Step 1:
all tools from ```DROP_INTO_REPLICATEDSTORAGE``` drop into ```ReplicatedStorage```
For giving automaticly the cooresponding access card to players depends on their team, create/add this lines:

## Example
```lua
local replicatedStorage = game.ReplicatedStorage
local accessCard_one = replicatedStorage["AccessCard-1"]

game.Players.PlayerAdded:Connect(function(player)
	player.CharacterAdded:Connect(function()
		
		if player.Team == game.Teams["Level-1"] then
			local accessCardlvl_1_clone = accessCard_one:Clone()
			accessCardlvl_1_clone:SetAttribute("AccessLvl", 1)
			accessCardlvl_1_clone.Name = "AccessCard"
			accessCardlvl_1_clone.Parent = backpack

		end
	end)
	
end)
```
* When using ```player.Team``` we are getting current joined player team.
* ```game.Teams[The name of the team]``` will give back the team object.
* ```player.Team == game.Team[The name of the team]``` give us true or false depending on that we add the access card

```SetAttribute("AccessLvl", number 0-5)``` will decide what level this card can give access to 

!```accessCardlvl_1_clone.Name = "AccessCard"``` VERY IMPORTANT TO GIVE THE NAME ```AccessCard``` ~player cant have 2 access cards in same time.