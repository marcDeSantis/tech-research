Below is a two-part answer.

Part 1 – Competitive landscape at a glance (tabular).  
Part 2 – How those differences map to the needs of a technology-hardware/solutions reseller and concrete recommendations.

──────────────────────────────────────────

PART 1.  Snapshot of 11 leading eCommerce options
──────────────────────────────────────────

Key:  
• B2B = native functions such as company accounts, PO/credit limits, contract pricing.  
• Config = readiness for complex or configurable/BTO (build-to-order) products without heavy custom code.  
• TCO = relative 3-yr total cost of ownership for a mid-sized catalog (~20 k SKUs).  
• API-first = “headless / composable-friendly” score.  
Scoring: 1 (Low/Poor) – 5 (High/Excellent)

| # | Platform (vendor) | Deployment model | Native B2B depth | Config product depth | Ecosystem / Apps | API-first | Typical 3-yr TCO | Strength headline | Key watch-outs |
|---|-------------------|------------------|------------------|----------------------|------------------|-----------|------------------|-------------------|----------------|
| 1 | Salesforce Commerce Cloud + Salesforce CPQ | SaaS (multi-tenant) | 5 | 5 (with CPQ) | 4 | 4 | $$$$ | Seamless Sales/Service/CPQ + strong enterprise B2B | High licensing & SI costs; heavy SFDC dependence |
| 2 | Adobe Commerce (Magento 2) | PaaS (Adobe cloud) or self-host | 4 | 4 (configurable, bundle, 3rd-party CPQ) | 5 | 4 | $$$ | Rich catalog, large extension market, visual configurators available | Ongoing patching/upgrades; need DevOps skills |
| 3 | BigCommerce Enterprise | SaaS | 3 (BundleB2B, B2B Edition) | 3 (bundles, options; Threekit app) | 4 | 4 | $$ | Fast to launch, lower TCO, open APIs | Deep customization sometimes needs micro-services |
| 4 | OroCommerce | Open-source (PHP) | 5 | 3 | 3 | 3 | $$ | Purpose-built B2B, strong corporate account & quoting | Smaller ISV/agency ecosystem |
| 5 | SAP Commerce Cloud (Hybris) + SAP CPQ | PaaS/SAP | 5 | 5 | 4 | 3 | $$$$ | Enterprise grade, tight SAP ERP & CPQ tie-in | Long implementation cycles; license/hosting fees |
| 6 | commercetools | SaaS (API–first) | 4 | 4 (via MACH architecture) | 3 | 5 | $$$ | Composable flexibility, elastic scaling | Requires front-end & CPQ build; costs shift to dev team |
| 7 | Elastic Path Commerce Cloud | SaaS (headless) | 3 | 4 (Cortex API, Product Builder) | 3 | 5 | $$$ | Subscription-style products, bundles, price books | Smaller community than BigCommerce/Adobe |
| 8 | VTEX | SaaS (multi-tenant) | 4 | 3 | 3 | 4 | $$ | Unified marketplace, OMS built-in | Fewer North-Am system integrators |
| 9 | Shopify Plus | SaaS | 2 (B2B launched 2022) | 2–3 (customizer, 3rd-party apps) | 5 | 3 | $$ | Very fast to market, huge app ecosystem | Still maturing B2B feature set; variant limits |
|10 | WooCommerce + Composite Products | Self-host (WordPress) | 2 | 3 | 4 | 2 | $ | Low entry cost, vast plugin library | Scaling, security, multi-store pain at enterprise level |
|11 | Open-source headless stack (e.g., Spree + Vendure + custom CPQ) | Self-host / cloud | 3 | 4–5 (code-driven) | 3 | 5 | $$–$$$ | Maximum control & license freedom | Higher engineering load, no “out-of-box” B2B |

──────────────────────────────────────────
PART 2.  Mapping the choices to your business goals
──────────────────────────────────────────

Your stated needs  
1. Serve BOTH enterprise accounts and smaller business buyers.  
2. Offer two catalog experiences:  
   a) standard “add-to-cart” SKUs (e.g., accessories, peripherals)  
   b) complex, configurable SKUs (e.g., custom servers, multi-year software + service bundles).  
3. Future-proof scaling and integrations (ERP, CRM, entitlement/renewals, channel portals).  
4. Reasonable speed to market & manageable cost structure.

Decision drivers, ranked for tech-sector resellers  

A. B2B depth – corporate account hierarchies, contract or volume pricing, quote-to-cash, PO/credit checkout, quick-order.  
B. Configurability – native configurator or tight CPQ integration; ability to prevent invalid component mixes.  
C. API & composability – your catalogs/configured products may feed partner portals, inside-sales tools, etc.  
D. Ecosystem / talent pool – ease of finding integrators & extensions.  
E. TCO – budgets vary between enterprise and SMB, so subscription + support + dev + hosting must sit in “sane” range.

Option short-list & rationale

