---
layout: single
title: "When will AI Agents work for Renewable Monitoring?"
categories: blog
tags:
  - Solar
  - Business
  - Infrastructure
  - Sales
  - AI
  - English
classes: wide theme-dark
date: 2024-10-01 10:46:57 +0100
excerpt: After many years of experience in the Asset Performance Management (APM) field, one key lesson has become clear; without a reliable...
header:
  overlay_image: /assets/images/mcp.jpg
  teaser: /assets/images/mcp.jpg
---

# When will AI Agents work for Renewable Monitoring?

Wouldn't it be beautiful if we could ask our solar datalogger or SCADA something like, _"Hey, how much have I produced this month?"_ in natural language?

Or even better, hearing Siri remind us with voice to plug in our car since the electricity price is very low or zero at that moment. Or receiving a payment at the end of the month from our small battery system that automatically charges or discharges based on market prices, weather forecasts, and more.

Wouldn't it be beautiful to see a control center for a medium-sized IPP managing a handful of GW of renewable installations with just a couple of humans, or none at all? Imagine a dedicated AI agent continuously benchmarking data, providing recommendations and insights such as: _"Strings #10 to #15 need cleaning; production is lower than expected based on corrected irradiation values interpolated from plant stations and satellite data."_ And even dispatching a local robot or calling a human technician from O&M, clearly explaining the issue via a voice conversation.

Although this might still sound like science fiction, I strongly believe I'll witness it in my lifetime. Actually, we already have all the tools and basic research needed. They just need implementation. The reason it's not here yet is primarily due to insufficient manpower and developers to utilize these tools fully.

Some people remain wary of AI, and others laugh at it when the results are humorous—like AI-generated images with extra fingers or Will Smith eating spaghetti. Others argue it's not truly intelligent. **I agree, AI isn't intelligent _as humans are_. They are powerful tools, from now.** Humans are the supreme species due to our historical capacity to create tools to cope with our limitations, creating specialized tools for specific purposes. Just as a hammer is perfect for driving a nail but not removing it, AI models excel in tasks they're trained for.

Expecting a multipurpose tool or intelligence like AGI (Artificial General Intelligence) is currently unrealistic. Creativity or consciousness is even further away. Yet, agents trained for specific tasks, acting as cheap robotic manpower, are already here.

> LLM models need connections to reality—they need to understand _"what is out there."_

We already know what LLMs are capable of, and each new model release from OpenAI, Google, Claude, etc., continues to amaze us. But these models need connections to reality—they need to understand _"what is out there."_

### The Role of MCP (Model Context Protocol) in Bridging AI and Reality

This is the purpose of the MCP (Model Context Protocol). MCP was released last November by Anthropic, a leader in AI, and since then, major companies like Stripe, Microsoft, OpenAI, and IBM have adopted it. MCP is a natural evolution of what OpenAI introduced with its Custom GPTs, capable of interacting via API endpoints (called [actions](https://platform.openai.com/docs/actions/introduction)).

MCP evolves the concept of APIs (Application Programmatic Interface), which expose platform data and functionalities for machine interaction but have limitations due to fixed responses and documentation requirements. MCP allows an AI Agent (like ChatGPT) to dynamically discover and understand system capabilities without needing API documentation. See here a better explanation from IBM experts:

[Embedded video: _MCP vs API: Simplifying AI Agent Integration with External Data_](https://www.linkedin.com/embeds/publishingEmbed.html?articleId=8162368961979513161&li_theme=light)

For instance, when a client wants to know their solar installation's monthly production, they typically contact the datalogger via a specific API endpoint:

```bash
api.solarbrand.com/getHistoricData?variable=power&startDate=2025-05-01&endDate=2025-05-29
```

This endpoint definition varies from system to system, requiring developer-provided documentation. MCP simplifies this with a wrapper:

```javascript
app.post("/mcp/query", async (req, res) => {
  let mcp_context = req.body.mcp_context;
  let intent = parseIntent(mcp_context.user_query);

  if (intent === "production_by_month") {
    let { fromDate, toDate } = extractDates(mcp_context);
    let api_response = await callAPI("/getHistoricData", {
      variable: "power",
      startDate: fromDate,
      endDate: toDate,
    });

    mcp_context.result = api_response.data;
    mcp_context.units = api_response.units;
    mcp_context.api_calls = [
      `/getHistoricData?variable=power&startDate=${fromDate}&endDate=${toDate}`,
    ];
  }

  res.json({ mcp_context });
});
```

The MCP tells the AI Agent how to use the API based on the provided context, as well as what data it is receiving and in what format. After that, the AI Agent may need to sum the values and perform a conversion. It might also need to call different services to retrieve market prices and carry out an hourly multiplication— if the client requests the result in monetary terms in a subsequent question.

MCP's advantage is flexibility. Rather than programming rigid workflows, AI agents adapt dynamically, potentially making traditional monitoring platforms obsolete.

> I envision a future _beyond_ rigid SaaS monitoring platforms.

I envision a future beyond rigid SaaS monitoring platforms with fixed feature roadmaps. Instead, smart AI agents will communicate via MCP directly with the systems, trained with terabytes of operational data from similar plants. They will model and onboard plants simply by uploading the "as-built" project documentation and guide field technicians by voice, WhatsApp calls, or even generate explanatory images _on-the-fly,_ or interact via augmented reality.

This aligns with Satya Nadella's claim that [SaaS will collapse](https://youtu.be/9NtsnzRFJ_o?si=-Y37nyXG8keCfT66&t=2804), something I didn't understand at first, but now I do.

A silent revolution is underway. The smarter kids on the room are already implementing MCPs for more attractive, higher-margin markets. Companies like Stripe, HubSpot, and Spotify are enabling MCP servers so AI agents can interact with their data, opening new monetization opportunities.

### Challenges and Opportunities in the Renewable Sector

For the renewable sector, the question remains: **_When will [Huawei](https://www.linkedin.com/company/huawei/), [SMA Solar](https://www.linkedin.com/company/sma-solar/), [GreenPowerMonitor, a DNV company](https://www.linkedin.com/company/greenpowermonitor/), [meteocontrol](https://www.linkedin.com/company/meteocontrol/), and others provide MCP access to their dataloggers?_**

It may take years, primarily because there are no widespread MCP clients or AI agents to drive current demand, beyond enthusiastic researchers and labs.

What's next? What if MCPs are implemented _locally_? What if agents run directly on edge devices, such as SCADA systems or dataloggers? Could this mark the beginning of AIoT (Artificial Intelligence of Things), where systems autonomously control and make decisions, perhaps _operating hierarchically_ with central, more capable AI supervising constrained local agents?

Regardless, the future is bright. We should feel grateful to witness the birth of this new technological revolution.

---

**Are you aware of the MCP Protocol?** [**Follow me**](https://www.linkedin.com/comm/mynetwork/discovery-see-all?usecase=PEOPLE_FOLLOWS&followMember=ingenierodavidgomez) or **drop a comment below👇** for more strategies about APM, AI, renewables and sustainability.

**#AI #renewables #AssetManagement #solar #MCP**
