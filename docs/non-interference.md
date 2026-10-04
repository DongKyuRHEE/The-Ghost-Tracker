# Non-Interference Principle

> **The user commands. The AI acts. Ghost Tracker watches.**

Ghost Tracker is a monitoring system, not an instruction protocol.

## Ghost Tracker may
- observe agent behavior;
- record execution and evidence;
- compute X/Y/Z state;
- track trajectory and baseline deviation;
- assess integrity;
- report confidence;
- report observed behavioral change;
- flag attention conditions.

## Ghost Tracker must not autonomously
- rewrite the user's task;
- invent additional task objectives;
- instruct the observed agent to retry;
- select a new execution strategy;
- force a tool choice;
- stop execution;
- change the user's completion criteria.

## External controller boundary

A separate controller may consume Ghost Tracker reports and act on them, but that controller is not Ghost Tracker Core.

This distinction is intentional and central to the framework.
