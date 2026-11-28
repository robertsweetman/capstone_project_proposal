# Project Summary <!-- Typically 500 words -->

## Scope

The project will deliver a consistent, repeatable and secure internal development platform for hosting the client's application services. (S1)

The organisation intends to become fully cloud native, but lacks a shared approach for building and managing services. Application teams follow different deployment patterns and repeat decisions about CI/CD, repositories, naming, tagging, permissions and identity. (S1, S3, S16)

This inconsistency risks security misconfigurations, avoidable shortcuts and slow project starts. (K3, S2) A paved-road platform addresses these issues. Its built-in guardrails support NIST compliance and protect personal data through least-privilege access and data residency controls. (S2, S3, B3)

## Business Impact

The project will deliver:

- Pre-built scaffolding so teams can start a new application quickly (K1)
- CI/CD pipelines with properly scoped permissions (K26, B3)
- Guardrails for networking, naming, access, managed identities and security (K25, B3)
- SonarQube static analysis and Trivy vulnerability scanning in every pipeline (K25, K26)
- Reusable Terraform modules adapted from the client's existing infrastructure-as-code (K26)
- An Azure DevOps project template with sensible defaults (S5)

Turning existing assets into a self-service product gives the organisation a competitive advantage. New services reach market faster, cost less to start and carry lower security risk than bespoke builds. I will evidence this by comparing time to first deployment and set-up effort before and after adoption. (K1, K25)

## Implementation plan

A platform approach was selected because it removes duplicated effort and enforces security by default, rather than relying on each team's individual discipline. (S17)

### Analysis & Business Case

A stakeholder workshop and user-story mapping will elicit functional and non-functional requirements. These will be prioritised using MoSCoW, with a target of standing up a new project within one working day. (S18)

A build, hire or buy options appraisal will use capability mapping. Each option will then be scored in a weighted decision matrix. Stakeholders will agree the criteria in advance, aligned to strategic principles such as security by default and avoiding vendor lock-in. I will evaluate whether these techniques produced a sound decision. (K2)

The business case will set out costs, tangible and intangible benefits, payback period and risks for each option. I will assess how well it supported the decision compared with a cost-only comparison. (K4)

I will prepare the solution proposal with a range of digital tools and standard approaches, detailed in Research Needs. (K5, S5)

Cost and time will be estimated using staff and supplier day rates and story points. Each phase will have a budget with 10% contingency. Actuals will be tracked in Azure DevOps burndown charts and Azure Cost Management, overruns will be managed through MoSCoW scope trade-offs, and estimates will be re-baselined after each sprint demo. (K15)

The project plan will estimate risks and opportunities in a log scored for likelihood and impact, with owners and defined mitigation strategies:

- Low adoption, mitigated by early-adopter teams and onboarding guides
- Security misconfiguration, mitigated by policy-as-code and pipeline scanning
- Delivery delay, mitigated by contingency and scope trade-offs

Opportunities include reusable modules and broader automation. The log will be reviewed every sprint. (K3, S2)

### Project delivery methods

Agile (Scrum) suits iterative platform delivery with early feedback from application teams. (S5) Work is tracked in Azure DevOps with Project Managers, and deviations from specification are handled through backlog reprioritisation. (S6)

Sprint demos will update technical stakeholders, with plain-language milestone reports for non-technical stakeholders. (K17, S13, B5)

### Technical Implementation

I will compare and contrast the chosen design with alternatives and justify the research and evaluation methods used, as set out in Research Needs. (K18)

The main innovation will be ephemeral, self-hosted Azure DevOps runner pools and OpenID Connect federated credentials for CI/CD authentication. I will evaluate them against fixed runners and stored service-connection secrets on security, provisioning time, cost and operational complexity. (S14)

During implementation, I will interpret existing artefacts to drive design changes and record the outcomes in Architecture Decision Records (ADRs) and pull request comments. These artefacts include architecture diagrams, Terraform state, `terraform plan` diffs, SonarQube and Trivy reports, and pipeline logs. Updated diagrams and Terraform module tests will document and validate the platform. (K27) Pull request reviews and branch policies will apply throughout. (S19)

Performance and security benchmarks will be used to verify that the platform meets the agreed requirements. (S18)

### Timescales (K15)

- 2 weeks: research, options appraisal and sign-off
- 6 weeks: implementation in Scrum sprints
- 2 weeks: roll-out, feedback and lessons-learned review

### Success Measures

Success will be measured by time to first deployment, the number of teams onboarded and the number of security findings resolved. Benchmarks will also confirm that no application deploys with a High or Critical vulnerability. (S18)

## Lessons Learned

A review at roll-out will capture what worked, why, and recommendations for future projects. (S22)

<!--
[Typically 500 words. Must:
- Describe the project scope (what are you doing)
- Explain the business impact (why is it valuable)
- Include high level implementation plan (how will you do it and how long will each stage take)
- Tag where KSBs will be met in the project
The important thing is to convince the EPAO there is scope to hit all KSBs.]
-->
