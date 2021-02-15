# Lambda Discord Bot: Documentation
## Lambda Tags / Message Formatting
Tags are a great way to format your custom messages, they are supported on most instances of them.
### How do you format tags?
`Other message content goes here {tag.attribute}`
### Note:
If any one tag is invalid, the whole message will output it's raw value. Make sure that your tags are valid.

---
### *Type:* User
Represents a Discord User. 
#### Attributes:

| Attribute | Output | Output Type | Example Output |
| ----------- | ----------- | ------- | ------- |
| `{user}`      | The user's tag in Name#Discrim format. | Raw String | Username#1234|
| `{user.name}` | The user's username.  | Raw String | Username |
| `{user.nick}` | The user's server nickname. | Raw String  | Nickname
| `{user.mention}` | The ping, or mention of a user. | Raw String  | @Username |
| `{user.discrim}` | The user's discriminator. | Raw String  | 1234 | 
| `{user.id}` | The user's User ID. | Raw String  | 6214532484759437332 |
| `{user.pfp}` | The avatar (as URL) of the user. | Raw String  | - |

### *Type:* Integer
Represents a number or integer.
#### Attributes:

| Attribute | Output | Output Type | Example Output |
| ----------- | ----------- | ------- | ------- |
| `{number}` | The number itself. | Raw String | 22
| `{number.ord}` | The number as an ordinal. | Raw String | 22nd

### *Type:* Warn
Represents a warn via `>warn` command.
#### Attributes:
 
| Attribute | Output | Output Type | Example Output |
| ----------- | ----------- | ------- | ------- |
| `{warn.reason}` | The reason of the warn. | Raw String | Spamming
| `{warn.moderator}` | The user who dealed the warn. | *User* | Mod#1234
| `{warn.count}` | The total amount of warns the offender now has. | *Integer* | 2

---
### Leveling messages
These tags will be represented in level-up messages. Configure them by using the `>levelsettings message` command.

| Tag variable | Type | Description | 
| - | - | - |
| user | *User* | The user that leveled up.
| level | *Integer* | The new level of the user.

### Warn messages
These tags will be shown whenever someone is warned.

|Tag variable | Type | Description | 
 | - | - | - |
| user | *User* | The user that was warned. 
| warn | *Warn* | The warn that was dealt.

---
### Examples

Here are some examples of Lambda tags:
> `Congratulations {user.mention} on leveling up to level **{level}**!`

> `**{user}** was warned for {warn.reason}. This is their {warn.count.ord} warning.`

### Need help?

If you need help, join our [Support Server](https://discord.gg/vuAPY6MQF5) and ask your question there.
