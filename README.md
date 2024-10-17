# Cloud-Native-Buildpacks
Create Docker images without Dockerfile with buildpacks

## Cloud Native Buildpacks

### What is CNBs?
- The CNB project was initiated by Pivotal and Heroku in January 2018 and joined the Cloud Native Computing Foundation (CNCF) as an Apache-2.0 licensed project in October 2018.
- Cloud Native Buildpacks (CNBs) **transform your application source code into container images** that can run on any cloud.
- With buildpacks, organizations can concentrate the knowledge of container build best practices within a specialized team, **instead of having application developers across the organization individually maintain their own Dockerfiles**.
- This makes it easier to know what is inside application images, enforce security and compliance requirements, and perform upgrades with minimal effort and intervention.

#
### Why CNBs?
- Control - Balanced control between App Devs and Operators.
- Compliance - Ensure apps meet security and compliance requirements.
- Maintainability - Perform upgrades with minimal effort and intervention.

#### Features of CNBs:
- It auto-detects your code's programming language and its version
- Advanced Caching
- <mark>Images can be built directly from application source without additional instructions</mark>.
- Supports more than one programming language family.
- Image contains only what is necessary.
- Leverage production-ready buildpacks maintained by the community.
