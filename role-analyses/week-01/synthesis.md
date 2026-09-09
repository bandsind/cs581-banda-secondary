# Role Analysis — Module 1

**Student:** Sindi Banda  
**Weeks:** 1–2  
**System:** OT Security Information & Event Management (OT-SIEM)  
**Role A:** NRC Security Inspector  
**Role B:** Plant Cybersecurity Manager  

---

## Role A Perspective: NRC Security Inspector

An NRC Security Inspector would focus on whether the licensee can show that OT-SIEM and its connections are properly identified, protected, and documented. Under 10 CFR 73.54 and the site's approved cyber security plan, the inspector would want evidence showing that important digital systems and their connections are protected from cyberattack. Looking at my attack surface map, the inspector would question any connection that is based only on assumption and would want to see how access, monitoring, and the integrity of security data are protected. Anderson's system view also applies because the security of OT-SIEM depends on the technology, procedures, and people around it, not only one security control.

---

## Role B Perspective: Plant Cybersecurity Manager

A Plant Cybersecurity Manager would focus more on whether OT-SIEM can actually work and be maintained in the plant environment. The manager would care about whether the data feeds from RMS, PSI, and PPC are reliable, whether missing or false information can be detected, and whether analysts can manage the alerts effectively. NEI 08-09 provides an industry implementation view of the cyber security program, which connects more closely to the manager's responsibility of putting security requirements into practice. Anderson's discussion of psychology and usability also matters because even a strong security control can fail if the people using it cannot understand or manage it effectively.

---

## Divergence Analysis

Both roles want OT-SIEM to be protected, but they would act differently when they find the same problem. The NRC Security Inspector would ask for evidence that the control meets the approved cyber security plan and would flag missing documentation, unsupported connections, or controls that cannot be verified. The Plant Cybersecurity Manager would focus on fixing the problem while keeping monitoring reliable and avoiding unnecessary effects on plant operations. The main difference is that the inspector is responsible for regulatory oversight, while the manager is responsible for implementing and maintaining the controls in the actual operating environment.

---

## Synthesis

The two perspectives show that nuclear cybersecurity requires both regulatory oversight and practical implementation. A security control can meet a documented requirement but still create problems if it produces too many alerts, depends on unreliable data, or is difficult to maintain. A decision that satisfies both roles would provide clear evidence that the control is implemented while also making sure it can be operated and maintained reliably. A difficult conflict can happen when stronger monitoring improves detection coverage but creates more alerts than analysts can realistically review, forcing the plant to balance security coverage with operational usability.

---

## Unresolved Operational Question

How much should OT-SIEM monitoring be tuned to reduce false alerts before reducing the alert volume begins to weaken the plant's ability to detect a real cyberattack?

---