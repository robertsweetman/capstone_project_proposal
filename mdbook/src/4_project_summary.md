# Project Summary <!-- Typically 500 words -->

## Scope

The project will deliver a consistent, repeatable and secure cloud platform for hosting the client's services. (S1)

While the intention is to become fully cloud native, what's lacking is a shared approach for building and managing services. (S1, S16)

Teams are application focussed and, without guidance or automation, each would likely re-invent a slightly different wheel. (S3, S16)

Each would ask the business the same questions about CI/CD, repositories, resource naming, resource tagging, permissions, user management and so forth. (S16)

Inconsistency also risks security misconfigurations, shortcuts and slow project starts. (K3, S2)

Building a platform on which applications can live addresses all these issues. (S1, S2)

Built-in guardrails also support NIST compliance and protect personal data through least-privilege access and data residency controls. (S3, B3)

## Business Impact

- Pre-built scaffolding means teams can start building their new application quickly (K1)
- CI/CD pipelines with properly scoped permissions are built in (K26, B3)
- Rules around networking, resource naming, access, managed identities and security are already in place (K25, B3)
- Static code scanning (SonarQube) and vulnerability analysis (Trivy) are already built in to guard against security issues (K25, K26)
- Terraform infra-as-code modules for client resources already exist (K5, K26)
- Azure DevOps setup (user stories management) comes with sensible defaults (S5)

The business can be confident that teams building or migrating services work within established guardrails, not without oversight. (K1, K25)

## Implementation plan

A platform approach was chosen because it removes duplicated effort and enforces security by default, rather than relying on each team's discipline. (S17)

### Analysis & Business Case

A build, hire or buy options appraisal using capability mapping will compare alternatives (K2, K4, K18) and estimate cost and time. (K15)

### Project delivery methods

Agile (Scrum) suits iterative platform delivery with early feedback from application teams. (S5) Work is tracked in Azure DevOps with Project Managers, and deviations from specification are handled through backlog reprioritisation. (S6)

Sprint demos will update technical stakeholders, with plain-language milestone reports for non-technical stakeholders. (K17, S13, B5)

### Technical Implementation

Requires domain specific research around Azure landing zones, areas of responsibility, terraform state file management, layered security and least privilege. (K18)

The main innovations involve broadening the scope of the automation and using cutting edge Azure DevOps approaches, especially around CI/CD pipelines via managed identities and Azure DevOps pools. (S14)

Architecture diagrams and terraform module tests will document and validate the platform (K27), with pull request reviews and branch policies applied throughout. (S19)

Requirements will be prioritised using MoSCoW. (S18)

### Timescales (K15)

- 2 weeks, Research, business case & sign off
- 6 weeks, Implementation (Scrum sprints)
- 2 weeks, Roll-out, feedback & lessons learned review

### Success Measures

Time to first deployment, teams onboarded and security findings resolved will show whether requirements are met. (S18)

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
