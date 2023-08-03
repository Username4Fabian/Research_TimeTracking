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

#### Performance

The most important part of the overall performance is the CPU. In the following diagram the CPU performance is better with the newest model of the Pi, but due to product shortages and higher prices, the Pi 3B+ is still an option to keep in mind. The Pi 4B gets the best performance in most aspects such as CPU, GPU, RAM and USB Throughput.

<img src="Hardware_files/RaspberryPi_Benchmark.png" alt="RaspberryPi_Benchmark" style="width: 40%;" />

In an image-recognition-experiment conducted by the website arrow.com, it was concluded that there is a 20% performance increase from the Model 3B+ to the Model 4, resulting in a difference of approximately 0.9 seconds in their specific setup. It is important to note that these values may drastically increase by using specialized algorithms and specifications.

<br>

#### Specifications

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

#### Conclusion

Overall can be said that the RaspberryPi3B is the better option for this project, due to a lower price range. While still a great product, the increased performance of the RaspberryPi4, does not justify the higher prices in the case of our specific project.

<br>

### Shields:

<br>

### Housing / Water Resistance:

<br>

### Cooling:

<br>

### Power Consumption / Battery:

In oder to calculate the power consumption, I am going to use the estimated values calculated earlier in the "specifications"

> The peak power consumption for the Pi3 is ~5.7 Watts and ~5.6 Watts for the Pi4 at their peak.

To compensate for potential losses and power fluctuations, the power consumption will be rounded up to 6 Watts. The final version of the time tracking system should be able to run for approximately 10 hours to ensure that an entire event can be tracked. The common standard for batteries of the required size is 12V, which is chosen due to its better accessibility and lower price. <br>

The RaspberryPi only uses 5V so a transformer is needed. The average efficiency of a small transformer is ~70%, so this will be part of the calculation as well. <br>

The steps to calculate the necessary battery size are as follows:

* Total energy consumption over 10 hours = Power x Time = 6 watts x 10 hours = 60 watt-hours
* Battery Capacity for 10 hours of Operation: Total watt-hours / Battery Voltage = 60 watt-hours / 12 volt = 5Ah
* Adjust for the power loss during 12V to 5V transformation: Power × (1 / efficiency) × Time = 6 watts × (1 / 0.7) × 10 hours ≈ 85.71 watt-hours
* Adjust further for power loss: New total watt-hours / Battery Voltage = 85.71 watt-hours / 12 volts ≈ *7.14 Ah*.

It is important to note that this is only a rough overview of the needed battery size. In reality the power consumption may variate due to the Pis power fluctuating power consumption.

<br>

With this information, a battery capacity of at least 8Ah is needed, although a buffer should be considered.

Possible options are:


| Product                      | Capacity | Price   | Product-Link                                                                                                                                                                                                                                |
| ------------------------------ | ---------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Green Cell® AGM 12V 8Ah     | 8 Ah     | 29.09€ | [Amazon.de](https://www.amazon.de/Green-Cell-Akkubatterie-Alarmanlage-Taschenlampen-12V-8Ah/dp/B08JGYXMNS/ref=sr_1_5?__mk_de_DE=ÅMÅŽÕÑ&crid=1I2LO8EP05RMP&keywords=12v+8ah&qid=1691100512&sprefix=12v+8+ah+%2Caps%2C112&sr=8-5https:/) |
| EMOS Wartungsfreier Bleiakku | 9 Ah     | 20.06€ | [Amazon.de](https://www.amazon.de/EMOS-Wartungsfreier-Bleiakkumulator-faston-B9675/dp/B01MQJTOHB/ref=sr_1_5?__mk_de_DE=ÅMÅŽÕÑ&crid=IK9SNX1N1DIC&keywords=12v%2B9ah&qid=1691100807&sprefix=12v%2B9ah%2Caps%2C130&sr=8-5&th=1https:/)    |
| Green Cell® AGM 12V 10Ah    | 10 Ah    | 29.20€ | [Amazon.de](https://www.amazon.de/Green-Cell-Akkubatterie-Alarmanlage-Taschenlampen-12V-10Ah/dp/B08JGYY8KN/ref=sr_1_5?__mk_de_DE=ÅMÅŽÕÑ&crid=32XB0R04X91SG&keywords=12v+10ah&qid=1691100894&sprefix=12v+10ah%2Caps%2C136&sr=8-5)       |

The best option here would be the **EMOS 12V 9Ah lead acid battery** with a weight of 2.42kg.

<br>

### Internal Time Synchronization:

<br>

##### Sources:

* [https://magpi.raspberrypi.com/articles/raspberry-pi-4-specs-benchmarks](https://magpi.raspberrypi.com/articles/raspberry-pi-4-specs-benchmarks)
* [https://www.arrow.com/en/research-and-events/articles/image-recognition-speed-comparison-google-coral-edge-tpu-pi-3b-plus-vs-raspberry-pi-4](https://www.arrow.com/en/research-and-events/articles/image-recognition-speed-comparison-google-coral-edge-tpu-pi-3b-plus-vs-raspberry-pi-4)
* [https://core-electronics.com.au/guides/raspberry-pi-4-vs-3-model-b-performance-benchmark/](https://core-electronics.com.au/guides/raspberry-pi-4-vs-3-model-b-performance-benchmark/)
* [https://amazon.deAmazon.de](https://amazon.de)
* [https://chat.openai.com](https://chat.openai.comhttps:/)

[^1]: The Model B and B+ perform almost the same in the, for this project, important aspects, so they are treated as an equal here.
