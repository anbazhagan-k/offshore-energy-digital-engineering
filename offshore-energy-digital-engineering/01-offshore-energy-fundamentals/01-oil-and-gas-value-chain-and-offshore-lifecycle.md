# Lesson 01 — Oil & Gas Value Chain and Offshore Asset Lifecycle

**Module:** 01 — Offshore Energy Fundamentals  
**Audience:** Aspiring Digital Engineering / Engineering Information Management / Asset Information Management professionals  
**Study depth:** Functional and information-management depth — understand what each activity does, the facilities and equipment involved, how work moves between phases, and what information must be controlled. This is not a petroleum engineering design course.  
**Status:** STUDY MATERIAL CREATED — learner study and assessment pending

---

## 1. Learning outcomes

After studying this chapter, you should be able to:

1. Explain upstream, midstream and downstream activities and how they connect.
2. Describe the main stages of an offshore oil and gas development, from exploration to decommissioning.
3. Distinguish a producing field, well, fixed platform, floating production facility, subsea development, pipeline and LNG terminal.
4. Trace a simplified hydrocarbon path from a reservoir to a customer.
5. Recognise the main project participants: operator, engineering contractor, EPC/EPCI contractor, drilling contractor, OEM/vendor and operations team.
6. Identify the engineering information created, reviewed, handed over and maintained at each lifecycle stage.
7. Explain where Digital Engineering and Engineering / Asset Information Management contribute — without confusing these roles with process, subsea, structural or petroleum design engineering.

## 2. The oil and gas value chain

The oil and gas value chain is commonly divided into three broad segments:

- **Upstream:** find and produce oil and natural gas.
- **Midstream:** gather, process, transport and store production so it can reach processing plants, refineries, export terminals or markets.
- **Downstream:** refine crude oil, process and distribute gas and petroleum products, and deliver products to end users.

The boundaries are not universal. For example, gas processing and gathering may be classified as upstream or midstream depending on the company, contract, jurisdiction or industry definition. Learn the activity being performed, not only the label.

### 2.1 Upstream — exploration and production (E&P)

**Purpose:** Identify hydrocarbon resources, establish whether they can be developed economically and safely, build the required facilities, and produce oil or gas.

Typical activities:

1. **Licensing and acreage:** a government or regulator grants rights to explore or develop a defined area.
2. **Geological and geophysical studies:** teams interpret rock formations and seismic data to identify possible reservoirs.
3. **Exploration drilling:** a well is drilled to test whether hydrocarbons are present.
4. **Appraisal:** additional data and wells help estimate the extent, quality and deliverability of a discovery.
5. **Field development planning:** the operator selects a development concept, well count, production capacity, facilities and export route.
6. **Development drilling and construction:** production wells and facilities are installed.
7. **Production operations:** wells produce fluids; facilities separate, treat, compress, pump, meter and export them.
8. **Well intervention and late-life management:** wells and facilities are maintained, repaired, optimised or shut in as required.

**Common upstream assets and systems:**

- Reservoirs and production wells
- Wellheads and Christmas trees
- Subsea trees, manifolds and control systems
- Fixed offshore platforms and floating production units
- Drilling rigs and well intervention equipment
- Production separators, pumps and compressors
- Gas dehydration and treatment packages
- Flare and vent systems
- Produced-water treatment and disposal systems
- Export pumps, metering and pipeline interfaces

**Digital Engineering / information-management relevance:**

- Well, field, facility and equipment identifiers must be consistent.
- Seismic, well, geological, engineering and operations data have different owners, formats and access rules.
- Facility design information must be connected to installed equipment and operating records.
- Changes to wells, process systems, equipment and operating limits must be traceable.
- The asset team needs reliable information for maintenance, integrity, modifications and decommissioning.

### 2.2 Midstream — connection, processing, transport and storage

**Purpose:** Move and condition production between the producing asset and the next processing, export or consumption point.

Typical activities and infrastructure:

