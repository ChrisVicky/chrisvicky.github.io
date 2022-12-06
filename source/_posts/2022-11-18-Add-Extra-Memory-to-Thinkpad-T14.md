---
title: "Add Extra Memory to Thinkpad T14"
toc: true
categories:
    - Memo
tags:
    - Hardware
    - Performance Improve
    - DIY
---

Working on hard projects with Hadoop cluster really runs out the limit of my poorly configured laptop. Therefore, I decide to add an extra memory card to it to boost the performance.

## 1. Check the hardware information

* Before openning up the shell, we should figure out whether my laptop has an spare set for the extra memory and which memory card I should buy.
* To do that, we perform the following command to monitor the hardware status
```shell
sudo dmidecode memory > memory.log
```

<!-- more -->

<center>
    <img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"
        src="/img/image_2022-12-06-21-38-11.png"><br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;display: inline-block;color: #999;padding: 2px;">command output</div>
</center>

> note: I've accidentally remove `memory.log` which generated before adding the extra memory, and this screenshot is taken after the card is inserted.

* According to the output, the Maximun Capacity of Memory of my laptop is 32GB, meaning that it is capable of accepting an extra memory of 16GB.
* Another important information here is the speed. Because both memory cards will be accessed with the same bus, the slower speed could be a bottle net.
> I bought a memory card from Samsung with the same speed and data width for 300 RMB on Taobao.

## 2. Openning the Laptop

* Using tools from the shop, the laptop is rather easy to tear. The only thing to mention here is that, be gental not to break the machine down and after insertion, do not fix the screw before the evaluation process succeeds.

> In fact, the work can be down with a screwdriver and a student ID card.

## 3.  Evaluation

* After insertion, boot the machine and enter the Operatin System to check whether the extra Memory works well.

<center>
    <img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"
        src="/img/image_2022-11-18-11-20-48.png"><br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;display: inline-block;color: #999;padding: 2px;">Successfully Boot up Heavy Virtual Machines after Installation of the Additional 16GB Memory Card</div>
</center>


