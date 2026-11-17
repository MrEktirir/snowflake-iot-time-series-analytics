# IoT Time Series Analytics & Forecasting with Snowflake

## Project Overview

An end-to-end IoT time series analytics project implemented using Snowflake, covering data ingestion, transformation, analytical SQL, gap filling, and machine learning forecasting.

Based on the official [Snowflake Quickstart](https://www.snowflake.com/en/developers/guides/getting-started-with-time-series-using-snowflake-streaming-sis-ml-notebooks/).

## Architecture

IoT Sensor Simulator → Snowpipe Streaming → Raw Data → Dynamic Tables → Analytics Views → Time Series Analysis → ML Forecasting

## Technologies

- Snowflake
- Snowpipe Streaming
- Dynamic Tables
- SQL Time Series Functions
- ASOF JOIN
- Snowflake ML Forecast
- Java IoT Simulator
- GitHub Codespaces

## Implementation

### 1. IoT Data Ingestion

Streamed 1,733,760 simulated IoT sensor records into Snowflake using a Java streaming client.

### 2. Data Transformation

Created incremental Dynamic Tables to transform raw IoT events into structured sensor metadata and readings.

### 3. Time Series Analytics

Performed statistical analysis, window functions, moving averages, time-based rolling averages, and five-minute downsampling.

### 4. ASOF JOIN

Aligned sensor readings collected at different frequencies using timestamp-based matching.

### 5. Gap Filling

Generated regular time intervals and applied Last Observation Carried Forward (LOCF) to fill missing observation points.

### 6. Machine Learning Forecasting

Trained a `SNOWFLAKE.ML.FORECAST` model using historical TAG401 sensor measurements and generated 1,440 future predictions.

Visualized historical readings alongside predicted values and uncertainty bounds.

### 7. Snowflake Copilot

Attempted the natural-language SQL workflow, but the account reported that Cortex Code was not enabled or its usage limit had been reached.

## Key Outcomes

- 1.7M+ IoT events ingested
- Incremental transformation pipeline implemented
- Multiple time series analysis techniques explored
- Sensor readings synchronized with ASOF JOIN
- Missing observation points handled using LOCF
- 24-hour sensor forecast generated

## Reference

[Official Snowflake Time Series Quickstart](https://www.snowflake.com/en/developers/guides/getting-started-with-time-series-using-snowflake-streaming-sis-ml-notebooks/)