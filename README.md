To add, remove, or change a keybind then look in stored keybinds then look at the `UserInputType` you want it to be(Keys,Gampdad) then inside the player dictionary key looks like this.


```
local StoredKeybinds = {
  [player] = {
    ["Gamepad"] = {
      ["KeyBind name has to be same as the Key type action"] = Input to activate,
      ["To add another key do this"] = Input to activate,
    }
    ["Keys"] = {
      ["Key name"] = Input to activate
    }
}
```

For the server put the name of the keybind you put in the other module or else it wont work looks like this

```
function Actions.Name of action on the client module(player, inputState)
      What input stae you want the key to do something like this
      if inputState == Enum.UserInputState.Begin then
        What the action does when you hold the Key
      elseif input == Enum.UserInputState.End then
        What the action does when you let go of the key
      end
  end
```
Also if you add an other action then do the same thing up there with the name for the other action.

Any module parented under the RecieveActions Module has to be required if you want the action that calls the module function to have a function.
