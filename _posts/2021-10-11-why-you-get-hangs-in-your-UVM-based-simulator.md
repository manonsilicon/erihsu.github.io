---
layout: post
title: Why you get hangs in your UVM-based simulation
tags: [UVM]
---

I summerize some main reasons when you may see your testbench simulator hangs:

1. get hangs in agent-driver/monitor forever loops because there is no time consumed in the loop
2. clock event not triggered because your design may have **Latch**
3. get hangs in reference model beacause rfm usually require complex expression(like fork-join,forever)
4. TLM port task is blocked(get(),peek()) 