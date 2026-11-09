# Roadmap

Where Cloud and Edge is heading: what is done, what is next, and what is only
an idea. Each step links to the decision behind it.

The code lives in two templates: d-lab-5/template-dlab5-cloud (the cloud and
its edge API) and d-lab-5/template-dlab5-edge (the Copier layer an edge is
made with). Their own ADRs hold the decisions; this site draws them.

## Now

- **The edge layer's chat remembers** (template-dlab5-edge, dlab5-edge-template
  1.1.0): waiting proposals survive a restart, outcomes are told back to
  Claude, the last ten conversations can be continued, and a page's selection
  is announced once. Ported from the Mediathek edge, which had them first.
- **Diagrams of how the two work together**, on this site.

## Next

- **Every edge on the layer.** Edges that hold hand-made copies of an early
  layer move onto it with Copier, so a fix reaches them with `copier update`.
- **Conformance profiles** for edge, cloud and shared repositories, read by
  `dlab5-repo-conformance`, and a recorded template version for a cloud
  (`.template.json`).

## Later

- A cloud made with Copier as well, so it takes the template's fixes the way
  an edge does. Its own decision first.
