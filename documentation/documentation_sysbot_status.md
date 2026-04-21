## `/sysbot_status`

Shows the current public status of the Sysbots `XSF1` and `XSF2`.

### What this command does
When an admin or user runs `/sysbot_status`, the bot:
- Checks the saved Sysbot configuration
- Posts a status embed for `XSF1` if it exists
- Posts a status embed for `XSF2` if it exists
- Automatically removes each status message after 30 seconds

### Important behavior
- Each status message stays up for **30 seconds from the moment it is posted**
- If both `XSF1` and `XSF2` exist, both messages are posted and each has its **own separate 30-second timer**
- If one switch is missing, only the one that exists will be shown
- If neither exists, the bot posts a short fallback message and removes it after 30 seconds

### What users will see
Each status embed may include:
- Switch name
- Prefix
- Modded status
- Current game
- Self-serve raid eligibility
- Trading availability
- Description
- Notes

### Example use
Use this command when:
- Staff want to quickly confirm which Sysbots are active/configured
- Users need a temporary public status check
- You want a clean status message that does not stay in the channel permanently

### Auto-cleanup
This command is designed to keep channels clean.

That means:
- The bot posts the status
- Users can read it
- The message disappears automatically after 30 seconds

### Notes for staff
- `/sysbot_status` is a read-only command
- It does **not** edit the Sysbot config
- To change Sysbot settings, use `/sysbot_config`
- `/sysbot_status` is intended for quick public visibility, not permanent logging
