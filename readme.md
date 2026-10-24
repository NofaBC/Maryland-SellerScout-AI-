Maryland SellerScout AI™
Residential seller opportunity intelligence | NOFA AI Factory™

Maryland SellerScout AI™ is a browser-based proof of concept that helps real estate professionals research, prioritize, and track potential residential seller opportunities across Maryland. It demonstrates an explainable, rules-based opportunity score and a simple prospecting workflow, without requiring a backend or API keys.
Prototype only: All included properties and addresses are fictional. The application does not retrieve live property records, identify confirmed sellers, calculate validated probabilities of selling, or automatically contact homeowners. Despite the product name, the current scoring engine is rule-based, not an AI/ML predictive model.

Features
- Maryland-wide coverage: County filter for all 23 Maryland counties and Baltimore City.
- Property search and filtering: Search by address, city, or ID; filter by county, residential property type, opportunity priority, and lead status.
- Explainable opportunity scores: Prioritizes records using supplied ownership duration, estimated equity, absentee ownership, vacancy, and listing signals.
- Prospecting workspace: Inspect property details and scoring reasons; update lead status and research notes.
- Dashboard metrics: Matching records, high-priority opportunities, saved prospects, and follow-ups.
- CSV workflows: Download a CSV template, import authorized property records, and export leads.
- Browser persistence: Changes are saved locally using localStorage where supported.
- No installation required: A standalone index.html file built with HTML, CSS, and JavaScript.
Run locally
1. Download or clone this repository.
2. Open index.html in a modern web browser (Chrome or Edge recommended).
3. Explore the fictional example records or use CSV template and Import CSV to load data you are permitted to use.
There is no build step, package installation, backend service, or API key.
Importing data
Use the in-app CSV template to obtain the expected column layout. The importer expects at least:
id,address,city,county,propertyType,yearsOwned,estimatedValue,estimatedMortgage,absentee,listingSignal,vacant,status
MD-EXAMPLE-1,Sample Property,Rockville,Montgomery,Single Family,18,500000,150000,false,none,false,New
- Use true or false for absentee and vacant.
- Supported listing signals include expired, withdrawn, valuation_request, and none.
- The imported CSV replaces the current working dataset; export any changes before replacing or resetting records.
- Do not import personal contact information or sensitive client data into this prototype.
Opportunity scoring
Scores range from 0 to 100 and reflect research priority only, based on information in each record. Example indicators include:
- Years owned
- Estimated equity, derived from the provided estimated value and mortgage balance
- Absentee-owner indicator
- Vacancy indicator
- Listing history or a voluntarily submitted valuation request
Scores and explanations are heuristic—not trained or validated probabilities of a sale. Data accuracy, ownership, equity, property status, and any intention to sell must be independently verified.
Data and privacy
The demo does not scrape Maryland public-record websites or connect to MLS/property-data APIs. Future integrations must use appropriately licensed, permitted, and contractually authorized data sources. MLS data use may require broker and MLS approval.

Browser localStorage is not secure customer relationship management storage and is unsuitable for confidential or sensitive information. Imported data and notes stay in the current browser unless you explicitly export them; clearing browser storage may remove them.

Before any real-world outreach, the real estate professional is responsible for verifying applicable Do Not Call, TCPA, CAN-SPAM, Maryland marketing and privacy rules, fair housing requirements, and any permissions or consent needed for a specific communication channel. The prototype does not perform compliance clearance or automated outreach.
Suggested production roadmap
1. Validate the workflow with a Maryland realtor and confirm lead qualification criteria.
2. Integrate a licensed Maryland property-data provider and permitted MLS feeds, where available.
3. Add authenticated accounts, a secure database, data provenance, refresh timestamps, and duplicate handling.
4. Introduce permissioned CRM integrations, consent/DNC checks, and auditable outreach workflows.
5. Evaluate AI-assisted research summaries or predictive models only with suitable real datasets, validation, and ongoing monitoring.
Technology
- HTML5, CSS3, JavaScript
- Browser localStorage
- Standalone static website; no external dependencies required
Ownership
NOFA AI Factory™ / NOFA Business Consulting, LLC

This is a demonstration project. No open-source license is granted by this README; add a LICENSE file if public reuse is intended.