- Gathering pipelines collect production from multiple wells or facilities.
- Onshore or offshore pipelines transport oil or gas.
- Compression stations raise gas pressure to support transport.
- Pump stations move liquids through pipelines.
- Gas processing plants separate gas liquids and remove unwanted components.
- Storage terminals hold crude oil, refined products or gas.
- Export terminals transfer products to ships or other transport systems.
- LNG liquefaction plants cool natural gas to approximately -162°C so it becomes a liquid for storage and transport.
- LNG carriers transport LNG; receiving terminals store and regasify it for pipeline delivery.

**Digital Engineering / information-management relevance:**

- Pipeline route, segment, crossing, valve, station and inspection information must be controlled.
- Line lists, pipeline registers, material data, corrosion information and inspection history support integrity management.
- Compressor, pump, metering and terminal equipment data must link to maintenance and operational systems.
- Interfaces between offshore facilities, pipelines, terminals and third parties need clear battery limits and data responsibilities.
- LNG facilities require reliable equipment, process, instrumentation, safety, cryogenic-service and operating information.

### 2.3 Downstream — refining, products and distribution

**Purpose:** Convert crude oil and gas into products and deliver them to industrial, commercial and domestic customers.

Typical activities:

- Crude oil refining: separation and conversion processes produce fuels and other products.
- Petrochemical production: feedstocks are converted into chemicals and materials.
- Gas processing and distribution: gas is treated to meet applicable specifications and delivered through transmission and distribution networks.
- Product storage, terminals, shipping, marketing and retail distribution.

Examples of products include petrol/gasoline, diesel, aviation fuel, LPG, lubricants, bitumen, petrochemical feedstocks and natural gas.

**Digital Engineering / information-management relevance:**

- Refineries and petrochemical plants contain large interconnected process, utility, electrical, instrumentation and rotating-equipment systems.
- Equipment registers, piping and instrumentation diagrams (P&IDs), line lists, electrical records, control-system data and maintenance history must remain aligned.
- Product quality, process safety, inspection, reliability and regulatory records depend on accurate information.

### 2.4 Compare the three segments

| Segment | Main question | Typical facilities | Typical output / handoff |
|---|---|---|---|
| Upstream | Where are hydrocarbons, and how do we produce them? | Wells, platforms, subsea systems, FPSOs | Produced oil, gas and associated fluids |
| Midstream | How do we gather, condition, move and store production? | Pipelines, compressor stations, processing plants, terminals, LNG facilities | Transported or conditioned hydrocarbons |
| Downstream | How do we convert and deliver products to users? | Refineries, petrochemical plants, distribution networks | Fuels, chemicals and delivered gas |

**Important:** An organisation may operate in more than one segment. Integrated energy companies can own upstream fields, pipelines, LNG facilities, refineries and distribution businesses.

## 3. Offshore development — what makes it different?

An offshore development produces hydrocarbons from beneath the seabed. Compared with an onshore field, offshore projects must account for marine conditions, water depth, waves, wind, currents, corrosion, logistics, evacuation, limited access and specialist vessels.

The development concept depends on factors such as:

- Water depth and metocean conditions
- Reservoir location, size, pressure and expected production
- Distance to existing infrastructure and export markets
- Number and location of wells
- Oil, gas and water composition
- Required processing and storage capacity
- Safety, environmental and regulatory requirements
- Capital cost, operating cost and project economics

### 3.1 Common offshore development concepts

**Fixed platform:** A structure supported by legs or a jacket founded on the seabed. It may carry drilling, production, utilities, accommodation and control facilities.

**Jack-up rig:** A mobile offshore drilling unit with legs that are lowered to the seabed and a hull raised above the water. It is generally used in suitable shallow-water conditions. A jack-up is normally a drilling unit, not the same thing as a permanent production platform.

**Semi-submersible:** A floating offshore unit supported by submerged pontoons and columns. Semi-submersibles can be used as drilling units or, in suitable designs, floating production facilities.

