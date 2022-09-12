# ESGF Compute Working Team Meeting - 2022-09-12

## Logistics

Where: Zoom
When:  12/09/2022
Who:   ESGF CWT

## Actions

- [ ] AS: Report recommencement of CWT meetings to ESGF XC
- [ ] AS: Publish and share meeting minutes
- [ ] AS: Draft a roadmap
- [ ] AS: Draft terms of reference

## Agenda

1. Welcome and introductions
2. CWT Logistics
   - chairs
     - Ag Stephens (CEDA)
     - Carsten Ehbrecht (DKRZ)
   - team
     - all who are interested 
   - meetings
     - 12/09, 10/10, 14/11, 12/12 - second Monday of each month 3pm (UK), 4pm (CET)
     - public minutes on GitHub
     - every third meeting (i.e. quarterly), "share and discuss" theme:
       - Discuss alternative approaches used by members of the CWT
       - Discuss alternative approaches used by external organisations/projects (invited to specific meetings)
       - Capture new requirements
       - Discuss proposals for future developments
       - Include/merge with other relevant meetings: e.g. the quarterly Birdhouse meetings
       - Investigate other technologies/approaches: e.g. Cloud, Containers, Machine Learning, etc.
   - communication
     - Slack: #cwt (https://esgf-chat.slack.com/archives/C8CQPTQSJ)
     - GitHub: https://github.com/ESGF/esgf-cwt
     - Interactions:
       - IS-ENES3
       - ESGF Working Teams
       - C3S, IPCC etc 
   - reporting
     - to Executive Committee (XC) as required
   - concerns
     - should any member want to raise concerns about how the CWT is being managed then they should raise them with the ESGF XC.
   - terms of reference
     - needed (see action)
3. CWT plan:
   - Reboot proposal Google Doc: https://docs.google.com/document/d/1IZNJXfG2IXf4GDNxh4CZYkXyQbcePp4tL7AIDUdhycM/edit#
   - objectives:
     - Develop a single, shared solution for ESGF compute.
     - Gather support and collaboration for co-development and maintenance of the ESGF compute solution.
     - Provide a comprehensive testing framework to ensure robust and reliable WPS processes when working with major ESGF datasets.
     - Provide guidance and support on how to deploy and manage compute nodes.
     - Report to the ESGF Executive Committee and liaise with other ESGF Working Teams
     - Undertake continuous improvement of the ESGF compute solution through (i) ongoing review/discussion and (ii) openness to new and changing technologies/developments.
4. Technologies and focus:
   - Functional priorities: 
     - Python open source code-base
     - Data-reduction - i.e. subsetting (time, level, lat, lon), averaging (time, level, horizontal space)
     - Integration with authentication systems developed in ESGF
   - Proposed solution:
     - roocs: 
       - https://roocs.github.io/overview/ 
       - Developed, and running in production, to support subsetting of CMIP6 data for the C3S Climate Data Store
       - Running at CEDA, DKRZ and IPSL
       - Python, Xarray, Intake, Birdhouse WPS
       - Notebook example clients use the "rooki" client library that hides the WPS interface (if preferred)
       - Used as the data source for the IS-ENES3 compute prototype, which employs the Climate4Impact portal as its frontend. 
       - deployable on single machine or cluster (using Slurm)
5. Code management:
   - A new GitHub repository at https://github.com/ESGF/esgf-cwt for communication within, and about, the CWT; and project meeting notes
   - (existing) GitHub repositories for code - with agreed procedures for code review, pull requests and releases
   - GitHub issues to track issues
   - GitHub projects to manage and communicate the Roadmap
6. Roadmap (proposed):
   - Restart CWT Meetings
   - Improve systems for monitoring/logging usage/problems (extending Dashboard)
   - Deploy production CWT Node ("rook" WPS) on VMs at CEDA and DKRZ using Ansible recipes
   - Document the installation process for the VM-based deployment
   - Publicise the new service and plan user feedback/review
   - Review by collaborators and users
   - Respond to feedback with a new plan
   - Engage with CWT partners on requirements for deploying on their nodes
   - Develop Docker/Kubernetes/VM recipes as required
7. Discussion and questions
8. Next steps:
   - Agree/publish our roadmap
   - add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
   - Fork github.com/ESGF/esgf.github.io/
     - commit updates, and create a PR for SA to merge
 
# Notes
