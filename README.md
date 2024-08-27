# Indian-Premier-League-in-depth-data-analysis
We are analyzing the Indian Premier League dataset to get insights into various facets of the biggest franchise cricket league. 

Indian Premier League (IPL) is the world's biggest Twenty20 franchise cricket league governed by The Board of Control for Cricket in India (BCCI). The league was founded by the Board of Control
for Cricket in India in 2007. There are two separate datasets, one based on match-by-match and the other based on ball-by-ball entries from IPL 2008 till IPL 2024. Below is a brief explanation 
of the analysis done.

## Match-by-match dataset (features/attributes)

   - MatchNo: It denotes the match number in the order of occurrence
   - city: City where the match was played
   - date: Date on which match was played (YYYY-MM-DD)
   - player_of_match: Best player awarded based on performance
   - venue: Stadium where the match was played
   - neutral_venue: 1 - the city where the match is played is not the home venue for both the participating teams, 0 - otherwise
   - team1: First participating team
   - team2: Second participating team
   - toss_winner: Team winning the toss (Based on coin flipping outcomes - heads or tails)
   - toss_decision: Decision made by the team after winning the toss
   - winner: Winning team
   - result: Winning the match either by runs or wickets
   - result_margin: Magnitude of victory by runs or wickets
   - eliminator: Y - if the match ends in a tie, the winner is decided by super over, N - if the match does not end in a tie, Match abandoned - if the match stands abandoned.
   - method: Y - if the duckworth-lewis method was used during the match, N - otherwise.
   - umpire1: First standing umpire in the match.
   - umpire2: Second standing umpire in the match.

## Ball-by-ball dataset (features/attributes)

   - MatchNo: It denotes the match number in the order of occurrence. 
   - inning: Inning no. of the match.  
   - over: Over no. of an innings. 
   - ball: Ball no. of an over. 
   - batsman : Batsman on strike.
   - non_striker: Batsman on non-striking end.
   - bowler: Bowler bowling the over.
   - batsman_runs: Number of runs scored by the batsman on the ball. 
   - extra_runs: Runs scored in the form of extras.
   - total_runs: Total runs scored of the ball.
   - is_wicket: If the batsman is dismissed or retired hurt of the ball. 
   - dismissal_kind: Type of dismissal.
   - player_dismissed: Player dismissed of the ball.
   - fielder: Fielder involved in the dismissal.
   - extras_type: Type of extras
   - batting_team : Team batting
   - bowling_team : Team bowling

### a) Data Cleaning

   Missing values have been filled appropriately as per the cricket records in match-by-match as well as ball-by-ball datasets to make all the entries non-null.

### b) Data analysis and visualization

   For analysis, numpy and pandas modules have been employed and for visualization seaborn, matplotlib and tabulate modules are used. On analyzing both the datasets, the below records are fetched:
   
   - Total wins for each team
   - Win/Loss ratio for each team
   - Runs comparison of Virat Kohli, Rohit Sharma and Mahendra Singh Dhoni for each of the years
   - Orange Cap winners for each year
   - Purple cap winners for each year
   - Most runs against each team by an individual
   - Most wickets against each team by an individual
   - Most sixes each year as well as overall (Top 10)
   - Most fours overall (Top 10)
   - Best strike rate for a batsman (with minimum 120 balls faced) (Top 10)
   - Total players to play for each team
   - Ratio of balls faced and boundaries scored by a batsman with a minimum of 150 balls faced (Balls per boundary) (Top 15)
   - Ratio of balls bowled and wickets taken by a bowler with a minimum of 350 balls bowled (Balls per wicket) (Top 15)
   - Most Player of the Match awards (Top 15)
   - Highest and narrowest margin victories (in terms of runs)
   - Highest and narrowest margin victories (in terms of wickets)
   - Run-rate for each team in powerplay and death overs (17-20) each year.
