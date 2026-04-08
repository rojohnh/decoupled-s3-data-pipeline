# Decoupled AWS S3 Data Pipeline & Headless Architecture

## Architectural Overview
This repository outlines the data engineering and headless cloud architecture required to process, organize, and serve massive datasets (600GB+) with $0 idle server costs.

By decoupling the heavy data layer from the frontend application, we achieve infinite scalability. The architecture ensures that millions of concurrent read requests hit AWS S3 and CloudFront CDNs rather than fragile monolithic databases.

## Pipeline Features
* **Automated Data Hydration Management:** Python-based automation designed to process cloud-stored assets locally without exhausting primary drive space using smart sampling.
* **EXIF Metadata Extraction:** Dynamically reads biological timeline data from raw image EXIF headers to construct chronological `manifest.json` files for the frontend application.
* **Headless Deployment:** Prepares perfectly structured directories (`YYYY/MM/DD`) ready for instant AWS CLI synchronization to public S3 buckets.

## The Business Value
This decoupled architecture guarantees 99.999% data durability, eliminates server CPU overload during massive traffic spikes, and reduces idle infrastructure CapEx to zero.
