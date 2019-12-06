---
title: "Smoker Automation and Monitoring"
date: 2019-12-06T17:00:00-04:00
categories:
  - dadOps
tags:
  - dadOps
  - automation
  - metrics
  - devOps
  - cloud
  - rtl_433
  - rtl-sdr
  - bbq
  - wsm
  - weber
---

A few years ago I purchased a smoker. After my first few cooks I realized I needed a better view into what was going on during the sometimes 12+ hour cooks. I ended up building an automated temperature control system and a separate monitoring system using a raspberry pi, RTL-SDR dongle and a Thermo Pro wireless thermometer.

The temperature controller is built using a 3d printer cooling fan, a pet food bowl, a pid controller, wire and a few globs of jb weld to hold it all together.

Once the lit coals are placed in the smoker, we close off the other vents on the bottom and partially close the top lid. We want to starve the fire for oxygen to avoid a drafting scenario that causes the temperature to carry away. By limiting the airflow we give the pid controller full control of the smoker's oxygen and temperature as a byproduct.


The dashboard is built using Grafana. It can be configured to send Slack alerts if the smoker's cooking temperature falls outside of the desired range or if the probe for the food reaches the set temperature.




In part 2 we will discuss how we get the temperature from the wireless thermometer to Grafana.