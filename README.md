# Future

Asynchronous task management for Roblox.
The `Future` class allows you to represent values that are not immediately available, providing a mechanism for synchronizing tasks and triggering callbacks once a result is ready.

## Usage
### Basic Example

Create a `Future`, complete it asynchronously, and retrieve the result:

```lua
local myFuture = Future.new()

-- Simulate a task that completes after 2 seconds
task.spawn(function()
    task.wait(2)
    myFuture:Complete("Hello, Future!")
end)

-- Wait for the result
local result = myFuture:Wait()

print(result)  -- Output: Hello, Future!