**Drillship:** A ship-shaped mobile drilling unit that uses a drilling system and station-keeping, commonly dynamic positioning, to maintain its position.

**FPSO — Floating Production, Storage and Offloading:** A floating facility that receives production from subsea wells or other sources, processes it, stores oil and offloads it to shuttle tankers. Some FPSOs also export gas by pipeline; configurations vary.

**Subsea development:** Production equipment is installed on the seabed. Subsea wells and trees connect through flowlines, manifolds and risers to a host platform, FPSO or shore facility. Control and power may be supplied through umbilicals.

**Tie-back:** A subsea field or satellite development is connected to an existing host facility rather than receiving a completely new standalone production facility.

### 3.2 Functional equipment awareness

For a Digital Engineering / Information Management role, learn what equipment does and how it connects. You are not expected to design it, calculate its process duty or approve its mechanical integrity.

| Equipment / system | Functional purpose | Information you should recognise |
|---|---|---|
| Wellhead / subsea tree | Controls access to and flow from a well | Well / tree identifier, configuration, pressure rating, status |
| Manifold | Combines or distributes flow from multiple wells or lines | Manifold tag, connected wells, valves, piping interfaces |
| Flowline | Carries produced fluids between subsea equipment and host | Line number, route, size, material, design conditions |
| Riser | Connects seabed pipeline / system to a floating or fixed facility | Riser ID, type, interface, inspection and integrity records |
| Umbilical | Carries control, chemical, hydraulic or electrical services | Umbilical ID, service, termination points, configuration |
| Separator | Separates gas, oil and water | Equipment tag, process service, design data, connected lines |
| Compressor | Raises gas pressure | Equipment tag, driver, duty, datasheet, maintenance history |
| Pump | Moves liquids or raises liquid pressure | Equipment tag, duty, driver, datasheet, maintenance history |
| Heat exchanger | Transfers heat between process streams | Equipment tag, service, datasheet, inspection records |
| Flare system | Safely disposes of gas during defined operating or upset conditions | Flare header, relief devices, flare tip, cause-and-effect interfaces |
| Produced-water system | Treats water separated from production | Package tags, treatment equipment, discharge / reinjection interfaces |
| Instrumentation and control | Measures and controls process conditions | Instrument tag, range, loop, I/O, control-system references |

## 4. Follow the hydrocarbons — a simplified offshore-to-market example

Consider a fictional offshore gas-condensate field.

1. Gas and liquids are produced from reservoir formations through production wells.
2. Wellheads or subsea trees control the flow from each well.
3. Flowlines carry production to a subsea manifold or host facility.
4. Risers bring production to the host facility, if the development uses a floating or platform host.
5. The production facility separates gas, condensate and produced water.
6. Gas is treated and compressed to meet export requirements.
7. Gas travels through an export pipeline to an onshore gas plant or LNG facility.
8. At an LNG plant, gas is further treated and liquefied for storage and shipping; alternatively, treated gas may enter a pipeline network.
9. Condensate may be stabilised, stored and exported separately.
10. Products reach industrial users, utilities or other customers.

This is an illustrative route, not a universal design. Actual facilities may have different process steps, equipment, export routes and ownership boundaries.

**Exercise — draw the process path:** Create a simple block diagram showing:

`Reservoir → Well → Subsea / Wellhead System → Flowline / Riser → Production Facility → Export Pipeline → Gas Plant / LNG Terminal → Market`

Add a separate branch for produced water and condensate. Label where the operator, pipeline operator and LNG plant operator may have different responsibilities.

## 5. Project lifecycle — from opportunity to end of asset life

Do not confuse the **industry value chain** (upstream / midstream / downstream) with the **project and asset lifecycle**. The first describes what part of the industry an activity belongs to. The second describes how a specific asset is conceived, designed, built, operated and eventually retired.

A simplified offshore project lifecycle is:

### Phase 1 — Opportunity, licensing and exploration

**What happens:** An area is evaluated, exploration rights are obtained, geological and geophysical studies are performed, seismic surveys are interpreted and exploration wells may be drilled.

