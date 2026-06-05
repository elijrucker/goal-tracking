# Jack of Diamonds - AWS Skill Builder Learning Plan

## Card Details

- **Card**: Jack of Diamonds
- **Suit**: Diamonds
- **Domain**: Tools & Platforms
- **Color Tier**: 🟠 Orange
- **Difficulty**: Advanced

---

## Status

- **Current Status**: In Progress
- **Start Date**: 2026-05-15
- **Target Completion**: 2026-07-31
- **Completion Date**:
- **Time Invested**:

---

## Goal Description

Complete the official AWS Skill Builder Developer Learning Plan. This is the foundational AWS training that precedes the DVA-C02 exam prep course. Being official AWS content, it provides authoritative knowledge of AWS services and architecture relevant to the Developer Associate certification.

---

## Resources

- [AWS Skill Builder - Developer Learning Plan](https://skillbuilder.aws/search?la=cta&cta=topbanner&searchText=developer-learning-plan) - Official AWS training platform
- [AWS Well-Architected Framework](http://aws.amazon.com/architecture/well-architected/) - AWS best practices for building secure, high-performing, resilient, and efficient infrastructure
- [AWS CLI User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html) - Official AWS CLI documentation and reference
- [AWS Architecture Center](https://aws.amazon.com/architecture/) - Reference architectures, diagrams, and best practices
- [AWS Builder](https://builder.aws.com/) - Hands-on AWS building and experimentation platform

---

## Prerequisites

- [ ] 9♦️ - Boot.dev (foundational programming knowledge)

---

## Subtasks

- [x] AWS Cloud Practitioner Essentials
- [ ] Developer learning path modules _(Target: complete all 6 modules (18 courses) by 2026-07-31)_
  - [x] Phase 0 (2026-06-01)
  - [/] Phase 1 (2026-06-04)
  - [ ] Phase 2
  - [ ] Phase 3
  - [ ] Phase 4
  - [ ] Phase 5
  - [ ] Phase 6
- [ ] Review AWS DVA-C02 exam guide
- [ ] Complete AWS Skill Builder practice questions/knowledge checks

---

## Progress Notes

- [2026-06-01] Target set: complete all 6 learning path modules by 2026-07-31. Approximately 2-3 courses per week required. Revisit if summer course load increases.
- [2026-05-21] AWS dev environment container operational on ejr-homeserver. Python 3.12, Node.js 18, AWS CLI v2, CDK 2.1124.1 confirmed. AWS credentials mounted via volume from server. IAM user ejr-dev configured with PowerUserAccess and MFA. Node.js upgraded from 18 to 24 (Active LTS, supported through April 2028) after encountering CDK deprecation warnings. CDK bootstrapped to us-east-1 (CDKToolkit CloudFormation stack created). ejr-dev IAM user temporarily granted AdministratorAccess for bootstrap, reverted to PowerUserAccess on completion. AWS billing budget updated to $40/month with alerts at 85% and 100%. Git identity configured via ~/.gitconfig volume mount rather than baking into Dockerfile — single source of truth, inherited automatically by container. Docker run command saved as ~/docker/aws-dev/run.sh for repeatability as container configuration grows. Container launched going forward via ./run.sh.
- [2026-05-19] Established AWS dev environment foundation on ejr-homeserver: Ubuntu 24.04 LTS installed and hardened (SSH key auth, password auth disabled), Tailscale running as exit node, Docker installed and verified. AWS container build in progress — language/runtime to be confirmed from course materials before finalizing image.
- [2026-05-14] Transitioned to In Progress — daily touch points established alongside summer coursework
- [2026-04-27] AWS Cloud Practitioner Essentials completed 2024-03-29 (certificate of completion achieved) — satisfies first subtask. 10-hearts c4d course building further AWS-adjacent developer foundation ahead of formal Skill Builder work.

---

## Completion Notes

---

## Reflection & Lessons Learned

### [2026-05-21]

- IAM user naming and credential management require the same "rebuild over debug" instinct applied to the server setup. Account hardening (MFA on both root and IAM user, PowerUserAccess scoping) established before any course work begins — professional habit over convenience.

---

## Unlocks

- K♦️ - AWS DVA Prep Course
