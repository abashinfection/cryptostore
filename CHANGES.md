## Changelog

### 0.3.2
  * Bugfix: Fix book building example
  * Feature: Ability to pull config file from S3 bucket instead of local filesystem, polling for updated config is supported.
  * Feature: Updated to work with latest version of cryptofeed
  * Feature: Liquidations support for Arctic
  * Bugfix: Aggregating parquet files at the end of time no longer causes file not found error.
  * Feature: Temporary parquet files are now gathering in a seperate folder
  * Bugfix: Parquet column type fix
  * Bugfix: Fix issue where max depth was being passed incorrectly to cryptofeed
  * Bugfix: rename kafka host kwarg to bootstrap, as cryptofeed backend expects
  * Feature: Candles support

### 0.3.1 (2020-11-14)
  * Feature: Influxdb 1.x authentication support
  * Bugfix: Extend timeout of Google Drive connection
  * Feature: Parquet file compression
  * Feature: Parquet file content optimization
  * Feature: Option to enable parquet file appending
  * Feature: Retry writes to storage engines (rather than dying).
  * Feature: Support for snapshot_interval
  * Feature: Parquet files can be stored in directories per day
  * Bugfix: Set arctic storage quota to unlimited (rather than 10G)
  * Bugfix: Regression in arctic storage backend
  * Feature: Opened parquet files (when appended) are suffixed with '.tmp'
  * Feature: Liquidations support

### 0.3.0 (2020-08-18)
  * Feature: Config options for controlling data channel timeouts
  * Feature: Path option in config for local parquet storage
  * Feature: Configurable filenames for parquet storage
  * Bugfix: Ticker missing from ZMQ pass through
  * Feature: Store data to Google Drive
  * Bugfix: Kafka now supports the time interval for storage intervals (feature added in 0.2.1)

### 0.2.1 (2020-03-17)
  * Feature: Open Interest support
  * Example: Added example code for orderbook reconstruction from data in Arctic
  * Feature: More granular control over data storage intervals
  * Feature: Support receipt timestamps from cryptostore
  * Example: Added example code for ZMQ passthrough

### 0.2.0 (2020-02-11)
  * Bugfix: Fixed elasticsearch timestamps
  * Feature: Support for different S3 endpoints to allow writing to other providers
  * Bugfix: Missing config value for redis socket

### 0.1.1 (2019-11-27)
  * Feature: Rework backfill to operate even when store's data differs
  * Bugfix: Log exception/traceback when aggregator process dies
  * Feature: Support for max book depth via `max_depth` parameter.
  * Feature: Funding data support
  * Bugfix: Kraken trades not storing correctly
  * Bugfix: Book delta interval between snapshots not correctly read from config

### 0.1.0 (2019-08-21)
  * Feature: Elasticsearch support
  * Feature: Data passthrough support
  * Feature: Config for book data is more granular
  * Feature: Data retention time for Redis data

### 0.0.8 (2019-07-06)
  * Feature: Trade Data backfill
  * Bugfix: Stop storing extra column in arctic
  * Feature: Plugin interface to allow configurable 3rd party/non core functionality
  * Feature: InfluxDB Support
  * Bugfix: Ensure numeric data stored in parquet is as float
  * Feature: Rotating file logger

### 0.0.7 (2019-05-23)
  * Bugfix: Trades not working correctly with redis aggregator
  * Feature: Book delta support

### 0.0.6 (2019-05-19)
  * Feature: Kafka support

### 0.0.5 (2019-05-08)
  * Feature: Install entry point script with setuptools
  * Bugfix: Incorreclty storing level/order size in book updates in Arctic
  * Bugfix: Optional dependenices no longer required to be installed
  * Feature: Redis decoupled from aggregator, in preparation for the caching backend to be user selected

### 0.0.4 (2019-05-04)
  * Bugfix: missing comma in setup.py
  * Feature: S3 support
  * Feature: Command line option, --config/-c to provide path to configuration

### 0.0.3 (2019-05-02)
  * Initial Alpha Release - data storage to arctic, parquet and google cloud storage

### 0.0.1/0.0.2 (2019-04-14)
  * Pre-alpha, experimental release