**Information examples:** Licence / block data, seismic survey metadata, well records, geological interpretations, exploration reports, regulatory submissions and decision records.

**Digital / information role:** Preserve source, ownership, version, location, quality, access restrictions and lineage of information. Ensure technical records can be found and interpreted later.

### Phase 2 — Appraisal and concept selection

**What happens:** A discovery is assessed to understand reservoir extent and production potential. Development concepts are compared, such as a fixed platform, FPSO, subsea tie-back or phased development.

**Information examples:** Appraisal well data, reservoir models, production forecasts, concept studies, option evaluations, cost and schedule assumptions, risk registers and decision records.

**Digital / information role:** Establish controlled data sets and decision traceability. Make sure the selected concept and assumptions are identifiable and linked to the approved project basis.

### Phase 3 — FEED (Front-End Engineering Design)

**What happens:** The selected concept is developed to a level that defines the technical scope, design basis, major equipment, plot arrangements, process configuration, interfaces, cost estimate and execution strategy.

**Typical engineering outputs:**
- Design basis and engineering philosophies
- Process flow diagrams (PFDs) and P&IDs
- Equipment lists and preliminary equipment datasheets
- Plot plans, general arrangements and 3D model information
- Electrical load lists and single-line diagrams
- Instrument indexes and preliminary I/O lists
- Line lists, piping classes and material specifications
- Control, shutdown and safety-system philosophies
- Project specifications, interface registers and deliverable registers

**Digital / information role:** Define information requirements, tag-numbering rules, document metadata, classification, exchange formats, review workflows, model/data expectations and handover requirements early. This is where information requirements should be designed into project execution, not added at the end.

### Phase 4 — Detailed engineering and procurement

**What happens:** Engineering disciplines develop the design to construction / fabrication detail. Long-lead equipment and materials are specified, purchased and manufactured.

**Typical information outputs:**
- Approved-for-construction drawings
- Detailed P&IDs, isometrics and piping layouts
- Structural, civil, mechanical, electrical and instrumentation design deliverables
- Vendor datasheets, drawings, manuals and certificates
- Material requisitions, purchase orders and technical bid evaluations
- Equipment and instrument tag registers
- Cable schedules, termination drawings, loop diagrams and I/O lists
- Cause-and-effect charts, logic diagrams and control-system configuration records

**Digital / information role:** Manage revisions and approval status; connect tags to documents, models and vendor data; monitor deliverable completeness; control transmittals and technical queries; resolve duplicate or inconsistent identifiers; maintain traceable design changes.

### Phase 5 — Fabrication, construction and installation

**What happens:** Modules, jackets, topsides, pipelines and subsea equipment are fabricated, assembled, inspected, transported and installed. Offshore hook-up and integration connect systems and facilities.

**Information examples:** Fabrication drawings, weld maps, inspection and test records, material traceability, non-conformance reports, construction work packs, lifting / installation records, as-built mark-ups and punch lists.

**Digital / information role:** Maintain links between design intent and installed configuration. Capture field changes and redlines, track construction status and ensure accepted changes are reflected in controlled records.

### Phase 6 — Commissioning and start-up

**What happens:** Systems are checked, tested, cleaned, flushed, pressure-tested, energised and functionally verified. The facility is prepared for safe start-up and production.

**Information examples:** Systemisation / subsystem registers, commissioning procedures, test packs, inspection certificates, loop folders, cause-and-effect test records, punch lists, operating procedures, training records and handover certificates.

**Digital / information role:** Support system-based completion and evidence. Confirm required documents, equipment data, certificates, procedures and maintenance data are available before systems are handed to operations.

### Phase 7 — Operations and maintenance

**What happens:** The facility produces, processes and exports hydrocarbons. Teams monitor performance, operate equipment, inspect assets, maintain systems, manage integrity and execute modifications.

