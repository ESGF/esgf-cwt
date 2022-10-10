# ESGF Compute Working Team Meeting - 2022-10-10

## Logistics

Where: Zoom

When:  10/10/2022

Who:   ESGF CWT:
   - Carsten Ehbrecht (DKRZ)
   - Ag Stephens (CEDA)
   - Paola Nassisi (CMCC)
   - Sasha Ames (LLNL)
   - Stephan Kindermann (DKRZ)
   - David Huard (Ouranos)
   - Steve Petruzza (Uni of Utah)
   - Alessandro Spinuso (KNMI)
   - Rob Jacob (Argonne National Lab, ANL)

## Actions

- [ ] AS: Report recommencement of CWT meetings to ESGF XC
- [ ] AS: Publish and share meeting minutes
- [x] AS: Draft a roadmap - including DH comment about short and longer-term roadmaps
   - https://github.com/ESGF/esgf-cwt/issues/5 
- [ ] AS: Draft terms of reference
   - https://github.com/ESGF/esgf-cwt/issues/6 

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
       - Include/merge with other relevant meetings: e.g. maybe the quarterly Birdhouse meetings
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
   - Improve systems for monitoring/logging usage/problems (extending roocs dashboard)
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
9. AOB:
   - Next meeting: 10/10/2022
 
# Notes

1. Welcome and introductions
   - the team introduced themselves and their roles/interest
2. CWT Logistics (see above)
3. CWT plan (see above)
4. Technologies and focus (see above)
5. Code management (see above)
6. Roadmap (proposed) (see above)
7. Discussion and questions:
   - **Moving a single solution for the ESGF Compute Node:**
     - DH: I am happy with this approach. Are there suitable entry points for others to contribute to the codebase?
       - AS: Yes, we can separate the work into strands such as: (1) deployment/operations, (2) enhancements to the tests, (3) new functionality, (4) connecting to new datasets/projects.
     - SA: In principle, it would not a problem to adopt the proposed codebase as long as it meets the requirements of ESGF2
   - **Use of GitHub versus Google Docs:**
     - SA: Google Docs is used in many ESGF groups. Is there a reason to avoid it?
     - AS: For static versions of meeting minutes and some documents, GitHub is a good option because it records the history as fixed versions. However, we may want to use Google Docs in some instances when a more collaborative approach is required. I propose we use the best tools for the job as necessary.
   - **roocs system for applying "fixes" on-the-fly**:
     - DH: The "roocs" code includes the `daops` library which has the capability to record, and apply, _fixes_ to ESGF datasets. Is that part of the plan for the CWT work?
       - AS: Whilst we developed the capability for on-the-fly "fixes" in the C3S-funded work, we did not generate many actual fixes. The default position for the CWT work will be to **run roocs with the fixing functionality switched OFF.** We can review this within the CWT and decide if it should be reconsidered, or implemented in a different way.
       - SA: we should also feed back to the WGCM about making the data standards precise/complete enough so that data doesn't require fixing.
   - **Roadmap**:
     - DH: I suggest having two roadmaps, one for short-term deployment, and one for longer-term development.
       - AS: That makes good sense, we will consider that when drafting a Roadmap.
8. Next steps (see above)
9. AOB (see above)
