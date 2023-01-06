# tpinteract

Key/lock teleports for Omegga. Pulled out of the [ny22](https://github.com/voximity/omegga-ny22) plugin.

## Installation

`omegga install gh:voximity/tpinteract`

## Usage

### Unlocked teleport on click

Use `/tpinteract` and insert the text into an Interact component's "Write to Console" field. It will look like:

`tp:X,Y,Z`

### Locked teleport

1. Stand at the destination of your locked teleport
2. Run `/locks new <lock-name> <key-name>`
    1. The `<lock-name>` is a unique name for your lock. It will always be unlocked by the same key.
    2. The `<key-name>` is a unique name for the key that unlocks this lock.
3. Paste the copied brick. It will teleport you to the destination only if you have the required key. This is the "lock" brick.
4. Create a new brick and add an Interact component to it.
5. Set the "Write to Console" field to `key:<key-name>`. It will grant `<key-name>` on click, the same key name you used when you created the lock.

#### Changing the teleport messages

To change the error message on a lock, use

`/locks error <lock-name> You do not have the key for that lock!`

To change the success message on a lock, use

`/locks message <lock-name> Welcome to my secret hideout!`
