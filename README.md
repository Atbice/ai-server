# AI-SERVER

## Introduction
The journey began with our desire to experiment with training larger models. However, we quickly realized that such tasks would monopolize our own computers, leaving no room for fun during our freetime. Both of us share a deep interest in hardware and building computers, which led Anton to suggest a creative solution.

## The Genesis
Anton proposed building our own server specifically for model training. Anton had acquired a used Dell Precision 5600 a few years ago, which was otherwise just collecting dust. The initial plan was straightforward: purchase a used AI card, install it, and start running. This turned out to be easier said than done. We starded to research which used AI card to buy  and we started to get good sense of what we wanted.

![41S8fOo3mML](https://github.com/Atbice/ai-server/assets/134963203/c0c3119e-557c-493f-a261-253ef6d7500b)


## Early Challenges
In the meantime, the plan was to get the server running at Anton's house with just the cpu's to prepare for the AI card to come. After much trial and error, we successfully installed Proxmox, enabling remote access. Unfortunately, we then faced a significant challenge: the server was extremely loud! Anton's wife was particularly unhappy with this setup! :D But we're not ones to give up easily.

## Problem-Solving
We thought replacing the power supply unit (PSU) with a quieter one would be a simple solution. However, we encountered unexpected compatibility issues; servers and home computers use different types of PSUs, and Dell has its own standards, so no off-the-shelf PSU would fit our server chassis. Luckily, Robert had an extra-large chassis left over from a previous computer build, which seemed like the perfect fix to our problem. With determination, Robert transported this bulky behemoth by train and tram to Anton's place.

<img src="https://github.com/Atbice/ai-server/assets/134963203/481bee5b-982f-46ae-9a1f-9e1268e20ad8" alt="Descriptive Image Text" width="500">

## Power Supply Struggles
We purchased a new standard PSU that fit perfectly in the larger chassis. However, it quickly became apparent that the PSU cables were not compatible with our server's components due to Dell's proprietary standards. Undeterred, we decided to take matters into our own hands. Armed with wiring schematics we found online, we meticulously mapped out the voltage requirements for each cable. After careful planning and some trial-and-error, we deconstructed the server's original PSU and merged its wiring with the new PSU.

Lo and behold, it didn't work! 

<img src="https://github.com/user-attachments/assets/fd3bf494-9f92-4b45-8d95-955b295c1c5b" alt="Descriptive Image Text" width="300">
<img src="https://github.com/user-attachments/assets/ceb90d1a-d357-4a45-a96b-4c8c5a1dfd95" alt="Descriptive Image Text" width="300">

## The Chassis Modification
Our next challenge arose when we tried to mount the server's motherboard in the larger chassis. As luck would have it, none of the screw holes on the new chassis aligned with the motherboard's mounting points. After some brainstorming, we realized there was only one practical solution: modify the chassis itself.

This led to a bit of creative engineering. Using a grinder, we carefully cut out the bottom plate from the original Dell Precision 5600 chassis, which included the mounting points for the motherboard. Once removed, we transferred this plate to the larger chassis, effectively creating a custom mounting solution. It wasn’t the prettiest process, but it was undeniably satisfying to see our DIY approach take shape.

<img src="https://github.com/user-attachments/assets/a1590436-dfd1-4376-b67a-6ff7e0dcf26e" alt="Descriptive Image Text" width="400">
<img src="https://github.com/user-attachments/assets/634de1b6-4b37-4e1a-a3df-b9e752bceaf8" alt="Descriptive Image Text" width="300">


