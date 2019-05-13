# Testing

## RemindCommand.java (Josh)

**Test 1: Good Case (send a reminder)** - `!remind general 1 hello`

**Test 2: Bad Case (invalid channel)** - `!remind notachannel 1 hello`

**Test 3: Bad Case (invalid time)** - `!remind general abc123 hello`

**Test 4: Bad Case (no message given)** - `!remind general 1`

## CommandAdminCommand.java (Sean)

*First, run `!cfg show_unknown_commands true` to ensure the bot will send a message when a blacklisted command is used.*

**Test 1: Good Case (disabling)** - `!ca fun disable` followed by `!8ball hi`

**Test 2: Good Case (enabling)** - `!ca fun enable` followed by `!8ball hi`

**Test 2: Bad Case (invalid category)** - `!ca abc123 disable`

**Test 3: Bad Case (invalid argument)** - `!ca fun abc`

## SetupCommand.java (Sean + Josh)

*Setup wizard runs through 9 settings that have error checking on each, an example of doing so for setting 1:*

**Good Case (requires a role in server)** - `setup` followed by `roleName`

**Bad Case (server does not have role with name provided)** - `setup` followed by `agalsdhfalsdkjgf;lkdjla;skdjg`

*Example for setting 2:*

**Good Case** - `setup` followed by *good case for setting 1* followed by `yes` or `no`

**Bad Case** - `setup` followed by *good case for setting 1* followed by `as;ldkfj;asldkfj;asdj`

*Additionally, after running `!setup`, you can run `!setup test` to get a list of settings, to visually see that they were changed.*
