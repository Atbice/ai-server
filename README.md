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

## Switching to a Server Rack
After putting significant effort into modifying the larger chassis, we felt optimistic that everything was finally coming together. However, upon booting the system, we hit another major roadblock: the GPU was not being detected. No matter what we tried—reinstalling drivers, re-seating the card, checking the BIOS—the system refused to recognize the GPU. Our best guess was that the motherboard was simply too old to support the newer GPU hardware. Disheartened but determined, we decided to pivot.

The best solution seemed to be investing in a proper server rack. After scouring online listings, we found a used Dell PowerEdge R730 that fit our needs perfectly. It was designed to handle dual GPUs, had robust server-grade components, and was a significant upgrade from our previous setup. Plus, since our GPUs were originally designed for rack-mounted systems, the R730 was a logical choice.

<img src="https://github.com/user-attachments/assets/84512c6f-af89-40f0-96b2-e5ac99c7ded3" alt="Descriptive Image Text" width="400">

## Success: GPUs Detected!
After setting up the PowerEdge R730 and installing both GPUs, we held our breath as we booted the system. When we checked the terminal, both GPUs were detected! The excitement was tangible—we had overcome one of the biggest hurdles we’d faced so far. It finally felt like all of our hard work and problem-solving was paying off.

<img src="https://github.com/user-attachments/assets/a7b07077-8cb0-44ec-b2a8-79f5f49ecf97" alt="Descriptive Image Text" width="300">

## Getting CUDA to Work
The next step was installing and configuring CUDA, which is essential for AI model training. CUDA can often be tricky to set up, with potential issues ranging from driver mismatches to dependency conflicts. Fortunately, having struggled with CUDA in the past, we had a lot of experience resolving these issues. This time, everything went relatively smoothly, and before long, we had CUDA fully operational.

With both GPUs now running CUDA, we were able to train and generate AI models efficiently. Watching the server utilize the full power of both GPUs for AI workloads was immensely satisfying. Everything seemed to be working perfectly.



## The Noise Problem
While the PowerEdge R730 was a solid choice in terms of performance, it introduced a new challenge: noise. Rack-mounted servers are notoriously loud, and both of our wives quickly made it clear that this wasn’t acceptable as a permanent solution.

To address the noise issue temporarily, we decided to move the server to Robert's basement. This provided a much-needed buffer from the sound, allowing us to test and set up the system without disturbing anyone in our homes. It wasn’t the ideal long-term solution, but it gave us the time and space we needed to figure out a quieter, more permanent setup.

<img src="https://github.com/user-attachments/assets/1aab9834-b072-4cf3-ae5d-5301131cea81" alt="Descriptive Image Text" width="300">

## A More Permanent Solution: Relocating to an Outbuilding
Thanks to Robert’s parents, we found a more permanent solution: one of their outbuildings. It was an ideal location for the server rack—away from living spaces and the constant complaints about noise. There was, however, a minor downside: we had to rely on a mesh router for connectivity. While the mesh router wasn’t slow for everyday use, the large AI models we often needed to download made the network speed feel less than ideal. Still, it was a small trade-off for finally having a dedicated space for our setup.

<img src="https://github.com/user-attachments/assets/3efc4806-3f1a-4751-9a30-5363ef994954" alt="Descriptive Image Text" width="300">

## Dealing With Heat
As we got everything up and running in the outbuilding, we encountered another problem: heat. Rack-mounted servers like the Dell PowerEdge R730 generate a significant amount of heat during operation, and the outbuilding wasn’t designed to handle it. Over time, the heat buildup became a real issue.

Our improvised solution involved redirecting the airflow from the server fans using tarpaulin to guide the hot air out of the building. It wasn’t the most elegant solution, but it worked well enough to keep the server operational without overheating. While not perfect, it was a testament to our resourcefulness and determination to keep things running.

<img src="https://github.com/user-attachments/assets/fd283076-05df-4648-a30b-91fdf0581a27" alt="Descriptive Image Text" width="300">

## Conclusion
What started as a simple idea to experiment with training larger AI models turned into an ambitious and challenging journey. Along the way, we faced numerous obstacles—from loud servers and incompatible power supplies to motherboard mounting issues and GPU detection problems. Each challenge pushed us to think creatively, adapt quickly, and learn more about hardware and server optimization than we ever expected.

In the end, our AI server is more than just a tool for training models—it's a symbol of persistence, problem-solving, and collaboration. From repurposing an old Dell Precision 5600 to finally settling into a dedicated outbuilding with a Dell PowerEdge R730, every step taught us something new.

While it's far from a perfect setup—with some compromises like slower network speeds and heat management—it works. And most importantly, it allows us to focus on what we originally set out to do: train and experiment with AI models.

The journey may have started as a practical solution, but it became a passion project that reflects our shared love for building, learning, and creating. And who knows? This might just be the foundation for something even bigger in the future. For now, we're proud of what we've accomplished—and excited to see where this server takes us next.
