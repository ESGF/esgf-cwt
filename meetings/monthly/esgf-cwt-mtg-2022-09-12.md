# ESGF Compute Working Team Meeting - 2022-09-12

## Logistics

Where: Zoom
When:  12/09/2022
Who:   ESGF CWT

## Actions

- [ ] AS: Report recommencement of CWT meetings to ESGF XC
- [ ] AS: Publish and share meeting minutes

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
   - communication
     - Slack: #cwt (https://esgf-chat.slack.com/archives/C8CQPTQSJ)
     - GitHub: https://github.com/ESGF/esgf-cwt
   - reporting
     - to Executive Committee (XC) as required
   - concerns
     - Should any member want to raise concerns about how the CWT is being managed then they should raise them with the ESGF XC.
   - terms of reference
     -  
3. CWT plan:
   - Reboot proposal Google Doc: https://docs.google.com/document/d/1IZNJXfG2IXf4GDNxh4CZYkXyQbcePp4tL7AIDUdhycM/edit#

Rebooting the ESGF CWT
We propose a reboot of the CWT in 2022, with a change of focus. The objectives of the new CWT will be to:
Develop a single, shared solution for ESGF compute.
Gather support and collaboration for co-development and maintenance of the ESGF compute solution.
Provide a comprehensive testing framework to ensure robust and reliable WPS processes when working with major ESGF datasets.
Provide guidance and support on how to deploy and manage compute nodes.
Report to the ESGF Executive Committee and liaise with other ESGF Working Teams
Undertake continuous improvement of the ESGF compute solution through (i) ongoing review/discussion and (ii) openness to new and changing technologies/developments.

The greatest challenge for the CWT is to unify the ESGF partners around a single solution. Such unification is desirable because (1) we do not have the capacity to support multiple solutions, and (2) collaborative development will enable greater concentration on the important areas of deployment and maintenance.
Functional priorities: data-reduction
We propose a Compute Node that delivers a standards-based API through WPS. Following the suggestions of the ESGF Future Architecture Report (Kershaw et al., 2020), we recommend that the CWT focuses on "data-reduction" operations because they have the potential to massively reduce the bandwidth and storage requirements across the globe if deployed at all nodes. The most effective operations for data-reduction are:
Subset: 	in time, level and horizontal space
Average: 	in time, level and horizontal space
Proposed software solution for the Compute Node
In recent years, the work of some European ESGF partners has concentrated on the use of the DRKZ Birdhouse WPS framework and the deployment of a shared software stack at CEDA (UK), DKRZ (Germany) and IPSL (France). This stack, known as "roocs" (remote operations on climate simulations), is deployed on a single server, or batch cluster, located beside an ESGF Data Node. 
The aim of this approach is to enable any ESGF Node Manager to deploy a common Compute Node from a standard recipe. The "roocs" stack is also being used as the data source for the IS-ENES3 compute prototype, which employs the Climate4Impact portal as its frontend. The "roocs" Web Processing Service (WPS) is focused on "data-reduction" operations, beginning with subset and average.

The "roocs" solution is a strong candidate for the ESGF Compute Node because:
it is already deployed in production, for C3S, at three ESGF partner sites (CEDA, DRKZ, IPSL)
it is written in Python, which is a common language in the ESGF stack
it uses on the open-source Birdhouse framework which is built upon the PyWPS library
it can already be installed on a single machine or cluster using Ansible playbooks
it includes a client-library ("rooki") that hides the WPS interface (if preferred)


Quarterly meetings: Share and Discuss
Every third CWT meeting (i.e. quarterly), the theme of the meeting would be to share and discuss other solutions and technologies to provide compute capabilities. These meetings would provide an opportunity to:
Discuss alternative approaches used by members of the CWT
Discuss alternative approaches used by external organisations/projects (invited to specific meetings)
Capture new requirements
Discuss proposals for future developments
Include/merge with other relevant meetings: e.g. the quarterly Birdhouse meetings
Investigate other technologies/approaches: e.g. Cloud, Containers, Machine Learning, etc.
Communication and project planning
The new CWT will conduct itself (as far as possible) in an open manner. We propose using:
A new GitHub repository at: https://github.com/ESGF/esgf-cwt
for communication within, and about, the CWT
(existing) GitHub repositories for code - with agreed procedures for code review, pull requests and releases
GitHub issues to track issues
GitHub projects to manage and communicate the Roadmap
A GitHub wiki to record information about the CWT and minutes of meetings (such as that used by the Birdhouse group at: https://github.com/bird-house/bird-house.github.io/wiki/Meetings)


4. Roadmap:
5. Next steps:
   - Agree/publish our roadmap
   - add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
   - Fork github.com/ESGF/esgf.github.io/
     - commit updates, and create a PR for SA to merge
 
  Restart CWT Meetings
 Improve systems for monitoring/logging usage/problems (extending Dashboard)
 Deploy production CWT Node ("rook" WPS) on VMs at CEDA and DKRZ using Ansible recipes
 Document the installation process for the VM-based deployment
 Publicise the new service and plan user feedback/review
 Review by collaborators and users
 Respond to feedback with a new plan
 Engage with CWT partners on requirements for deploying on their nodes
 Develop Docker/Kubernetes/VM recipes as required
 
 Create realistic milestones in GitHub

## Notes