**Information examples:**
- Current P&IDs, layouts and electrical drawings
- Equipment master data and technical attributes
- Operating procedures and alarm / trip information
- Preventive maintenance plans and work orders
- Inspection, corrosion and integrity records
- Instrument calibration and proof-test records
- Management-of-change records
- Incident, reliability and performance data
- Vendor manuals, certificates and spare-parts data

**Digital / information role:** Keep the operational information baseline accurate and usable. Support EAM / CMMS, document management, engineering applications, data platforms and operational reporting. Make sure changes are reviewed, approved, implemented and reflected across connected systems.

### Phase 8 — Late-life operations and decommissioning

**What happens:** The operator evaluates continued operation, life extension, cessation of production, well plugging and abandonment, removal or leaving-in-place options, site remediation and regulatory close-out.

**Information examples:** Asset condition and integrity records, well barrier records, subsea and pipeline records, hazardous-material inventories, decommissioning plans, removal records, environmental monitoring and final close-out evidence.

**Digital / information role:** Provide trustworthy records of what exists, where it is, its condition, interfaces, materials and history. Support risk assessment, safe execution, regulatory evidence and final information retention / transfer.

**Key principle:** Decommissioning should be considered during project development and design, not only when production stops.

## 6. What is FEED, EPC, EPCM and EPCI?

These terms describe common project delivery approaches. Contract definitions vary, so always check the actual contract and project execution plan.

| Term | Expanded form | General meaning |
|---|---|---|
| FEED | Front-End Engineering Design | Defines the project scope and design basis before detailed execution |
| EPC | Engineering, Procurement and Construction | Contractor engineers, procures and constructs the defined scope |
| EPCM | Engineering, Procurement and Construction Management | Contractor provides engineering, procurement and construction-management services; the owner may hold construction contracts |
| EPCI | Engineering, Procurement, Construction and Installation | Includes offshore installation within the contracted scope |
| O&M | Operations and Maintenance | Activities to operate, inspect, maintain and support the asset |

A project may use multiple contractors and contract packages. The operator / owner remains responsible for defining requirements, governance, acceptance and operation of the asset, subject to the applicable contractual and regulatory framework.

## 7. Who does what? Main industry stakeholders

| Stakeholder | Typical responsibility | Information contribution |
|---|---|---|
| Asset owner / operator | Owns or operates the field / facility; sets business and technical requirements | Asset requirements, standards, approvals, operating baseline and handover acceptance |
| Regulator / government authority | Grants rights, regulates safety, environment and resource management | Permits, submissions, compliance evidence, reports and regulatory records |
| Engineering consultant / FEED contractor | Develops concept and front-end design | Design basis, studies, PFDs, P&IDs, layouts, estimates and specifications |
| EPC / EPCI contractor | Executes engineering, procurement, construction and possibly installation | Detailed design, vendor data, construction records, test evidence and as-built information |
| Drilling contractor | Supplies and operates drilling unit / services under contract | Rig, well and drilling-operation records |
| OEM / vendor | Designs or supplies equipment and packaged systems | Datasheets, drawings, manuals, certificates, spare-parts and recommended maintenance data |
| Installation / marine contractor | Installs offshore structures, pipelines or subsea equipment | Installation procedures, vessel / survey records, as-installed coordinates and reports |
| Operations team | Runs the asset safely and reliably | Operating procedures, work orders, shift logs, operating data and change requests |
| Maintenance / integrity team | Maintains equipment and verifies asset condition | Maintenance history, inspection reports, integrity assessments and repair records |
| Digital / information-management team | Defines, governs, integrates and assures information | Information requirements, registers, metadata, data quality reports, handover packs and system interfaces |

## 8. The digital engineering connection — why this chapter matters to your role

A facility is not just steel, piping and equipment. It is also a large body of connected information describing the asset's requirements, design, configuration, installation, operation, maintenance and history.

Digital Engineering connects engineering methods, information, models, systems and workflows across the lifecycle. Engineering Information Management (EIM) focuses on governing and controlling engineering information. Asset Information Management (AIM) focuses on ensuring the information needed to manage and operate the asset is complete, accurate, accessible and maintained.

