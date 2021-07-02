# S3 Performance Optimization

## Single PUT Upload

- Single data stream to S3.
- Stream fails = upload fails.
- Requires full restart.
- Speed and reliability = limit of 1 stream.
- Max 5GB upload.


## Multipart Upload

- Min size 100MB.
- Data is broken up.
- Max parts 10,000 -> 5MB => 5GB.
- Last part can be smaller than 5MB.
- Parts can fail and be restarted.
- Transfer rate = speed of all parts.


## Transfer Acceleration

- Off by default.
- Uses AWS network instead of ISP routing.
- Based on Edge Location.
