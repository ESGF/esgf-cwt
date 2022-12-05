# ESGF Compute Working Team Meeting - 2022-10-10

## Logistics

Where: Zoom

When:  10/10/2022

Who:   ESGF CWT:
   - Carsten Ehbrecht (DKRZ)
   - Ag Stephens (CEDA)
   - Sasha Ames (LLNL)
   - Katharina Berger (DKRZ)
   - David Huard (Ouranos)

## Actions

- [ ] AS: Report recommencement of CWT meetings to ESGF XC
- [x] AS: Publish and share meeting minutes
- [ ] AS: Share the roadmap with the XC and Slack team - https://github.com/ESGF/esgf-cwt/issues/5
- [ ] AS/CE: Draft the Terms of Reference then share: - https://github.com/ESGF/esgf-cwt/issues/6

## Agenda

1. Welcome and introductions
2. Actions and minutes from last meeting
- [ ] AS: Report recommencement of CWT meetings to ESGF XC - ongoing
- [x] AS: Publish and share meeting minutes - shared on Slack
- [x] AS: Draft a roadmap: see https://github.com/ESGF/esgf-cwt/issues/5 
- [x] AS: Draft terms of reference: see 
   - https://github.com/ESGF/esgf-cwt/issues/6 

3. Roadmap:
- the team reviewed the Roadmap, at: https://github.com/ESGF/esgf-cwt/issues/5

Notes:
- DH: is the Compute Node dependent on other ESGF Services?
  - AS: not it only requires that ESGF data is visible on the local POSIX file system.
- DH: is it easy to install the new (dockerised) ESGF Data Node?
  - AS: we have created Ansible playbooks to set it up and we are supporting partners with the installation.
        So it is certainly easier than in the past.
- DH: We should include "spatial averaging over polygons" in the additional features section.  
- SA: Scott has made some suggestions of alternative approaches (as part of ESGF2) - to be shared with this group (for next meeting?).

4. Discussion and questions

5. Current Team Efforts:

- [ ] AS: Add "Current Team Efforts" to the agenda template.
  - a place for existing issues/discussion and farming out the work

AS: Yes, we can separate the work into strands such as: (1) deployment/operations, (2) enhancements to the tests, (3) new functionality, (4) connecting to new datasets/projects.

5. Next steps:
   - start implementing the Roadmap
   - add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
   - Fork github.com/ESGF/esgf.github.io/
     - commit updates, and create a PR for SA to merge
   - Can rewrite the entire CWT/Compute section.
   - DH: can review drafts (or draft)

6. AOB:
   - Next meeting:
     - Date: 14/11/2022
     - **FOCUS: Wider "share and discuss" meeting to discuss technologies, projects etc.**
 
# Notes

1. Welcome and introductions
   - the team introduced themselves and their roles/interest

