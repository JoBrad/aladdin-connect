# aladdin-connect
Python module that allows interacting with Genie Aladdin Connect devices. This fork adds a Door convenience class.

Note that shared doors are not currently supported, only doors that are owned by your account can be controlled.

## Usage
```
from aladdin_connect import AladdinConnectClient

# Create session using aladdin connect credentials
client = AladdinConnectClient(email, password)
client.login()

# Get list of available doors
doors = client.get_doors()
my_door = doors[0]

# Issue commands for doors
my_door.close()
my_door.open()

# Get updated door status
print(my_door.status)
```
