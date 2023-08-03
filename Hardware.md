# Hardware

### Overview:

* What coding languages will be used?
* Will we take pictures or videos?
* The creation of a possible miniature version to check the camera angle
* What resolutions are possible with the processing power of the Pi?
* What Raspberry Pi version can handle the needed resolutions?
* Is there a Shield for our needs?
* What case will we use? Water resistance is important due to rain
* How will we handle the cooling of the system?
* What type and size of battery will be needed? We should be able to run for around 12 hours
* Is there a shield that uses SIM Cards
* How will we make sure to sync the internal times of the Pis?

<br>

### Coding Languages:

<br>

### Pictures / Videos:

<br>

### Possible / Needed Resolutions:

<br>

### Different Raspberry Pi Versions:

When choosing a Raspberry Pi Version to work with, we need to take a few different values in account. This includes:

* performance
* energy consumption
* price
* availability of shields

<br>

##### Performance

The most important part of the overall performance is the CPU. In the following diagram the CPU performance is better with the newest model of the Pi, but due to product shortages and higher prices, the Pi 3B+ is still an option to keep in mind. The Pi 4B gets the best performance in most aspects such as CPU, GPU, RAM and USB Throughput.

<img src="Hardware_files/RaspberryPi_Benchmark.png" alt="RaspberryPi_Benchmark" style="width: 40%;" />

In an image-recognition-experiment conducted by the website arrow.com, it was concluded that there is a 20% performance increase from the Model 3B+ to the Model 4, resulting in a difference of approximately 0.9 seconds in their specific setup. It is important to note that these values may drastically increase by using specialized algorithms and specifications.

<br>

##### Specifications

This table describes the difference between the two models in question. In some tests it shows a huge difference, in the parts most important for this project, they perform almost the same. The size and the layout are the same for both, so most shields can be reused, but cases will need to be changed due to the ethernet port bing moved and the full size HDMI port being replaced by two micro HDMI connectors. <br>
The peak power consumption for the Pi3 is ~5.7 Watts and ~5.6 Watts for the Pi4 at their peak. <br>

<img src="Hardware_files/RaspberryPi3vs4.jpeg" alt="RaspberryPi3vs4" style="width: 40%;" />

The pricing shows the Raspberry Pi 3B as the overall cheapest model.


| Product                     | Price    |            |
| :---------------------------- | ---------- | ------------ |
| Raspberry Pi 4 Model B 4GB  | 78.99€  | Amazon.com |
| Raspberry Pi 4 Model B 8GB  | 126.04€ | Amazon.com |
| Raspberry Pi 3 Model B 1GB  | 51.21€  | Amazon.com |
| Raspberry Pi 3 Model B+ 1GB | 77.99€  | Amazon.com |

[^1]

<br>

##### Conclusion

Overall can be said that the RaspberryPi3B is the better option for this project, due to a lower price range. While still a great product, the increased performance of the RaspberryPi4, does not justify the higher prices in the case of our specific project.

<br>

### Shields:

<br>

### Housing / Water Resistance:

<br>

### Cooling:

<br>

### Power Consumption / Battery:

<br>

### Internal Time Synchronization:

<br>

##### Sources:

* [https://magpi.raspberrypi.com/articles/raspberry-pi-4-specs-benchmarks](https://magpi.raspberrypi.com/articles/raspberry-pi-4-specs-benchmarks)
* [https://www.arrow.com/en/research-and-events/articles/image-recognition-speed-comparison-google-coral-edge-tpu-pi-3b-plus-vs-raspberry-pi-4](https://www.arrow.com/en/research-and-events/articles/image-recognition-speed-comparison-google-coral-edge-tpu-pi-3b-plus-vs-raspberry-pi-4)
* [https://core-electronics.com.au/guides/raspberry-pi-4-vs-3-model-b-performance-benchmark/](https://core-electronics.com.au/guides/raspberry-pi-4-vs-3-model-b-performance-benchmark/)
*

[^1]: The Model B and B+ perform almost the same in the, for this project, important aspects, so they are treated as an equal here.
