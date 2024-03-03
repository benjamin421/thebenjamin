---
title: "Lab Insights"
date: 2023-07-11
draft: false
description: "Insights from setting up a lab from scratch and learning wet lab work."
slug: "lab"
subjects: ["Wet Lab", "Molecular Biology"]
showDate: false
showHeadingAnchors: true
showAuthor: true
showReadingTime: false
showEdit: true
showSummary: true
showPagination: true

---

{{< lead >}}
Last updated — February 2024 | Insights from setting up a lab from scratch and learning wet lab work.
{{< /lead >}}

## Introduction

This is a living document. I'm using it to drop tips and insights I've come across as I'm navigating the process of building out an independent lab and running my own experiments. 

Here's my current [lab spec](https://docs.google.com/spreadsheets/d/1_U8BmltdECJMfYgyDgldQfdFVstmoHeaHXaW7ajp764/edit?usp=sharing). 

Many of the below tips have come from conversations with others who've done this in the past. Special thanks to John Schloendorn and Philip Goetz who've provided the bulk of the input on buildout. Some of their direct comments have been included in the quote blocks below. 

Additionally, I am grateful to [Ichor Life Sciences](https://ichorlifesciences.com/) for hosting me for a 2 week training in their lab when literally dozens of academic labs turned me down. 

The old system is breaking. Let's try something new. 

## Setting Up an Independent Lab
### General Insights
1) Thorough planning is necessary before setting up a biolab. Don't just start buying equipment. Know what experiments you'll be attempting to run first. Watch YouTube videos on how equipment works, especially for the specific models you're considering buying. Marginal cost trade-offs can lead to huge trade-offs in terms of time cost and efficiency.
2) Consider cost-effective alternatives for space such as rented storage cubes, as renting traditional lab space is often more costly. In Saint Louis, [a basic space](https://cic.com/st-louis-lab-space) with limited shared equipment costs $2,000/mo.
3) Setting up automated eBay searches can help you find equipment more efficiently than checking for new listings regularly. 
4) >Don't make stuff that you can buy! This obsession of biohackers with making centrifuges and PCR machines is dumb. Those are easy to get. FAR more useful and practical (and easy) to make your own biosafety cabinet or PCR hood. That's about the only thing worth making yourself.
5) Be mindful of the challenges associated with cell culture and storage. More on this below.
6) Be cautious about purchasing outdated equipment for which disposables are no longer available.
7) Gaining visibility may attract government attention; take steps to reassure authorities about your activities. 
    >Call the local Sheriff early on and show him it's not a drug lab.  Just so he knows when that inevitable tip comes in.
8) Budget strategically, focusing on necessary equipment like PCR machines and electrophoresis and less on items like microscopes.

### Equipment and Consumables
1) Aim to pay about 1-2% of the new list price for used equipment. You won't always hit that range but I've quickly learned that lab equipment depreciates faster than a new car leaving the lot. 
2) Avoid specialty equipment, no matter how cheap. It will have limited information on how to use it and be expensive to repair. 
3) Paying a lot extra for equipment may be worth it if it lets you analyze smaller quantities, e.g. a Nanodrop.
4) Check return policies, software requirements, user manuals, and licenses before purchasing equipment.
    > 'No returns' is okay if the price is low enough. Most of the stuff sold by professional auctioneers that's untested, works. They honestly don't know how to test it. But do email them & tell them how to test it if it's really simple. Sometimes they'll offer to let you return it anyway if you ask BEFORE you buy.
5) Save auction photos with the serial numbers for equipment to potentially download the software for free.
7) Opt for durable analog equipment (1980s) over digital equivalents (1990s), with exceptions for advanced tech like qPCR and flow cytometry.
8) A standard refrigerator for cooling samples may be a cheaper and safer alternative than a refrigerated centrifuge.
    > You don't need more than like 5% accuracy with centrifuge speed, and the digital stuff breaks in shipping, and can be unusable without software.
9) The Stratagene Robocycler is the best PCR machine out there and is available on eBay for around $150.
10) Save money on an autoclave and buy [this](https://www.amazon.com/gp/product/B0000BYCFU/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) instead. 
11) Purchase balances for under $500 from Amazon and if you need less than 10 mg, just make a dilution.
12) > The Thermo e-gel system pays for the cost of the pre-cast gels easily, by being zero-mess and zero-time. You only need the base unit, not the camera. A cell phone can take the image just fine. Again Thermo's iBlot easily returns its consumable cost as time & mess saved, and then some.  Same for pre-cast protein gels. Make sure you understand the difference between DNA & Protein electrophoresis, and put them on the budget separately.
13) Utilize the [Henderson–Hasselbalch equation](https://en.wikipedia.org/wiki/Henderson%E2%80%93Hasselbalch_equation) as a substitute for a pH meter.
14) Avoid paying for calibration services; instead, purchase a calibration set for scales and pipettes. It is not hard. 
15) Platforms like Quartzy or LabSpend are recommended for managing reagent and consumable reordering efficiently.
16) Always procure reagents from quality suppliers. Buying poor quality will just add one more level of complexity to your troubleshooting. 
    - People I've been working with seem to trust [New England BioLabs](https://www.neb.com/en-us/) alot so I am ordering from them also. 
    - [Santa Cruz](https://www.scbt.com/home) has been mentioned to me as a less favorable supplier, especially for antibodies.

## Best Practices for Wet Lab

I use the jargon here. That's on purpose. I'm not going to define everything, but I will link to words that I wouldn't have known what they meant when I started. 

### Cell Culture Techniques
1) Cells need to be regularly [passaged](https://www.jove.com/v/5052/passaging-cells-cell-lines-subculturing-methods-and-applications) to prevent over-confluence, ensuring healthy growth and reproduction.
2) When pipetting media or similar substances into a cell culture, aim the liquid against the container wall to avoid cell damage and prevent pipette contamination from backspray/splashing.
3) Pre-wetting the pipette helps in achieving more accurate [aliquoting](https://www.merriam-webster.com/dictionary/aliquot). 
    - However, this should be avoided when [aspirating](https://www.merriam-webster.com/dictionary/aspirate) DNA.
4) Decant cells before media to allow the media to wash cells off of the container neck.
4) Pipette up and down to mix cells thoroughly before aspirating to seed a culture.

### Gene Delivery
1) When conducting transductions, use a vector that is homogeneous with the target cell to enhance efficiency.
2) Cells in serum-free media replicate slower due to less protein. It's advisable to use media without serum (e.g., FBS) during transduction/transfection to not interfere with the construct's uptake in the cells.
3) Perform tests with unloaded constructs to determine the optimal cell:virus particle ratio, AKA, 'MOI'. A similar principal applies to working with plasmids, etc in transfection. 
4) When centrifuging virus particles, orient the conical tubes with openings facing the center to be able to guestimate where pellets too small for the naked eye may be.

### Safety and Maintenance
1) Decontaminate everything that will enter the fume hood from the outside with 70% isopropyl alcohol to maintain a sterile environment.
2) Use quatricide to clean sterile hoods once every week or anytime after working with a virus to ensure sterility.

### Misc.
1) If encountering issues, blame your buffer first. Then blame yourself. Then scrutinize other factors.
2) Always include a positive control when working with antibodies to validate experimental results.
3) [Jove](https://app.jove.com/) is super helpful for protocols. 

---

Questions on any of the above or my experience doing this? [Send me an email](mailto:me@benjaminbanderson.com).