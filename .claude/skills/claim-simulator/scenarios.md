# Pre-Built Scenarios

Ready-to-use patient encounter scenarios for the Claim Simulator.

---

## Scenario 1: The Clean Claim (Beginner)

### Patient Demographics
- **Name**: Maria Santos
- **DOB**: 1978-04-12 (47 years old)
- **Insurance**: Blue Cross Blue Shield PPO
- **Member ID**: BCB447821956
- **Copay**: $35

### Clinical Note

**Date of Service**: 2026-02-25
**Provider**: [Use NPI search to find a real Family Practice provider]
**Place of Service**: 11 (Office)
**Visit Type**: Established Patient

**Chief Complaint**: "My throat has been sore for 3 days"

**HPI**: 47-year-old female presents with 3-day history of sore throat. Reports difficulty swallowing, low-grade fever (100.2F at home), and mild fatigue. Denies cough, runny nose, or ear pain. No recent sick contacts. No known allergies.

**ROS**: Constitutional: Low-grade fever, fatigue. HEENT: Sore throat, difficulty swallowing. Negative: cough, rhinorrhea, otalgia, rash.

**Exam**:
- Vitals: T 100.4F, BP 118/72, HR 76, RR 16
- General: Alert, no acute distress
- HEENT: Pharynx erythematous with bilateral tonsillar exudates. No peritonsillar swelling. TMs clear bilaterally. Nares clear.
- Neck: Bilateral anterior cervical lymphadenopathy, tender
- Lungs: Clear to auscultation bilaterally

**Results**: Rapid strep test: Positive

**Assessment**: Acute streptococcal pharyngitis

**Plan**: Amoxicillin 500mg TID x 10 days. Push fluids. Return if worsening or no improvement in 48 hours.

### Expected Coding
- **Dx**: J02.0 (Streptococcal pharyngitis)
- **CPT**: 99213 (Established, low MDM) + 87880 (Rapid strep)
- **Expected outcome**: Clean claim, paid in full

### Learning Objectives
- Basic E/M level selection (2021 guidelines, MDM-based)
- Linking diagnosis to procedure
- Appropriate lab coding

---

## Scenario 2: The Coding Trap (Intermediate)

### Patient Demographics
- **Name**: Robert Chen
- **DOB**: 1955-08-30 (70 years old)
- **Insurance**: Medicare Part B
- **MBI**: 1EG4-TE5-MK72

### Clinical Note

**Date of Service**: 2026-02-25
**Provider**: [Use NPI search to find a real Internal Medicine provider]
**Place of Service**: 11 (Office)
**Visit Type**: Established Patient

**Chief Complaint**: "Diabetes follow-up, feet are tingling"

**HPI**: 70-year-old male with Type 2 diabetes mellitus on insulin, here for quarterly follow-up. Reports worsening tingling and numbness in bilateral feet over the past 2 months. Also notes increased thirst and urination. Last A1C was 8.9% three months ago. Has diabetic nephropathy with CKD stage 3 (last GFR 42). Also has hypertension controlled on lisinopril and COPD on home nebulizer.

**ROS**: Constitutional: Fatigue, increased thirst. Neuro: Bilateral foot numbness/tingling, worse at night. GU: Polyuria. Respiratory: Baseline dyspnea on exertion, no change. CV: No chest pain.

**Exam**:
- Vitals: BP 138/82, HR 72, RR 18, Wt 210 lbs
- General: Obese male, no acute distress
- CV: RRR, no murmurs
- Lungs: Decreased breath sounds bases bilaterally, no wheezes
- Extremities: No edema. Bilateral feet: decreased monofilament sensation 3/10 sites left, 4/10 sites right. Diminished ankle reflexes bilaterally. Skin intact, no ulcers.
- Neuro: Decreased vibration sense bilateral feet. Proprioception intact.

**Labs ordered**: A1C, BMP (GFR), urine microalbumin

**Assessment**:
1. Type 2 diabetes mellitus with diabetic polyneuropathy, poorly controlled
2. Type 2 diabetes with diabetic chronic kidney disease, stage 3
3. Essential hypertension
4. COPD, stable

