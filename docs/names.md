---
title: Author Names
---

Providing an author name is straight-forward: just set the `name`
attribute. However, sometimes fine-grained control over the name
is required.

## Name parts

There are many ways to describe the parts of names; we support the
following:

- given names,
- surname,
- dropping particle,
- non-dropping particle,
- and suffix.

We use a heuristic to parse names into these components. This
parsing may produce the wrong result, in which case it is
necessary to provide the relevant parts explicitly.

The respective field names are

- `given` (aliases: `first`, `firstname`)
- `surname` (aliases: `family`)
- `dropping-particle`
- `non-dropping-particle`
- `suffix`

The full display name will be constructed from these parts, unless
the `name` attribute is given as well.

### Example

```yaml
authors:
  - given: Ludwig
    dropping-particle: van
    surname: Beethoven
    affiliation: '1'
    
  - given: Louis
    non-dropping-particle: de
    surname: Broglie
    affiliation: '2'
```