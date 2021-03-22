---
Title: Assignment 1
Subtitle: Computer performance, reliability, and scalability calculation
Author: Vikas Ranjan
---

## 1.2 

#### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes     |
| 1024x768 PNG image                         | 1 MB          |
| 1024x768 RAW image                         | 7.5 MB        | 
| HD (1080p) HEVC Video (15 minutes)         | 36 MB         |
| HD (1080p) Uncompressed Video (15 minutes) | 36000 MB      |
| 4K UHD HEVC Video (15 minutes)             | 228 MB        |
| 4k UHD Uncompressed Video (15 minutes)     | 228000        |
| Human Genome (Uncompressed)                | 1.5 GB        |

References:

1. One character is 1 byte, so 128 characters is 128 Bytes.
2. # of pixels is 1024 * 768 = 786,432 pixels. For RGB, every pixel in the image is 3 bytes. Therefore, the total file size would be 786,432 * 3 = 2,359,296 bytes which would be 2.25MB. PNG is compressed, I assume the compression ratio as 2, then the size is almost 1 MB. 
3. 1024 * 768 * 10/1024/1024 = 7.5MB
4. 900*30*1290*1080*8/8/1000/1024/1024 = 36 MB
5. 1000 times more than compressed.
6. 900*30*4096*2160*8/8/1000/1024/1024 = 228 MB
7. 1000 times more than compressed.
8. 6×10^9 base pairs/diploid genome x 1 byte/4 base pairs = 1.5×10^9 bytes or 1.5 Gigabytes

#### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 64 GB    |   1  |
| Daily Twitter Tweets (Snappy Compressed)  | 43 GB    |   1  |
| Daily Instagram Photos                    | 75 T     |  23  |
| Daily YouTube Videos                      | 104 TB   |  32  |
| Yearly Twitter Tweets (Uncompressed)      | 23 TB    |   7  |
| Yearly Twitter Tweets (Snappy Compressed) | 15 TB	   |   5  |
| Yearly Instagram Photos                   | 27375 TB |8213  |
| Yearly YouTube Videos                     | 37960 TB |11388 |

References:

1. Average total daily tweets ~ 500 million. The umcompressed daily storage needed is 500 million * 128 bytes, which is about 64,000,000,000 bytes, which is about 64 GB.
2. Snappy compression has a 1.5-1.7x ratio for plain text. Assuming if use 1.5x for all, compressed data size could result in about 43 GB.
3. The storage size is 0.75 * 100,000,000 * 1MB = 75,000,000 MB, which is about 75 TB.
4. The daily video is 500 hours * 60 * 24 = 720000 hours = 720000 * 60 minutes, which is 720000 * 4 per 15 minutes length. So the storage is about 720000 * 4 * 36 MB = 103,680,000 MB ~ 104 TB.
5. 64 GB * 365 = 23,360 GB ~ 23 TB.
6. 43 GB * 365 = 15,695 GB ~ 15 TB.
7. 75 TB * 365 = 27,375 TB.
8. 104 TB * 365 = 37,960 TB.

#### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | ??   |            |
| Twitter Tweets (Snappy Compressed) | ??   |            |
| Instagram Photos                   | ??   |            |
| YouTube Videos                     | ??   |            |

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 140.367 ms           |
| Low Earth Orbit Satellite | 40 ms                |
| Geostationary Satellite   | 240 - 280 ms         |
| Earth to the Moon         | 1300 ms              |
| Earth to Mars             | 3-21 minutes         |

Reference:

https://wondernetwork.com/pings
https://www.omniaccess.com/leo/#:~:text=The%20GEO%20latency%20is%20of,and%20an%20essential%20part%20if
https://www.satsig.net/latency.htm
https://www.spaceacademy.net.au/spacelink/commdly.htm

