You have to keep track of the time you spend on the project and its features or tasks.
In order to transparently do so, create tickets in the provided Gitlab project corresponding to the tasks you perform.

To log time write a comment on this issue with the `/spend` slash command.
For example to log 2 hours and 15 minutes create this comment:

`/spend 2h15m`

You should see a message stating that you have added the given amount to the spent time of the issue.

In the wiki a [[Timetracking]] site is automatically added containing a statistical overview of the spent time per user and week.

If you make a mistake, you can remove booked time with `/spend -2h` for example.
NEVER use `/remove_time_spent`!
It will delete every users time.
While GitLab supports an optional date argument to `/spend`, we do not accept that.
You have to book all time in a timely manner.
Therefore all time will be counted at the day you enter it in GitLab.