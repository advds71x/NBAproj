---
layout: post
title: Code Documentation
nav-menu: true
permalink: /codedoc
---
## Rmarkdown and HTML Files
- Rmarkdown file: description.Rmd
- [Github Repo link](https://github.com/advds71x/nba_data_analysis)
- [Compiled HTML link](https://advds71x.github.io/nba_data_analysis/description)

### ./data
- game_stats_all.csv
- team_stats_all.csv
- post_62_games_pred.rds
- pre_20_games.rds


### ./nba_simulation_shiny
- ShinyApp source code
- [ShinyApp link](https://kate-yueyi-li.shinyapps.io/nba_simulation_shiny/)

### ./plots

### ./source
- EDA_visualize.R
- data_integration.R
- data_scraping.R
- data_wrangling.R
- feature_eng.R
- model_build.R
- simulation.R




## Wrap-Up Functions
- Data Scraping
    - `get_schedule_data(year,month)`: obtain the game schedules and results in specific year and month
    - `combine_game_data()`: combine the game schedules data
    - `get_team_stats(year)`: obtain the team-level data (30 teams in the league) of first 20 games in specific year

- Data Wrangling and Feature Engineering
    - `get_ws_data(year)`: obtain the win share data in specific year
    - `get_team_year_feature(year)`: obtain the team performance feature vectors in specific year
    - `get_game_year_feature(year)`: obtain the game results in tidy format in specific year
    - `get_injury_data(year)`, `combine_injury_data()`: obtain and combine the injury data

- EDA
    - `team_def_off_plot(year)`: show each team's defense vs offense in specific year
    -  `team_rank_plot(year,Nfirst)`: show each team's season rank vs first N games' rank in specific year
    - `home_way_plot(year)`: show each team's home and away records in specific year; show western vs eastern records
    - `team_ws_plot(year)`: show each team's highest winshare in specific year
    - `player_ws_plot()`: show the winshare of top players in the league in recent years

- Model Building
    - `get_train_test_data(year,firstN)`: obtain the training and test data of first N games in specific year.
    - `build_logit_model_year(train_year, test_year, firstN)`: use the first N games of train_year to build the model, and test the model on test_year. return the prediction results (W/L) and winning probability of each game.

- Integrative Prediction
    - `combine_season_data()`: combine the team performance feature data of multiple seasons
    - `team_pc_plot()`: create the PC plot for the team performances of all the 30 teams in multiple seasons; the distance matrix of season data
    - `team_cluster_plot()`: create the cluster plot for each team in multiple seasons
    - `win_prob_prediction(train_year, test_year,firstN,year_effect)`: The winning probability prediction function allow for year_effect

- Simulation
    - `WL_record_cal(game_schedule,WL_record)`: calculate the W/L records for each team given the game schedule
    - `game_simulation(pred_result,B,year,Nfirst)`: given the predict results in specific year, repeat the game simulation for B times