These disciplines overlap, but are not identical to process engineering, mechanical design, subsea engineering or operations authority.

### 8.1 Information objects you should learn to recognise

| Information object | What it tells you | Typical relationships |
|---|---|---|
| Asset / facility | Which physical asset is being managed | Contains areas, systems, equipment and structures |
| Area / system / subsystem | Functional or physical grouping | Contains equipment, lines, instruments and documents |
| Equipment tag | Unique identifier for an item of equipment | Links to datasheet, drawings, maintenance and vendor records |
| Instrument tag | Identifier for a measurement or control device | Links to instrument index, loop, I/O, P&ID and calibration records |
| Line number | Identifies a process or utility piping line | Links to line list, P&ID, isometric and inspection records |
| Document number | Identifies a controlled engineering document | Has title, revision, status, discipline, lifecycle and references |
| 3D object | Digital representation of a physical component | Should map to tags, attributes, documents and system context |
| Vendor data item | Supplier-provided technical information | Links to purchase package, equipment tag and handover requirements |
| Maintenance object | Object managed in an EAM / CMMS | Links to equipment master, task list, plan, work order and history |
| Change record | Records an approved change to design or configuration | Links request, impact assessment, approvals, affected objects and close-out |

### 8.2 Example: one pump, many connected records

Imagine a pump with tag **P-101**.

Its information may include:

- Equipment register record: tag, description, equipment type, area and service.
- P&ID: shows process connections, valves and instruments.
- Equipment datasheet: duty, design conditions and technical requirements.
- 3D model: physical location, dimensions and interfaces.
- Vendor documents: certified drawings, manual, certificates and spare-parts list.
- Electrical records: motor, cable, load and single-line references.
- Instrument records: associated pressure, temperature, vibration or flow instruments.
- EAM / CMMS record: functional location, equipment master, maintenance plans and work history.
- Operations records: operating procedures, isolation requirements and abnormal-event history.
- Change records: approved modifications and updated as-built information.

If the pump is replaced or its service changes, the change may affect multiple records and systems. A drawing update alone does not guarantee that the equipment master, maintenance plan, vendor document set and 3D model have also been updated.

**This is a central EIM / AIM problem:** ensuring that connected information remains consistent with the approved and installed asset configuration.

### 8.3 Typical Digital Engineering / EIM / AIM responsibilities

Depending on the employer and project, responsibilities may include:

1. Define information requirements and deliverable requirements.
2. Establish tag-numbering, document-numbering and classification rules.
3. Maintain equipment, instrument, line, cable and document registers.
4. Administer engineering content and controlled revisions.
5. Coordinate information exchange between operator, EPC, OEM and other contractors.
6. Validate completeness, uniqueness, consistency and relationships in submitted data.
7. Manage 3D model / document / tag associations and digital handover.
8. Map engineering data to EAM / CMMS and other operational systems.
9. Support asset information standards, governance and data ownership.
10. Monitor data quality and resolve defects before handover and during operations.

You may be asked to configure, validate or govern information in systems such as engineering document-management platforms, 3D / engineering applications, data handover tools, SAP or IBM Maximo. The actual technology stack varies by company.

## 9. Important concepts and abbreviations

| Term | Meaning |
|---|---|
| E&P | Exploration and Production |
| FEED | Front-End Engineering Design |
| EPC | Engineering, Procurement and Construction |
| EPCM | Engineering, Procurement and Construction Management |
| EPCI | Engineering, Procurement, Construction and Installation |
| O&M | Operations and Maintenance |
| FPSO | Floating Production, Storage and Offloading |
| FSO | Floating Storage and Offloading |
| MODU | Mobile Offshore Drilling Unit |
| PFD | Process Flow Diagram |
| P&ID | Piping and Instrumentation Diagram |
| EAM | Enterprise Asset Management |
| CMMS | Computerised Maintenance Management System |
| MOC | Management of Change |
| OEM | Original Equipment Manufacturer |
| FAT | Factory Acceptance Test |
| SAT | Site Acceptance Test |
| As-built | Record reflecting the installed / accepted configuration |
| Brownfield | Work on or modification to an existing operating asset |
| Greenfield | Development of a new asset or facility |
| Tie-back | Connection of a remote field / subsea development to an existing host |
| Handover | Formal transfer of systems, responsibilities and required information to the receiving organisation |

