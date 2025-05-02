SD-WAN LANDSCAPE (2024) – REORGANISED VIEW & FIT FOR A COMPANY WITH TWO U.S. DATA-CENTRES
================================================================================================

0. Why you should care  
For two data-centres a traditional “branch scale-out” view of SD-WAN is less relevant. What matters is:  
• High-speed, resilient DC-to-DC connectivity  
• Low-latency on-ramps into AWS/Azure/GCP regions in the U.S.  
• Strong, embedded security so you don’t have to hang a separate firewall stack off every edge box  
• A management plane that three engineers can actually run

1. Clean Market Map  
Instead of listing vendors alphabetically, it helps to group them by the **problem they solved first** (their “centre of gravity”) and by how they deliver the service.

A. Networking-heritage platforms (router DNA)  
   – Cisco (Catalyst/ASR + SD-WAN powered by Viptela), Cisco Meraki  
   – VMware SD-WAN by Velocloud  
   – HPE Aruba EdgeConnect (ex-Silver Peak)  
   – Juniper Session Smart (128T)  

   Core trait: deep routing features, rock-solid path selection, but usually need a **separate** NGFW for full security.

B. Security-heritage platforms (“Secure SD-WAN”)  
   – Fortinet Secure SD-WAN (FortiGate)  
   – Palo Alto Networks Prisma SD-WAN (ex-CloudGenix)  
   – Versa Secure SD-WAN / Versa SASE  
   – Check Point Quantum SD-WAN  

   Core trait: NGFW/IPS/SASE baked in; one appliance or one cloud license can cover both connectivity and security.

C. Cloud-native NaaS (Network-as-a-Service)  
   – Cato Networks, Aryaka, Alkira, Graphiant  
   – Customer deploys a lightweight edge or agent; the vendor’s private backbone + PoPs do the heavy lifting.  
   – Useful when you do **not** want to run any WAN infrastructure yourself.

D. Telco/ISP managed offers  
   – AT&T, Lumen, Verizon, Comcast, BT, Orange, NTT, etc.  
   – Typically re-badge one of the above technologies and add circuits + 24×7 ops.  
   – Good if you lack staff; less flexible for rapid policy changes.

2023–24 MQ snapshot (Gartner, Omdia, IDC synthesis):  
• Leaders: Cisco, Fortinet, Palo Alto, VMware, Versa, HPE Aruba  
• Challengers: Juniper, Cato, Check Point  
• Visionaries / Niche: Aryaka, Alkira, Graphiant, Telco-specific solutions

2. Shortlist for *your* scenario (2 U.S. DCs)
Below is an “80/20” filter: only vendors that can deliver ≥10 Gbps in a single appliance and have U.S. cloud gateways.

| Capability                                    | Cisco SD-WAN (Viptela) | Fortinet Secure SD-WAN | Palo Alto Prisma SD-WAN | VMware SD-WAN | Aruba EdgeConnect | Versa Secure SD-WAN |
|----------------------------------------------|------------------------|------------------------|-------------------------|---------------|-------------------|----------------------|
| Max DC-class throughput (1RU/2RU)            | up to 20 Gbps (C8500)  | 20 – 198 Gbps (FG-2xxxF/4xxxF) | ~20 Gbps (I-Series)   | 10 Gbps        | 40 Gbps (EC-XS)    | 20 Gbps (C-Series)  |
| Integrated NGFW / IPS                        | Optional (extra box/lic) | Native (same ASIC)     | Native (requires Prisma Access for cloud security) | None (needs 3rd-party) | Optional (via Aruba SSE) | Native |
| U.S. cloud/SaaS gateways / PoPs              | 38                     | 30+                    | 27+                     | 31+           | 20+               | 25+                 |
| Multi-cloud templates (AWS, Azure, GCP)      | Yes                    | Yes                    | Yes                     | Yes           | Yes               | Yes                 |
| Pricing model                                | DNA-Adv / term sub.    | HW + “Enterprise” bundle | Subscription-only      | $ per Mbps    | HW + sub.         | HW or sub.          |
| Operational complexity (1 = easiest)         | 3 (vManage)            | 2 (FortiManager)       | 3 (Prisma UI + Access)  | 3 (Orchestrator) | 2–3 (EZ UI)      | 4 (Versa Director) |
| Typical 3-yr TCO for 2 DCs @ 10 Gbps         | Highest                | Lowest                 | Medium-high            | Medium        | Medium            | Medium-low          |
| “Killer” strength                            | Rich routing & APIs    | All-in-one security + perf | App-aware ML path-choice | SaaS/VDI optim. | WAN optimisation   | Full SASE stack     |
| Key gap                                      | Extra firewall boxes   | Routing depth vs Cisco | Higher OPEX             | Needs NGFW     | SASE still maturing| Steeper learning curve |

3. Analyst-level takeaways
• The market is **converging with SASE**; security-heritage vendors now outsell router heritage in green-field projects ≤ 100 sites.  
• Cisco still owns ~35 % of installed WAN infrastructure, so it wins when customers want “no forklift”.  
• Fortinet is grabbing share fastest (≈ 30 % YoY growth) because the one-appliance model slashes capex in data-centre use-cases.  
• VM-ware Velocloud is losing mind-share post-Broadcom acquisition, but remains popular through carrier bundles.  
• Cloud NaaS players (Cato, Aryaka) are doubling revenue, yet they cap out at ≈ 5 Gbps edge throughput—fine for branches, not DC cores.

4. What should *you* do?

Step-1 | Thin the herd  
Ignore telco resell and NaaS for now—your engineers want control and you need ≥10 Gbps. That leaves: Cisco, Fortinet, Palo Alto, Aruba, Versa, VMware.

Step-2 | Run a proof-of-concept bake-off (30 days)  
Metrics:  
a) Encrypted DC-to-DC throughput under 64-byte packet flood  
b) Auto-failover time on dual circuits (MPLS + DIA or dual DIA)  
c) Cloud-path latency into AWS us-east-1, us-west-2, Azure Central US  
d) How many consoles / licenses required for full NGFW + SD-WAN policy  
e) Time to create a policy via GUI & via API/Ansible

Step-3 | Crunch the 3-year TCO  
Include: hardware, licenses, support, smart-hands install, staff training, and if needed external firewalls.

5. Likely outcome (based on similar customers)

• Fortinet Secure SD-WAN on FG-2000F/2600F appliances in each DC is usually 30–45 % cheaper than a Cisco C8500 + Firepower pair, while meeting the same performance and delivering inline NGFW.  
• If you are already 80-100 % Cisco and rely on advanced routing tricks (EVPN, SR-MPLS), Cisco SD-WAN is the smoothest fit—just budget for separate NGFW blades or boxes.  
• Palo Alto Prisma SD-WAN becomes attractive if you are a heavy Palo Alto firewall shop and want a single SaaS portal for branch + remote user + cloud security, accepting the premium subscription cost.

6. Quick decision matrix

If you prioritise …    →   Choose  
Lowest hardware count   →   Fortinet  
Deepest routing stack   →   Cisco  
Most advanced SASE      →   Palo Alto or Versa  
Best WAN optimisation    →   Aruba EdgeConnect  
Carrier-managed turnkey →   VMware (via ISP) or Telco variant

7. Next actions

1. Book demo gear (Fortinet 2000F, Cisco C8500-12X4QC, Palo Alto ION 3000)  
2. Lab test items in Step-2, capture metrics  
3. Request formal quotes (3-yr term) and compare NPV  
4. Present findings to leadership, pick vendor, schedule rollout

Need comparative pricing sheets, PoC test scripts, or integration checklists? Let me know and I’ll draft them.
