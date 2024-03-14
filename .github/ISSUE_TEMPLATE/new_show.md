---
name: New Show
about: A new project/show needs to be created for pipeline and production.
title: NAME - Full Project Name
labels: show
assignees: ''

---

#### Info

- Name: Full Project Name
- ShotGrid: [ShotGrid - NAME](https://automatik-vfx.shotgunstudio.com/page/project_overview?project_id=ID)
- Location: `LONDON`|`BERLIN` `/mnt/projects/NAME`

#### Creation Tasks

- [x] Create ShotGrid project
- [ ] Create file system folder via AMI
- [ ] Create OCIO setup
- [ ] Create Delivery Packager setup
- [ ] Deploy OCIO and Delivery Packager configs studio-wide

#### Archiving Tasks

- [ ] Create plate and comp ProRes movies
- [ ] Create folder structure and copy Nuke scripts
- [ ] Archive on ShotGrid

#### Color setup
Base config.ocio: **ACES**|**linear**

```mermaid
  graph LR;
      A[ ACES2065-1 ]-->B[ ACEScct ] -->C{{ ShotLUT }} -->D{{ ProjectLUT }} --> E[ ACEScct ] -->F[ Rec709 ] ;
```

```mermaid
  graph LR;
      A[ linear ]-->B[ AlexaLogC ] -->C{{ ShotLUT }} -->D{{ ProjectLUT }} --> E[ AlexaLogC ] -->F[ Rec709 ] ;
```