**Plan**:
1. Increase insulin glargine from 30 to 35 units nightly
2. Start gabapentin 300mg QHS for neuropathy
3. Continue lisinopril 20mg daily
4. Diabetic foot care education
5. Recheck A1C and GFR in 3 months
6. Referral to podiatry

### Coding Challenges
- Multiple diabetes manifestation codes required
- CKD staging must be coded separately per guidelines
- Sequencing rules for diabetes with complications
- Correct E/M level for complexity (moderate vs high MDM?)
- HCC (Hierarchical Condition Category) implications for Medicare

### Expected Coding
- **Dx**: E11.65 (T2DM with hyperglycemia), E11.42 (T2DM with diabetic polyneuropathy), E11.22 (T2DM with diabetic CKD), N18.3 (CKD stage 3), I10 (Essential HTN), J44.1 (COPD with acute exacerbation) or J44.9 (COPD unspecified)
- **Note**: COPD is stable, so J44.9 not J44.1
- **CPT**: 99215 (High MDM — multiple chronic conditions, medication management, moderate data review)
- **Trap**: Students often undercode to 99214 or miss the hyperglycemia code

### Learning Objectives
- Diabetes combination codes and sequencing
- CKD staging as additional code
- High MDM criteria under 2021 E/M guidelines
- HCC coding for risk adjustment

---

## Scenario 3: The Denial Gauntlet (Advanced)

### Patient Demographics
- **Name**: James Washington
- **DOB**: 1960-11-15 (65 years old)
- **Insurance**: Medicare Part B (primary), AARP Medicare Supplement (secondary)
- **MBI**: 4RK7-TH2-WN83

### Clinical Note

**Date of Service**: 2026-02-25
**Provider**: [Use NPI search to find a real Orthopedic Surgery provider]
**Place of Service**: 24 (Ambulatory Surgical Center)
**Visit Type**: Surgical

**Pre-operative Diagnosis**: Right knee medial meniscus tear, right knee osteoarthritis

**Procedure Note**:
Patient brought to OR, placed supine. Timeout performed. Right knee prepped and draped. General anesthesia administered.

Arthroscopic examination revealed:
1. Complex tear of medial meniscus, posterior horn — partial meniscectomy performed
2. Grade III chondromalacia medial femoral condyle — chondroplasty performed
3. Loose body removed from intercondylar notch
4. Intact ACL and PCL
5. Lateral compartment — Grade I changes, no intervention

Total surgical time: 45 minutes. Patient tolerated procedure well. To recovery.

**Post-operative Diagnosis**: Right knee medial meniscus tear, right knee osteoarthritis with loose body

### Denial Traps Built In
1. **Bundling trap**: Meniscectomy + chondroplasty in same compartment — NCCI edit
2. **Coverage trap**: Knee arthroscopy for osteoarthritis — Medicare LCD restrictions
3. **Modifier trap**: Need modifier RT (right side), possible modifier 59/XS for unbundling
4. **Documentation trap**: Medical necessity for loose body removal
5. **Place of service trap**: ASC vs outpatient hospital billing differences

### Expected Coding
- **Dx**: M23.312 (Medial meniscus tear, right), M17.11 (Primary OA, right knee), M24.172 (Loose body, right knee)
- **CPT**: 29881-RT (Meniscectomy), 29874-RT-XS (Loose body removal — separate compartment), 29877 may bundle with 29881 in same compartment
- **Expected outcome**: Partial denial (CO-97 for bundled chondroplasty)

### Learning Objectives
- NCCI bundling edits for arthroscopic procedures
- Modifier 59/XS unbundling rules
- Medicare coverage limitations for knee arthroscopy
- ASC billing requirements
- Appeal strategy for bundled services

---

## Scenario 4: The Coverage Maze (Advanced)

### Patient Demographics
- **Name**: Patricia Williams
- **DOB**: 1958-03-22 (67 years old)
- **Insurance**: Medicare Part B
- **MBI**: 7NH3-PQ8-BK45

### Clinical Note

**Date of Service**: 2026-02-25
**Provider**: [Use NPI search to find a real Endocrinology provider]
**Place of Service**: 11 (Office)
**Visit Type**: Established Patient

**Chief Complaint**: "Need to get a continuous glucose monitor"

