# Project Summary <!-- Typically 500 words -->

## Scope

The project will deliver a consistent, repeatable and secure internal development platform for hosting the client's application services. (S1)

The organisation intends to become fully cloud native, but currently lacks a shared approach for building and managing services. (S1, S16)

Application teams are not consistently following the same deployment patterns. (S3, S16)

Teams repeat decisions about CI/CD, repositories, resource naming, resource tagging, permissions, identity and user management. (S16)

This inconsistency risks security misconfigurations, avoidable shortcuts and slow project starts. (K3, S2)

Building a paved-road platform on which application teams can deploy addresses these issues. (S1, S2)

Built-in guardrails also support NIST compliance and protect personal data through least-privilege access and data residency controls. (S3, B3)

## Business Impact

- Pre-built scaffolding means teams can start building a new application quickly (K1)
- CI/CD pipelines with properly scoped permissions are built in (K26, B3)
- Rules around networking, resource naming, access, managed identities and security are already in place (K25, B3)
- Static code scanning (SonarQube) and vulnerability analysis (Trivy) are already built in to guard against security issues (K25, K26)
- Terraform infra-as-code modules for client resources already exist (K5, K26)
- Azure DevOps setup (user stories management) comes with sensible defaults (S5)

The business can be confident that teams building or migrating services work within established guardrails, not without oversight. (K1, K25)

## Implementation plan

A platform approach was selected because it removes duplicated effort and enforces security by default, rather than relying on each team's individual discipline. (S17)

### Analysis & Business Case

A stakeholder workshop and user-story mapping exercise will elicit functional and non-functional requirements from application developers, technical architects and business stakeholders. Requirements will be analysed and prioritised using MoSCoW, with the agreed target of standing up a new project within one working day. (S18)

A build, hire or buy options appraisal will use capability mapping to compare the proposed platform against the alternatives. This technique is appropriate because it explicitly compares required capabilities, ownership, delivery effort and operational support rather than relying on feature lists alone. The analysis will also explain the fit of capability mapping and whether a weighted decision matrix is needed to compare criteria such as cost, security, maintainability and time to value. (K2, K4, K18)

Cost and time estimates will use an initial resource day-rate calculation for internal staff and supplier inputs, supported by story-point estimation for implementation backlog items. Estimates will be re-baselined after each sprint demo and recorded in the project plan. (K15)

The project will maintain a risk and opportunity log. Each item will be scored for likelihood and impact, with named owners and clearly defined mitigation or exploitation activities. Key risks include inconsistent platform adoption, security misconfiguration and delivery delay; opportunities include reusable modules, faster onboarding and broader automation. (K3, S2)

### Project delivery methods

Agile (Scrum) suits iterative platform delivery with early feedback from application teams. (S5) Work is tracked in Azure DevOps with Project Managers, and deviations from specification are handled through backlog reprioritisation. (S6)

Sprint demos will update technical stakeholders, with plain-language milestone reports for non-technical stakeholders. (K17, S13, B5)

### Technical Implementation

Research will cover Azure landing zones, responsibility boundaries, Terraform state management, layered security and least privilege. The preferred design will be justified through a weighted decision matrix that compares evidence against agreed criteria. Where decisions remain uncertain, targeted proof-of-concept benchmarks will compare configuration and performance before a recommendation is made. (K18)

The main innovation will be to investigate ephemeral, self-hosted Azure DevOps runner pools and OpenID Connect federated credentials for CI/CD authentication. These approaches will be evaluated against traditional fixed runners and stored service-connection secrets using security, provisioning time, cost and operational complexity as the criteria. (S14)

Architecture diagrams and terraform module tests will document and validate the platform (K27), with pull request reviews and branch policies applied throughout. (S19)

Non-functional performance and security benchmarks will be used alongside MoSCoW prioritisation to verify that the platform meets the agreed onboarding and vulnerability requirements. (S18)

### Timescales (K15)

- 2 weeks: research, options appraisal and sign-off
- 6 weeks: implementation in Scrum sprints
- 2 weeks: roll-out, feedback and lessons-learned review

### Success Measures

Success will be measured by time to first deployment, the number of application teams onboarded and the number of security findings resolved. Benchmarks will also verify that no application deploys with a High or Critical vulnerability and that a new project can be stood up within one working day. (S18)

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
