# Role Analysis, Module 1
## Sindi Banda | Week 1-2

**Role A:** NRC Security Inspector
**Role B:** Plant Cybersecurity Manager

---

## Role A Perspective: NRC Security Inspector

An NRC Security Inspector would focus on whether the licensee can show that OT-SIEM and its connections are properly identified, protected, and documented. RG 5.71 describes an approach the NRC staff finds acceptable for meeting 10 CFR 73.54, including protection of digital systems tied to safety, security, and emergency preparedness functions. The document the inspector actually measures against is the site's approved cybersecurity plan rather than RG 5.71 itself, because RG 5.71 states that regulatory guides are not NRC regulations and compliance with them is not required.

The inspector's authority comes from 10 CFR 73.54(f). RG 5.71 Section C.3.5 confirms how this works in practice: the licensee does not have to submit its site-specific policies, implementing procedures, or supporting analyses to the NRC for prior review and approval, but that information must be available for NRC inspection. The inspector can therefore ask to see any analysis behind any claim, at any time, without having approved it in advance. The accountability that follows is that the inspector has to write findings that survive enforcement review, which is why an undocumented control is treated as an unmet one.

Looking at my attack surface map, the inspector would question any connection I listed without evidence and would want to see how the plant protects access, monitoring, and the integrity of security data. The rows I marked with an asterisk, the ones describing interfaces the plant architecture does not show, are exactly what an inspector would ask me to justify or remove. Anderson's security engineering framework also supports this system view because security depends on the whole system, including the technology, procedures, and the people maintaining it, not just one control.

---

## Role B Perspective: Plant Cybersecurity Manager

A Plant Cybersecurity Manager would focus more on whether OT-SIEM can actually work every day in the plant environment. NEI 08-09 Revision 6, "Cyber Security Plan for Nuclear Power Reactors," is the industry template licensees used to build the plan submittals required by 10 CFR 73.54, and RG 5.71 Revision 1 confirms the NRC has found it and its addenda acceptable for use. For my OT-SIEM map, the manager would care about whether feeds from systems such as RMS, PSI, and PPC are reliable, whether failed or false data can be detected, and whether analysts can manage the alerts effectively. Anderson makes the related point that a security control can fail if the people using it cannot work with it effectively.

The constraint this role carries and the inspector does not is change control. RG 5.71 Section C.2 states that revisions to the cybersecurity plan are processed in accordance with 10 CFR 50.54(p). If a fix would decrease the effectiveness of the plan, the manager cannot simply implement it and document the result, which means every correction has a schedule cost the inspector never pays. RG 5.71 Section C.3.3 adds a second constraint in the same direction: a security control should not be applied if it adversely impacts SSEP functions or performance, and when it does, the manager has to find an alternate control that provides at least equivalent protection and document why. The inspector can identify a gap. The manager has to close it without breaking the plant.

---

## Divergence Analysis

Both roles care about protecting OT-SIEM, but they would act differently when they find a problem. The NRC inspector would ask for evidence that the control meets the approved cybersecurity plan and would flag unsupported claims or missing documentation. The plant cybersecurity manager would focus on fixing the problem in a way that keeps monitoring reliable and does not create unnecessary problems for plant operations. This difference reflects the gap between regulatory oversight and practical implementation.

The incentives point in opposite directions on the same facts, and this is sharper than the difference in priorities. The inspector carries no cost for flagging something that turns out to be minor, and a real cost for missing something that turns out not to be. The manager carries the cost of every documentation hour, every outage window, and every 50.54(p) submittal. Applied to a suspected OT-SIEM compromise, that pushes the two roles toward different reporting paths for identical facts. Under 10 CFR 73.77, an event that adversely impacted a security function requires a one-hour notification to the NRC Headquarters Operations Center, while a vulnerability, weakness, or deficiency in the cybersecurity program is recorded in the site corrective action program within 24 hours and involves no call at all. The manager has an incentive to characterize an ambiguous finding as the second. The inspector has an incentive to test whether it was the first. Neither is acting improperly. The rule leaves "adverse impact" and "discovery" undefined enough that both readings are available.

---

## Synthesis

The two perspectives show that nuclear cybersecurity requires both compliance and practical operation. A control can look correct on paper but still fail if it is hard to maintain, produces poor alerts, or depends on data that cannot be trusted. A good decision would give the NRC inspector clear evidence that the control is implemented while also giving the plant manager something that can be operated and maintained reliably. This matches Anderson's broader point that security has to work as a complete system, not just as a list of technical controls.

The regulation has a structural answer to this divergence, not just a procedural one. RG 5.71 Section C.3.4 recommends forming a unified security organization that incorporates both cybersecurity and physical security and that is independent from operations. Independence from operations is what stops the manager's schedule and availability pressures from deciding security questions, and unification is what stops cyber and physical from answering the same question two different ways. The divergence between my two roles is therefore designed into the organization rather than accidental, and the organizational chart is where it is meant to be resolved.

Some decisions cannot satisfy both roles at once, and alert tuning on OT-SIEM is the clearest example. The inspector wants demonstrable detection coverage, which pushes toward more correlation rules and lower thresholds. The manager needs an alert volume that analysts can actually work through, which pushes the other way. Above a certain coverage level there is no configuration that satisfies both, because the binding constraint is analyst attention, and analyst attention is fixed in a way that rule counts are not. This is not a communication failure and better documentation does not resolve it. One role has to accept less than it wants, and the regulation does not say which.

---

**Open item.** The Anderson usability point in the Role B section needs an edition check before submission. In *Security Engineering* 3rd edition, psychology and usability is Chapter 3, outside a Chapters 1 and 2 assignment. In the 2nd edition it is Chapter 2 and the reference is inside the assigned range. Confirm which edition the syllabus assigns, and if it is the 3rd edition, either drop the sentence or make the point without attributing it to Module 1 reading. If the 3rd edition is assigned, Chapter 2 on threat actors is directly relevant to both roles and is currently unused.