## 10. What depth is required for your target role?

Use this depth guide to avoid spending time learning the wrong things.

| Subject | Required depth | What you should be able to do |
|---|---|---|
| Upstream / midstream / downstream | Strong overview | Explain activities, assets, outputs and interfaces |
| Exploration / appraisal / production | Functional overview | Explain why each phase exists and what information it produces |
| Offshore development concepts | Functional understanding | Distinguish platform, FPSO, subsea tie-back, pipeline and LNG interfaces |
| Process equipment | Recognition and purpose | Identify common equipment and understand its role in a process |
| Process calculations / reservoir engineering | Awareness only initially | Understand terminology and know when a specialist is responsible |
| FEED / EPC / commissioning | Strong working knowledge | Understand deliverables, gates, reviews, changes and handover |
| Engineering drawings and registers | Practical working knowledge | Read basic P&IDs, tag registers, equipment lists and document metadata |
| EIM / AIM / digital handover | Deep working knowledge | Define, validate, govern, relate and assure information |
| EAM / CMMS | Practical working knowledge | Understand asset hierarchy, equipment master, functional location, maintenance plans and work orders |
| Safety and regulatory obligations | Awareness and respect for authority | Recognise safety-critical information and follow approved governance; never act as technical authority without competence and authorisation |

**Your learning priority:** understand the asset and its lifecycle well enough to manage its information. You do not need to become a reservoir engineer, process designer or subsea equipment designer to enter an EIM / AIM pathway.

## 11. Practical exercises

Complete these exercises using fictional examples only. Do not upload confidential employer or client data.

### Exercise A — Classify the activity

For each activity, identify upstream, midstream or downstream. Some activities can be classified differently in different organisations; explain your reasoning.

1. Drilling an offshore exploration well.
2. Operating a subsea production tree.
3. Transporting gas through a long-distance export pipeline.
4. Liquefying natural gas at an LNG export plant.
5. Refining crude oil into diesel.
6. Distributing natural gas to industrial customers.
7. Storing crude oil at an export terminal.
8. Processing production fluids at an offshore platform.

### Exercise B — Trace an offshore development

Draw a simple flow diagram for a fictional offshore gas field. Include:

- Reservoir and production well
- Subsea tree
- Manifold
- Flowline
- Riser
- Host platform or FPSO
- Separation / gas treatment / compression
- Export pipeline
- Onshore gas processing or LNG facility
- End customer

Add the condensate and produced-water paths. Mark the boundary between offshore operator and pipeline / receiving-facility operator.

### Exercise C — Identify information deliverables by lifecycle phase

Create a table with these columns:

`Lifecycle Phase | Activity | Information / Document | Responsible Party | Receiving Party | Validation Check`

Add at least two records for each of these phases:
- FEED
- Detailed engineering / procurement
- Construction / installation
- Commissioning
- Operations

Example validation checks: unique tag, correct revision, approved status, required attributes populated, document-to-equipment relationship valid, vendor document linked to the correct equipment tag.

### Exercise D — Build a simple information relationship

For fictional pump P-101, list at least eight information objects that should be linked to it. Include at least one drawing, one datasheet, one vendor document, one 3D representation and one maintenance record.

Explain what could go wrong if the pump tag changes but the connected records are not updated.

## 12. Knowledge assessment

Answer in your own words; do not simply copy the chapter.

