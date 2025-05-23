 Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### General

#### Added
- New game variables/settings to `add_game` backend method
- `list_game_members` backend method
- `my_games` frontend method

#### Fixed
- Misc minor issues with both frontend and backend validation and docstrings

#### Changed
- Frontend and backend classes now require the database name
- Moved general overview/information from top of `stocks.py` to `readme.md`
- Moved sqlite helpers to separate script/module
- `_reformat_sqlite` methods now uses keys from database to map custom names
- All functions using `_reformat_sqlite` updated for new format
- Bumped backend version to 0.0.2
- `create` to `add` for most backend methods
- `list_users` now users sqlite helper functions
- Basic error handling to `add_user_to_game` backend method
- `create_game` to `new_game` in frontend


#### Removed
- Unneeded imports from `stocks.py`

### Database Creation (sqlite_creator_real)

#### Added
- Private game toggle (defaults to False)
- `status` to `game_participants`

#### Fixed
- Misc docstrings/descriptions

#### Changed
- Database name is now set in `.env` file
- `datetime_registered` to `datetime_created` in `users`
- `game_name` to `name` in `games`
- `game_status` to `status` in `games`
- `price_date` to `datetime` in `stock_price`
- `pick_status` to `status` in `stock_picks`

#### Removed
- idx_games Index
- Misc Todos

## [0.0.1] - 2025.04.29

### Added
- Changelog
- Readme
- _sql_get method for internal use to hopefully reduce redundancy
- add_stock_pick, list_stock_picks methods
- picks columns and custom columns/table option for _reformat_sqlite method
- Docstrings for methods list_users, list_stocks, get_stock, add_stock_price,
- Lots of placeholder methods
- create_game method now returns status
- Discord bot framework


### Fixed
- Data format for get_stock method

### Changed
- join_datetime to datetime_joined in game_participants table (SQLite DB)
- datetime_updated can no longer be null in stock_picks table (SQLite DB)
- username to display_name in add_user method
- get_stock and list_stock_prices methods now use _sql_get()
- Renamed StockGame class to Backend

### Removed
- Misc placeholders and completed todos

## [0.0.0] - Template

### Added

### Fixed

### Changed

### Removed