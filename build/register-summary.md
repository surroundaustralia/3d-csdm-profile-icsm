# Implementation Profiles for 3D CSDM

This repository contains the 
 ICSM - [ANZLIC](https://www.anzlic.gov.au/) [Intergovernmental Committee on Survey and Mapping](https://www.icsm.gov.au/) - [Common  profile](bblock/icsm.profiles.common) of the [Cadastral Survey Data Model Exchange Specification](https://icsm-au.github.io/3d-csdm-common/). 
 
 _The ICSM profile is a partial set of constraints, the full model is implemented by a further set of jurisdiction specific profiles using local vocabulary (codelists) and any additional content and rules necessary._
 
Profiles are defined in a consistent, machine-readable and validatable way using the [OGC Building Blocks methodology](https://ogcincubator.github.io/bblocks-docs/).


Each jurisdiction profile extends a [common ICSM profile] of a general [model of 3D cadastre](https://icsm-au.github.io/3d-csdm-model/), and an [encoding specification in form of a JSON schema](https://icsm-au.github.io/3d-csdm-common/).

The encoding specification and all profiles are compatible with the [OGC API Features](https://opengeospatial.github.io/e-learning/ogcapi-features/text/basic-main.html) data exchange specification, and can thus be implemented by any standards compliant software capable of handling nested object sub-schemas and control of codelist in content.

The relationships of this profile to specific jurisdictional profiles and and the underlying  common model are shown below:

![](https://lucid.app/publicSegments/view/f7e6c029-db67-4186-9592-cab6ec3437d0/image.png)


## Building Blocks

### `icsm.profiles.datatypes.address` — ICSM Address (Placeholder)

**Type:** schema

A simple implementation of ICSM address model. Can be mapped to or replaced by a standard ICSM schema when available.

### `icsm.profiles.icsm-2d` — Cadastral Survey 2D (+elevation) basic Profile

**Type:** schema

Profile to constrain a 2D implementation of the 3D Cadastre Survey Data Model

### `icsm.profiles.icsm-3d` — Cadastral Survey 3D profile

**Type:** schema

2d and 3D objects allowed, observations  and coords must be 3d.  Note that validation rules for 3D have not been elucidated pending future phases of development and testing.

### `icsm.profiles.common` — Cadastral Survey Common ICSM Profile

**Type:** schema

Common profile of the Cadastral Survey Data Model. All ICSM jurisdiction profiles will inherit schemas, rules and vocabulary bindings from this profile, ensuring consistency and minimising effort and complexity of jurisdictional profile specification.

