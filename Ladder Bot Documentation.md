Ladder Bot Documentation
Overview
The Ladder Bot manages a competitive ladder where teams can challenge each other and move up or down the ranks based on match results. This bot handles team registration, match reporting, challenge management, and more.

Commands
1. Registering a Team
Command: !register_team <team_name> <@member1> <@member2> ...
Description: Registers a new team with the specified members.
Parameters:
<team_name>: The name of the team to be registered.
<@member1>, <@member2>, etc.: Mentions of Discord users who are members of the team. If no members are mentioned, the command creator will be added as the sole member.
Example: !register_team Alpha @User1 @User2
Response: Confirms registration and lists the team members.
Permissions: Any user can register a team.

2. Starting the Ladder
Command: !start_ladder
Description: Initializes the ladder, sorting teams alphabetically and assigning initial ranks.
Parameters: None
Example: !start_ladder
Response: Confirms that the ladder has been started and posts the initial standings.
Permissions: Admin only

3. Challenging a Team
Command: !challenge <challenger_team> <team_name>
Description: The challenger_team challenges team_name. The challenger can only challenge a team up to two ranks higher.
Parameters:
<challenger_team>: The name of the team initiating the challenge.
<team_name>: The name of the team being challenged.
Example: !challenge Bravo Alpha
Response: Confirms the challenge and lists the teams involved.
Permissions: Any user can challenge if the ladder is running.

4. Reporting a Win
Command: !report_win <winning_team>
Description: Reports the result of a match, adjusting ranks accordingly.
Parameters:
<winning_team>: The name of the team that won the match.
Example: !report_win Alpha
Response: Updates the ranks and confirms the match result.
Permissions: Any member of the involved teams can report a win.

5. Accepting a Challenge
Command: !accept_challenge <team_name>
Description: Accepts a pending challenge.
Parameters:
<team_name>: The name of the team accepting the challenge.
Example: !accept_challenge Alpha
Response: Confirms that the challenge has been accepted and instructions for reporting the result.
Permissions: Any team can accept if a challenge is pending.

6. Declining a Challenge
Command: !decline_challenge <team_name>
Description: Declines a pending challenge, causing rank changes.
Parameters:
<team_name>: The name of the team declining the challenge.
Example: !decline_challenge Alpha
Response: Updates ranks and confirms that the challenge has been declined.
Permissions: Any team can decline if a challenge is pending.

7. Posting Standings
Command: !post_standings
Description: Displays the current standings.
Parameters: None
Example: !post_standings
Response: Lists the current rankings of all teams.
Permissions: Any user can post standings if the ladder is running.

8. Setting the Standings Channel
Command: !set_standings_channel <#channel>
Description: Sets the channel where standings will be posted.
Parameters:
<#channel>: The channel where standings will be posted.
Example: !set_standings_channel #standings
Response: Confirms the new standings channel.
Permissions: Admin only

9. Adjusting Team Rank
Command: !set_rank <team_name> <rank>
Description: Manually sets a team's rank.
Parameters:
<team_name>: The name of the team whose rank is being adjusted.
<rank>: The new rank for the team.
Example: !set_rank Alpha 1
Response: Updates the team's rank and adjusts other teams' ranks as needed.
Permissions: Admin only

10. Ending the Ladder
Command: !end_ladder
Description: Ends the ladder and clears all data.
Parameters: None
Example: !end_ladder
Response: Posts final standings, announces winners, and clears all teams and matches.
Permissions: Admin only

11. Show Documentation Link
Command: !show_help
Description: Provides link to Ladderbot's documentation
Parameters: None
Example: !show_help
Response: Provide's github link to documentation
Permissions: Anyone