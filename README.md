# Required Headcount Calculator

A Python tool to calculate the **Required Headcount (HC)** for contact centers, supporting different channels like Voice, Chat, and Email. This tool uses two methods: **Erlang C** for synchronous channels (Voice and Chat) and the **Linear Method (Workload)** for asynchronous channels (Email).

## Overview

Calculating the required headcount (HC) for a contact center can be challenging, especially when dealing with different channels that have unique characteristics:
- **Voice:** Requires immediate responses, so we use Erlang C to account for random arrivals and queuing.
- **Chat:** Also synchronous but agents can handle multiple chats concurrently, so we adjust Erlang C for concurrency.
- **Email:** Asynchronous, so we use the Linear Method based on workload and efficiency.

This tool simplifies the process by allowing you to input a few parameters and get the required headcount along with the occupancy rate you choose to ensure agents aren't overworked.

## Features

- Supports three channels: Voice, Chat, and Email.
- Uses **Erlang C** for Voice and Chat, and the **Linear Method (Workload)** for Email.
- Calculates the **Occupancy Rate** to ensure agents aren't overworked.
- Allows repeated calculations in the same session (loop).
- Input validation to ensure correct values.

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/AbdelrahmanAteef/Required-HC-Calculator.git
   cd Required-HC-Calculator
