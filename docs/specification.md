# Specification
This documents outlines the high level requirements for the OpenO2 Oxygen Concentrator for it to be most useful in a low resource setting. This is a live document and we are actively seeking feedback on these requirements and welcome your input.


## References 
* EN ISO 80601-2-69:2014 – Medical electrical equipment – Particular requirements for basic safety and performance of oxygen concentrator equipment Safety requirements
* EC 60601-1 – Medical electrical equipment – General requirements for basic safety and essential performance 
* EN ISO 8359:1996 – Oxygen concentrators for medical use – Safety Requirements
* [The clinical use of oxygen in hospitals with limited resources: Guidelines for health-care workers, hospital engineers and managers, WHO, Trevor Duke, May 2009](https://instructure-uploads.s3.amazonaws.com/account_100000000083919/attachments/23344297/Ortiz-The%20Clinical%20Use%20of%20Oxygen%20in%20Hospitals%20with%20Limited%20Resources.pdf?response-content-disposition=attachment%3B%20filename%3D%22Ortiz-The%20Clinical%20Use%20of%20Oxygen%20in%20Hospitals%20with%20Limited%20Resources.pdf%22%3B%20filename%2A%3DUTF-8%27%27Ortiz%252DThe%2520Clinical%2520Use%2520of%2520Oxygen%2520in%2520Hospitals%2520with%2520Limited%2520Resources.pdf&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJDW777BLV26JM2MQ%2F20200421%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20200421T092851Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=b4eb14df9da9b6579e17bd8e9fec9bcbeaaea6061a63618c9cd0159f37f6fe69)
* [Technical Specification For Oxygen Concentrators, WHO, 2015](https://apps.who.int/iris/bitstream/handle/10665/199326/9789241509886_eng.pdf?sequence=1)
* [Oxygen sources and distribution for COVID-19 treatment centres](https://www.who.int/publications-detail/oxygen-sources-and-distribution-for-covid-19-treatment-centres?fbclid=IwAR1B0VxtdrTNUBtNgtRuHSQHZ_girqXmVe81hs2RBdSP_SqgYuMoWELKZaU)
* [Evaluation of oxygen concentrators for use in countries with limited resources, D. Peel  R. Neighbour  R. J. Eltringham, May 2013](https://doi.org/10.1111/anae.12260)
* [PATH, Design for reliability: Ideal product requirement specifications for oxygen concentrators for children with hypoxemia in low- resource settings](https://path.azureedge.net/media/documents/DT_oxygen_concentrators_ideal_design.pdf) 


Below we highlight some key points from some of the above references that will inform the design process.

## Overview
Oxygen concentrators take air from the environment (~21% oxygen) and output concentrated oxygen (>82%) which can be delivered to hypoxemic patients. The reliable operation of oxygen concentrators in low-resource settings is limited by:
* Intermittent and power quality;
* a lack of access to spare replacement parts;
* lack of trained maintenance personnel; * hot, humid, and often dusty environments which affect the performance and useful life of the devices.

This document focuses on the device which produces the oxygen, additional breathing apparatuses is required to connect the output of oxygen to the patient. 

## User Profile and Environment of Use
The oxygen concentrator should be suitable for use in lower-level health care facilities in LRS. Clinically trained staff are on site; however, technical maintenance staff or engineers are rarely available. Lack of assigned or otherwise sufficiently trained personnel to conduct maintenance, high staff turnover, and lack of training programs translates to most devices not receiving the preventative maintenance required to function properly. Furthermore, replacement parts are often in scarce supply, and supply and maintenance infrastructure are rarely present, resulting in device underutilization or failure. Although pulse oximetry is an essential tool for early detection of hypoxemia and in guiding oxygen therapy, its availability and widespread use is often scarce in LRS.

Intermittent and unstable power as well as harsh hot and humid environments present challenging operating conditions that often cause premature failure of oxygen concentrators in LRS. The power quality at these facilities is poor and characterized by the occurrence of frequent power fluctuations and surges. Voltage sags and spikes often occur for a few minutes each time. Backup power sources are also often unreliable. We assume a minimum of 4 hours of power outages frequently encountered each day, which may last up to 22 hours. In addition, the majority of health care facilities above sea level to as high as 2,000 meters often experience harsh ambient conditions, including high temperatures (up to 40°C) and high humidity (up to 95%) simultaneously. Average low temperatures can fall between 5°C and 10°C. Health care facilities at altitudes above 2,000 meters experience cooler temperatures, lower atmospheric oxygen levels, reduced barometric pressures, and less humid conditions. Lastly, very dusty or sooty environments and unhygienic conditions are also common to LRS.

## Modes of Failure of Oxygen Concentrators
It's useful to know how existing models fail as we seek to design a system that is robust. These are some of the failure modes reported by PATH along with a desired behaviour of a system for LRS:

| Failure Mode | Ideal behaviour |
| -------------|-----------------|
|Power outages stopping oxygen delivery, with backup power systems expensive to buy and maintain.| Uninterrupted oxygen flow for 4 patients |
|Harsh operating environments can cause damage to internal electrical components (e.g., valves, compressor, sieve beds, and printed circuit boards) | Robust system, which operates well under harsh environments characterized by high temperature, humidity, and dust. Made using standard parts to facilitate maintenance |
|Frequent power spikes, power sags, and distortions can cause damage or stop oxygen concentrators | The device should be able to operate with poor power quality/on solar/without electrical power |
|Ongoing costs of the oxygen expensive.| Reliable, able to fix with locally available parts |

## Technical Requirements
These are the requirements that need to be taken into account to design a device that is both reliable, safe and useful in a clincal setting. Please see the article by PATH referenced above: [Design for reliability](#references).

## Evalulating your design
Here are some important parameters that we need to use to assess our designs:
1. **Cost**: designs need to be at least cost competitive with existing technology.
2. **High Operating Temperature**: A number of units don't work well at 40°C, it is important design for LRS do continue to work at these temperatures.
3. **High Operating Relative Humidity**: Units need to continue to operate effectively at 95% relative humidity.
4. **Low Power Consumption and Off-grid**: devices need to givea good oxygen flow at the lowest possible power consumption, and at least be competive with existing devices. They need to be able to operate in an off-grid setting, without reliable access to electricity.
5. **Reliability**: devices need to be robust, but also easy to maintain, when required.
6. **Maintenance**: ideally devices should be made, as far as possible, from standard parts to aid repair and maintance.