**HPI**: 67-year-old female with Type 1 diabetes mellitus diagnosed at age 12. Currently on insulin pump therapy (Omnipod 5). A1C has been 8.2% despite pump optimization. Experiencing frequent hypoglycemic episodes (3-4 per week), including 1 episode of hypoglycemic unawareness last month requiring assistance. Requests CGM (Dexcom G7) for better glucose management.

**Current Medications**: Insulin via pump (total daily dose ~42 units), lisinopril 10mg, atorvastatin 20mg

**Assessment**: Type 1 diabetes mellitus with hypoglycemia, on insulin pump, frequent hypoglycemic episodes with unawareness

**Plan**: Prescribe Dexcom G7 CGM system. Need to verify Medicare coverage requirements.

### Coverage Challenge
- **Question**: Does Medicare cover CGM for this patient?
- **Key factors**:
  - Must meet Medicare CGM criteria (therapeutic CGM vs personal CGM)
  - Must be on intensive insulin regimen (3+ daily injections OR pump)
  - Must perform SMBG 4+ times/day (or have documented need)
  - Must be seen by treating provider within 6 months
  - DME MAC requirements and specific HCPCS codes
  - Recent expansion of CGM coverage (check current NCDs)

### Expected Research Path
1. Search NCD for "continuous glucose monitoring"
2. Check LCD for DME MAC CGM requirements
3. Verify HCPCS: E2102 (CGM receiver), A9278 (CGM sensor)
4. Check if Dexcom G7 specifically is covered
5. Identify documentation requirements

### Learning Objectives
- Medicare DME coverage requirements
- NCD/LCD research workflow
- CGM-specific billing codes and policies
- Documentation requirements for DME coverage
- Understanding of MAC jurisdiction for DME

---

## Scenario 5: Full Cycle — From Cradle to Grave

### Overview
This scenario walks through EVERY phase of the revenue cycle for a single patient encounter, from pre-registration to final payment posting.

### Patient Demographics
- **Name**: Angela Rivera
- **DOB**: 1972-06-18 (53 years old)
- **Insurance**: UnitedHealthcare Choice Plus PPO (primary)
- **Member ID**: UHC884523107
- **Group**: TECH-CORP-2026
- **Copay**: $40 specialist / $250 ER
- **Deductible**: $1,500 (met: $1,200)
- **Coinsurance**: 20% after deductible
- **Out-of-pocket max**: $5,000 (used: $1,800)

### Phase 1: Pre-Registration & Scheduling
Patient calls requesting appointment for persistent abdominal pain, 2 weeks duration.
- Verify demographics
- Confirm insurance active
- Schedule appropriately (GI specialist vs PCP?)
- Collect copay information

### Phase 2: Eligibility Verification
- Verify UHC plan is active
- Confirm benefits for office visit + potential procedures
- Check referral/prior auth requirements
- Determine patient financial responsibility

### Phase 3: Clinical Encounter

**Date of Service**: 2026-02-25
**Provider**: [Search for a real Gastroenterology provider]
**Place of Service**: 11 (Office)

**Chief Complaint**: "Stomach pain for 2 weeks, getting worse"

**HPI**: 53-year-old female presents with 2-week history of epigastric pain, described as burning, worse after meals and when lying down. Associated with nausea, no vomiting. Denies melena, hematochezia, weight loss. Takes ibuprofen daily for back pain. Social history: occasional alcohol use, non-smoker.

**Exam**:
- Vitals: WNL
- Abdomen: Soft, moderate epigastric tenderness, no guarding/rebound, no masses, BS active
- Otherwise unremarkable

**Assessment**: Epigastric pain, GERD vs peptic ulcer vs gastritis. NSAID-induced gastropathy suspected.

**Plan**:
1. Omeprazole 40mg daily x 8 weeks
2. Discontinue ibuprofen, switch to acetaminophen
3. H. pylori stool antigen test
4. If no improvement in 4 weeks, schedule EGD
5. Dietary modifications counseling provided (15 minutes)

**Phase 4**: Code the encounter (Dx + CPT)
**Phase 5**: Build and submit the claim
**Phase 6**: Payment posting (ERA arrives with partial payment)
**Phase 7**: Patient billing (remaining balance after insurance)

### Learning Objectives
- Complete revenue cycle workflow
- Handoff points between RCM phases
- Financial responsibility calculation
- Payment posting with adjustments
- Patient statement generation
