#Module 3 - Homework

-- Creating external table referring to gcs path
CREATE OR REPLACE EXTERNAL TABLE `grounded-primer-411515.ny_taxi.external_green_tripdata`
OPTIONS (
  format = 'parquet',
  uris = ['https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-01.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-02.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-03.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-04.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-05.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-06.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-07.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-08.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-09.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-10.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-11.parquet',
  'https://storage.cloud.google.com/mage-zoomcamp-mboulanger/HW-WEEK3-GREEN-TAXI-DATA-2022/green_tripdata_2022-12.parquet'
  ]
);


##Question 1
SELECT count(*) FROM `grounded-primer-411515.ny_taxi.external_green_tripdata` 

##Question 3

SELECT count(*) FROM `grounded-primer-411515.ny_taxi.external_green_tripdata` WHERE fare_amount=0