1. What is the difference between the oil and gas value chain and the project / asset lifecycle?
2. Explain upstream, midstream and downstream with one offshore-related example each.
3. What is the difference between a fixed platform, an FPSO and a subsea tie-back?
4. What is FEED, and why are information requirements important before detailed engineering begins?
5. Name five types of information that should be handed over before a facility enters operations.
6. Why is an as-built record important?
7. What is the difference between EIM and AIM at a functional level?
8. A pump is replaced. Which engineering and operational information may need to be reviewed or updated?
9. Why should decommissioning be considered during project development?
10. Which tasks in this chapter belong to an information professional, and which require engineering or operational technical authority?

## 13. Recommended external study resources

Use these as recurring reference sources. Public regulatory and industry material is useful for understanding terminology and lifecycle context; always check the applicable country, regulator, contract and current revision for real projects.

### Industry value chain and terminology

- [U.S. Environmental Protection Agency — Oil and Gas Sector Information](https://www.epa.gov/smartsectors/oil-and-gas-sector-information) — concise explanation of upstream, midstream and downstream.
- [GPA Midstream — What is Midstream?](https://www.gpamidstream.org/about/what-is-midstream/) — useful explanation of gathering, processing, transportation and storage.
- [Library of Congress — Oil and Gas Industry Research Guide](https://guides.loc.gov/oil-and-gas-industry/introduction) — broad research guide and links to glossaries and reference material.
- [IOGP Europe — Glossary](https://iogpeurope.org/glossary/) — industry terminology, including gas supply-chain segments.

### Offshore operations and project lifecycle

- [U.S. EIA — Offshore Oil and Natural Gas in Depth](https://www.eia.gov/energyexplained/oil-and-petroleum-products/offshore-oil-and-gas-in-depth.php) — accessible overview of offshore production.
- [BOEM / BSEE — General Life Cycle of Offshore Oil and Gas Exploration and Production Operations (PDF)](https://www.boem.gov/sites/default/files/documents/oil-gas-energy/national-program/BSEE%20Lifecycle%20of%20Oil%20and%20Gas%20Offshore%20Exploration_0.pdf) — lifecycle graphic and stages.
- [BOEM — Exploration and Development Plans](https://www.boem.gov/oil-gas-energy/exploration-and-development-plans) — how exploration and development plans are reviewed in the U.S. Outer Continental Shelf context.
- [NOPSEMA — Decommissioning Guidance and Tools](https://www.nopsema.gov.au/offshore-industry/decommissioning/guidance-and-tools) — explains lifecycle planning and decommissioning expectations in Australia's offshore regulatory context.

### India-specific context

- [Oil Industry Safety Directorate (OISD) — Exploration and Production](https://oisd.gov.in/exploration-and-production-section) — India's offshore petroleum safety regulatory context and OISD material.
- [Directorate General of Hydrocarbons (DGH)](https://dghindia.gov.in/) — Indian upstream sector information, policies and reports.

### Useful terminology reference

- [SLB Energy Glossary](https://glossary.slb.com/) — searchable technical definitions. Use it when unfamiliar terms appear in lessons or project documents.

---

## 14. Completion checklist

Do not mark this lesson complete just because you have read it.

- [ ] I can explain upstream, midstream and downstream without looking at the chapter.
- [ ] I can trace a simplified offshore gas development from reservoir to market.
- [ ] I can distinguish platform, FPSO, subsea development, pipeline and LNG terminal.
- [ ] I understand the main project lifecycle stages from exploration to decommissioning.
- [ ] I can identify key deliverables created during FEED, detailed engineering, construction, commissioning and operations.
- [ ] I can explain how tags, documents, models, vendor data and maintenance records relate to one equipment item.
- [ ] I completed Exercises A–D.
- [ ] I answered the 10 assessment questions.
- [ ] I recorded open questions and a confidence score in the study log.

**Completion status:** STUDY MATERIAL AVAILABLE — awaiting learner exercises and assessment.

**Next lesson:** Lesson 02 — Oil and Gas Project Lifecycle in more detail, including project phases, decision gates, deliverables and information handover.
