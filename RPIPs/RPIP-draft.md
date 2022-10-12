---
rpip: 
title: Balancing pDAO Control of Development
status: Draft
type: Meta
author: Valdorff (@Valdorff)
discussions-to: 
created: 2022-10-12
---
# Balancing pDAO Control of Development

## Simple Summary

Process surrounding how we can effectively balance the desire to have pDAO guide development at a
high level without micromanaging and damaging our ability to develop effectively.

## Abstract/Motivation

The pDAO should determine high level goals, but it should not micromanage.

The core idea is to categorize developer decisions based on their perceived impact and then follow
a category-specific process. As impact increases, more review is appropriate. Review should be kept
to the minimum appropriate such that we don't slow development down or make developing unpleasant.

## Specification

### For Developers
Developers SHOULD categorize implementation decisions into one of the following categories. \
Sub-bullets are examples, and should not be taken as limiting the category.
- Purely beneficial changes
  - Bug fixes
  - Identical results with lower gas, lower CPU usage, etc
- Technical tradeoffs
  - This uses more gas on initialization, but less gas on call
  - This uses lower CPU but more memory
- Value tradeoffs
  - This is more convenient for all users, but can be slighlty gamed by malicious users
- High level design changes
  - We initially wanted to allow users to build their own blocks, but that will not be possible
    unless we make big changes in the design

#### Purely beneficial changes:
- Developers SHOULD implement them; no community consultation is called for

#### Technical tradeoffs:
- Developers MAY implement them based on their judgment
- Developers MAY discuss options with the community in discord (eg, a thread)
- Developers MAY discuss options in a forum post categorized as "Development"

#### Value tradeoffs:
- Developers MUST discuss options in a forum post categorized as "Development"
- Developers MUST present a preliminary choice they plan to move forward
  - Developers SHOULD try to include this in the initial post if possible
- From the time that a preliminary choice is posted, developers MUST allow 5 days for someone to say
  they'll be championing a veto vote
  - If someoneone is championing a veto vote, they MUST be given 10 days from when the preliminary
    choice was posted to request a snapshot vote
- If (A) there's no champion for a veto vote within 5 days, (B) there's no snapshot request within
  10 days, or (C) the snapshot vote fails, the developer SHOULD implement their preliminary choice

#### High level design changes:
- Developers MUST discuss options in a forum post
  - If applicable, it SHOULD be categorized based on its topic (eg, "Node Operator Experience")
  - If no category applies, or if multiple categories apply, it MAY be categorized as "Development"
- If there is a clear consensus choice (as shown by a poll and forum comments), the developer SHOULD
  propose that solution as the preliminary choice
  - From the time that preliminary choice is posted, developers MUST allow 7 days for comments
    explicitly opposing the preliminary choice
  - If there are 5 or more comments (from pre-existing forum members) opposing the preliminary
    choices, then it's clear there is no consensus choice
  - If the concensus choice survives the 7-day review period, the developer SHOULD implement the
    preliminary choice
- If there is not a clear consensus choice, there should be one or more RPIPs and snapshot votes to
  determine what the pDAO believes is the best path forward

### For Community Members
- Community members MAY start "value tradeoff" and "high level design change" conversations if they
  feel it's appropriate
  - If possible, they SHOULD start a small conversation with the developer (eg, on discord) to give
    the developer an initial chance to control the forum post
  - Community members MAY post to the appropriate category (as in the Developer section above) with
    a discussion topic
    - Community members SHOULD include options where possible
    - Community members SHOULD include a preliminary decision if they have a clear preference
