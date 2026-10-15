# KB-0001: Outlook search returns no or incomplete results (example)

> Sample article that shows the template in use. Adapt to your environment.

| Field | Value |
| --- | --- |
| Applies to | Microsoft Outlook for Windows (Microsoft 365 Apps), Windows 10/11 |
| Audience | End users and service desk |
| Review due | 2027-04-01 |

## Symptom
Searching in Outlook shows "No results" or misses recent messages, while the messages are visible in Outlook on the web.

## Cause
The local Windows Search index for Outlook is incomplete or corrupted, or Outlook is limited to a short cached-mail window.

## Resolution
1. Confirm the messages appear in Outlook on the web. If they do not, stop and escalate: it is not an index problem.
2. In Outlook choose **File > Options > Search > Indexing Options**.
3. Choose **Advanced > Rebuild**. Indexing can take from minutes to hours on large mailboxes.
4. Confirm the **Windows Search** service is running (`services.msc`).
5. In **File > Account Settings > Account Settings > Change**, check the **Mail to keep offline** slider, and increase it if needed.
6. Restart Outlook and test again after indexing finishes.

## How to verify
A search for a known recent message returns it. **File > Options > Search > Indexing Status** shows 0 items remaining.

## If this does not work
Create a new Outlook profile and test. Escalate to Tier 2 with the Outlook build number, the profile test result and the indexing status.
