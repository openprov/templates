
# An Open Community Repository for Provenance Templates

PROV-TEMPLATE is a declarative approach that enables designers and
programmers to design and generate provenance compatible with the PROV
standard of the World Wide Web Consortium. Designers specify the
topology of the provenance to be generated by composing templates,
which are provenance graphs containing variables, acting as
placeholders for values.  Programmers write programs that log values
and package them up in sets of bindings, a data structure associating
variables and values. An expansion algorithm generates instantiated
provenance from templates and sets of bindings in any of the
serialisation formats supported by PROV.

PROV-TEMPLATE is described in *Luc Moreau, Belfrit Victor Batlajery,
Trung Dong Huynh, Danius Michaelides, and Heather Packer. A templating
system to generate provenance. IEEE Transactions on Software
Engineering, April 2017* [(doi:10.1109/TSE.2017.2659745)](http://dx.doi.org/10.1109/TSE.2017.2659745).

## 1. Governance of the Repository

This repository contains free provenance templates allowing best
practice provenance to be shared and reused in any application.  We
invite the community to contribute templates to this repository.  To
ensure reusability and most reliable generation of provenance from
this repository, we adopt the following principles.


### 1.1 An Open Repository

 * Provenance templates are stored in a public persistent github repository, clonable by anybody.
 * Templates are expected to be accompanied with bindings illustrating their use.
 * Templates and bindings contributed to the repository are expected to be available under creative common licence (CC-BY).  This is the most accommodating of licenses offered; it is recommended for maximum dissemination and use of licensed materials.

### 1.2 A Stable Repository
 
 * The structure of the repository mandates versions of templates to be explicit, ensuring template identifiers remain persistent over time.  By adopting the "COOL URI" principle, we facilitate imaginative forms of provenance storage and processing to be conceived, in which template and bindings are managed separately where approapriate.



## 2. Repository Structure

The repository structure is as follows.

All templates for an application are stored in a single folder for that application. To avoid conflicts of names, we use the reverse Internet domain name to create a hierarchy structure in which this folder appears.  In the example below, `example.com` is the domain name to create the directory structure `/com/example/`, in which we can find application `application1`.

```

/com/example/application1/footemplate/1.provn
/com/example/application1/footemplate/1/example1.json
/com/example/application1/footemplate/1/another_example.json
/com/example/application1/footemplate/2.trig
/com/example/application1/footemplate/2/example.json

# optionally:
/com/example/application1/footemplate/1.png
/com/example/application1/footemplate/2.png
/com/example/application1/footemplate/README.md

```

All the versions of a template are stored in a folder whose name is that of the template.  In this example, we find two versions in the folder `footemplate`: `1.provn` and `2.trig`.  Versions are simply named by their number and are allowed to use any PROV recognised serialization.

Whenever there is a template `1.provn`, the folder `1/` at the same level contains examples of bindings. Any name can be used for the bindings examples: `example1.json` and `another_example.json` in this instance. Both are using the JSON serialisation of bindings.

All folders and file names must consist of lower cases, digits and special characters(`-` and `_`).  White spaces are not allowed. The purpose of these restrictions is to facilitate the mapping to URLs as discussed in the next section.

Optionally, in the `footemplate` folder, we can also find png visualisations of the templates, and a `README.md` file containing a textual description (and potentially reference to the visual repesentations) of the templates.

## 3. Template Expansion Microservice

For convenience, we will aim to expose templates directly through openprovenance at 
https://openprovenance.org/templates/




