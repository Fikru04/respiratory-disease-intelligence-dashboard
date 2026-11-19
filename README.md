##Respiratory Disease Intelligence Dashboard
> Developed during the November 16–18, 2026 Microsoft–CDC Buildathon, with Microsoft engineers serving as technical coaches.
Public Data Notice
This project uses only publicly available surveillance, laboratory, mortality, hospitalization, policy, and news data. No restricted, confidential, patient-level, proprietary, personally identifiable, or internal government data were used. The datasets can be obtained directly from their respective public providers.
##Overview
This proof of concept demonstrates how public respiratory-disease data can be transformed into timely, leadership-focused situational awareness. The project integrates U.S. surveillance, laboratory testing, hospitalization, mortality, policy, and news information into a unified dashboard. England is included only as an external comparator. U.S. data, interpretation, and implications remain primary.
The intelligence workflow addresses four leadership questions:
What changed?
What does the overall signal mean?
What is likely to happen next?
What questions should leaders be prepared to answer?
##Version 6.1
Version 6.1 retains the original Buildathon dashboard design and adds an AI-assisted intelligence layer:
Change Brief: Identifies meaningful changes since the previous reporting period.
Signal-Convergence Assessment: Explains whether indicators support a consistent or mixed respiratory-disease narrative.
Near-Term Outlook: Describes the potential direction of activity over the next two to six weeks, with uncertainty clearly stated.
Leadership Question Forecast: Anticipates likely leadership questions and provides evidence-based response framing.
AI-generated content supports, but does not replace, epidemiologic and public-health judgment. Material findings should be reviewed before leadership distribution.
##Key Features
U.S.-first respiratory-disease situational awareness
NREVSS multi-virus surveillance
Influenza, RSV, COVID-19, and adenovirus views
Hospitalization and mortality context
U.S.–England directional comparison
Seasonal baseline and upper-expected-limit calculations
Statistical signal detection
Historical periods of unusually high activity
Policy and news integration
Leadership-oriented interpretation
Self-contained HTML dashboard with embedded visualizations
Dashboard Logic
Typical for This Week
The historical median for the same ISO week, using a plus-or-minus two-week seasonal window.
Upper Expected Limit
The larger of:
Q3 + 1.5 × IQR
Median + 3 × MAD × 1.4826
The upper expected limit is never lower than the baseline.
Surveillance Status
Potential outbreak signal — investigate: At least two consecutive observations above the upper expected limit
One-week alert — verify next report: Exactly one observation above the upper expected limit
Approaching unusual activity: Observed value is at least 80% of the upper expected limit and the trend is increasing
Rising within expected range: The trend is increasing but remains below 80% of the upper expected limit
Within expected range: All other observations
These classifications are national statistical signals. They do not confirm outbreaks.
Data Sources
United States
CDC National Respiratory and Enteric Virus Surveillance System (NREVSS)
CDC national respiratory-virus test positivity data
National Healthcare Safety Network (NHSN) hospitalization data
National Center for Health Statistics (NCHS) mortality data
England Comparator
UK Health Security Agency respiratory surveillance feeds
Policy Context
Advisory Committee on Immunization Practices
U.S. Food and Drug Administration
Joint Committee on Vaccination and Immunisation
Medicines and Healthcare products Regulatory Agency
News and Official Context
Publicly available news reports
Publicly available government and public-health summaries
##Architecture
```text
Public Data Sources
        ↓
Data Ingestion and Standardization
        ↓
Seasonal Baselines and Signal Detection
        ↓
Surveillance Analytics and Visualizations
        ↓
AI-Assisted Intelligence Layer
        ↓
Leadership-Focused Dashboard
```
Suggested Repository Structure
```text
respiratory-disease-intelligence-dashboard/
├── README.md
├── LICENSE
├── .gitignore
├── dashboard/
│   └── respiratory_disease_intelligence_dashboard_v6_1.html
├── docs/
│   ├── dashboard-home.png
│   ├── pathogen-view.png
│   ├── architecture-diagram.png
│   └── buildathon-summary.pdf
└── assets/
    └── microsoft-buildathon-badge.png
```
Running the Dashboard
The dashboard is a self-contained HTML file:
Download or clone the repository.
Open `dashboard/respiratory_disease_intelligence_dashboard_v6_1.html` in a modern browser.
No web server or installation is required for the static demonstration.
##Buildathon Collaboration
This project was developed during a three-day Buildathon held November 16–18, 2026, through collaboration between CDC and Microsoft.
The Buildathon brought together public-health, analytics, and technology team members to explore how AI-assisted solutions can improve respiratory-disease situational awareness using publicly available data.
Microsoft engineers served as technical coaches and advisors throughout the event, providing guidance on architecture, data integration, AI capabilities, prompt design, dashboard development, and the effective use of Microsoft technologies. CDC participants contributed public-health subject-matter expertise, data interpretation, requirements, testing, validation, and user-centered feedback.
The project was presented during the final-day showcase and evolved from a surveillance dashboard into an AI-assisted respiratory-disease intelligence platform organized around four leadership questions:
What changed?
What does the overall signal mean?
What is likely to happen next?
What questions should leaders be prepared to answer?
The work combined:
Public-health problem framing
Data-source identification and validation
Data integration and quality review
Statistical surveillance and signal-detection methods
Dashboard and visualization design
Prompt engineering and AI-assisted analysis
User testing and feedback
Leadership-focused communication and situational awareness
##Lessons Learned
The largest challenges were primarily related to infrastructure readiness rather than analytics or AI:
Obtaining appropriate access and permissions
Establishing secure and reliable data connections
Resolving firewall and network restrictions
Once these foundational requirements were addressed, the team was able to focus on analytics, visualizations, and AI-assisted interpretation.
For future Buildathons, access, connectivity, and firewall requirements should be addressed before the event begins. A high-level overview of the Microsoft products, services, and target architecture should also be provided at the outset so participants share a common understanding of how the components fit together.
##Recognition
Microsoft–CDC Buildathon participant
Microsoft Buildathon badge recipient, pending issuance
Add the official badge image to `assets/` after receipt and update this section with the verified badge name and credential link.
Responsible Use
Treat generated narratives as decision-support content, not autonomous conclusions.
Validate important findings against the underlying source data.
Communicate uncertainty, reporting delays, and provisional values.
Do not infer localized outbreaks from national test-positivity data alone.
Use England as contextual evidence only, not as a direct predictor or policy driver for the United States.
##Disclaimer
This repository contains a proof-of-concept respiratory-disease intelligence dashboard created for educational, demonstration, and situational-awareness purposes.
All datasets used in this project are publicly available. No restricted, confidential, internal, patient-level, or personally identifiable information was used.
The analyses, visualizations, statistical classifications, and AI-assisted summaries do not constitute clinical guidance, policy recommendations, or official public-health determinations. Statistical signals shown in the dashboard should not be interpreted as confirmation of outbreaks. Confirmation requires additional evidence such as geographic clustering, clinical severity, hospitalization patterns, genomic linkage, or case review.
Any interpretations or conclusions presented in this repository are those of the project contributors and do not represent official positions, policies, or endorsements of CDC, HHS, Microsoft, or any other organization.
Data Availability
All datasets used in the project are publicly available from their respective source organizations. No special access, clearance, or permission is required to obtain the source data. Users should review and comply with each provider’s applicable terms, attribution guidance, and update schedules.
License
Before selecting a license, confirm that the repository contains only material the project contributors are authorized to publish. For a demonstration repository containing original documentation and code, a standard open-source license such as MIT may be appropriate. Third-party data remain subject to their original providers’ terms.