1. Salesforce Commerce Cloud + Salesforce CPQ  
   • Best when you are already an SFDC shop (Sales, Service, Pardot).  
   • Unified product master, shared pricebooks, approvals, renewals.  
   • Hits A, B, C, D very well. Biggest blocker is cost (license + SI) and 9-12 mo project duration.

2. Adobe Commerce (Magento 2) with B2B module + a CPQ app (Threekit, Configit, KBMax, etc.)  
   • Popular among tech hardware resellers thanks to flexible catalog (configurable, bundle, grouped) and solid B2B add-ons (company accounts, requisition lists, quick order).  
   • You can keep a single codebase and expose different storefront themes for SMB vs. enterprise.  
   • Mid-range cost; on-prem or Adobe-hosted. Dev/ops investment is non-trivial.

3. BigCommerce Enterprise + BundleB2B + Threekit or ConfigureID  
   • Lower TCO SaaS. API layer is wide open (GraphQL + REST) so you can bolt on a CPQ or build micro-service for configurations.  
   • Built-in multi-storefront lets you separate SMB storefront from an enterprise one sharing inventory.  
   • Limitation: deep CPQ logic (e.g., 1000s of compatibility rules) still lives outside in a service.

4. commercetools (headless) + best-of-breed CPQ (e.g., Tacton, Logik.io) + FE framework (Next.js, Vue Storefront)  
   • “Composable commerce” lets you swap pieces as your enterprise side grows.  
   • Strong fit when you have engineering muscle or a systems integrator and want to deliver multiple channels (web, inside-sales app, kiosk) off the same APIs.  
   • Initial build cost higher; SMB storefront will need a front-end or partner like Frontastic.

5. OroCommerce – for a B2B-only focus or if you need granular corporate account/permissions and are comfortable with PHP development.  
   • Native RFQ, quotes, price lists; basic configurable products adaptable for services.  
   • Smaller but growing ecosystem; good value if you self-host and control code.

Recommended selection pattern

Step 1 – Split requirements into “core commerce” and “complex configuration.”  
• Core commerce must handle pricing, tax, discounts, inventory, multi-store, corporate accounts.  
• Configuration engine can be native (if strong enough) or an external CPQ exposed as a service.

Step 2 – Choose a platform that:  
a) has adequate out-of-box B2B for corporate buyers, AND  
b) exposes an API (or plugin) where a CPQ/visual configurator can call back prices & rules.

“Best-fit tiers” summary:

Enterprise-heavy, high budget, strongest fit  
→ Salesforce Commerce Cloud + Salesforce CPQ (if SFDC stack)  
→ SAP Commerce Cloud + SAP CPQ (if deep SAP footprint)

Balanced enterprise + SMB, moderate budget  
→ Adobe Commerce (Magento 2) with B2B module + KBMax or Threekit  
→ BigCommerce Enterprise + BundleB2B + external CPQ

Developer-led, composable future-proofing  
→ commercetools or Elastic Path + best-of-breed CPQ + custom FE

Cost-sensitive, open-source control  
→ OroCommerce or Magento Open Source + open-source configurator, self-hosted

Quick “if-this-then-that” guide

• Already run Salesforce CRM and executives push for one cloud?  
  – Pick Salesforce Commerce Cloud + Salesforce CPQ.

• Have Magento skills, need strong catalog, want to own code, but not pay SAP-level fees?  
  – Adobe Commerce.

• Want SaaS simplicity, fastest launch, lower capex but still decent B2B?  
  – BigCommerce Enterprise (+ apps).

• Firm vision for composable architecture and in-house dev team comfortable with micro-services?  
  – commercetools.

Implementation next steps

1. List must-have B2B features (contract pricing, PO checkout, approval workflows, punchout, etc.) and score each shortlisted platform in a workshop.  
2. Document configuration/CPQ rules (compatibility matrix, price logic, approvals) to gauge whether native product types are sufficient or a dedicated CPQ is mandatory.  
3. Run two vendor demos – one focused on standard catalog flow, one entirely on a complex build-to-order scenario.  
4. Obtain 3-yr TCO quotes from at least two implementation partners per platform; include licenses, implementation, support.  
5. Pilot with a constrained catalog (e.g., accessories + one configurable server line) and measure performance/load before scaling.

Bottom line

• There is no single “best” platform, but the combination of Adobe Commerce or BigCommerce for the core store plus a purpose-built CPQ/visual configurator delivers the most balanced mix of B2B functionality, configurability and cost for technology resellers that must serve both SMB and enterprise buyers.  
• If you are already committed to Salesforce or SAP ecosystems, their commerce + CPQ suites leap ahead on integration and enterprise governance—budget permitting.  
• A headless/composable route (commercetools) is the forward-looking choice if you see omnichannel, marketplace and internal tooling flexibility as strategic.

Feel free to share more detail on existing tech stack, budget range or timeline and I can narrow the recommendation further.
