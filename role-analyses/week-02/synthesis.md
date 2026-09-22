# Role Analysis — Module 2
## Sindi Banda | Week 2

**Role A:** Nation-State Threat Analyst  
**Role B:** Insider Threat Investigator

---

## Role A Perspective: Nation-State Threat Analyst

The Nation-State Threat Analyst reads the Module 2 material by asking what an external actor has actually demonstrated and how that behavior could matter to the plant systems in scope. In my FSB Center 16 profile, public reporting from CISA AA22-083A and the DOJ supports targeting of energy and nuclear organizations, but it does not prove access to a plant process computer, physical security system, or safety system. My Week 1 attack surface map shows PPC historian events and PSI security events flowing to OT-SIEM, but it does not show a return path from OT-SIEM into those systems. This role would flag any claim that treats that missing path as proven. Its authority is mainly advisory, and it is accountable for accurate attribution, confidence levels, and clear limits on what the evidence supports.

---

## Role B Perspective: Insider Threat Investigator

The Insider Threat Investigator looks for conditions that could allow a trusted or formerly trusted person to misuse access. The Maroochy Shire case is useful because the attacker had detailed SCADA knowledge and used stolen engineering equipment after he was no longer authorized. This role would watch contractor access, account termination, equipment recovery, unusual privilege changes, remote sessions, and unexplained configuration changes. Anderson helps explain why those indicators need context. **Cognitive dissonance** can cause someone to keep defending a risky decision after warning signs appear. **Authority and its abuse** shows why an employee may follow a questionable instruction from someone believed to have authority. The **risk thermostat** suggests that stronger controls can sometimes make people more comfortable taking risks elsewhere. The investigator therefore has to focus on observable actions, consider legitimate explanations and false positives, and avoid treating unusual behavior by itself as proof of malicious intent. (Anderson, *Security Engineering*, 3rd ed., Ch. 3, "Psychology and Usability")

---

## Divergence Analysis

The two roles can receive the same evidence and take different actions. A valid-account login, for example, could match a documented FSB technique. The Nation-State Threat Analyst would compare it with known TTPs, outside threat reporting, and other signs of external compromise. The Insider Threat Investigator would check who owns the account, whether the access fits that person's job, and whether the activity differs from the person's normal baseline. The analyst may prioritize blocking an external path and updating defenses, while the investigator may need to preserve evidence, review access history, and decide whether internal access should be restricted. Their disagreement is therefore about authority, priorities, and what action the evidence justifies.

---

## Synthesis

This divergence shows that nuclear cybersecurity depends on coordination between technical threat analysis and internal access investigation. A decision such as disabling a departing contractor's accounts, recovering equipment, and removing unnecessary privileges can satisfy both roles because it reduces both external credential abuse and insider misuse. A harder decision is whether to disable a suspicious account immediately or quietly monitor it to collect more evidence. Immediate action may reduce operational risk, while continued monitoring may help identify who is responsible. In that situation, one action cannot fully satisfy both priorities at the same time, so the organization has to balance protection, evidence collection, and operational impact.
