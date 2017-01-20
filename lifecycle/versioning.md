# Versioning

```
v1.0.4
 ^ ^ ^ Patch
 | ' Minor
 ' Major
```

A release is made every sprint, and every release is marked with a *version number*. Sprints are named according to their version numbers, as well. This version number is in the format `MAJOR.MINOR.PATCH`.

## Naming sprints and milestones

- The first sprint is always `v0.1`.
- The next sprint will increase the *minor* number, such as `v0.2`.
- At the end of a milestone, the *major* number will be increased, such as `v1.0`.

## Naming releases

The first official release of a sprint will be named after the sprint, such as `v0.1.0`. In practice, you may need to make minor patch releases after that, in which case it'll increase the *patch* number, such as `v0.1.1`.

## Example schedule

> #### Milestone v1
>
> - `v0.1`
> - `v0.2`
> - `v0.3`
> - `v1.0`
>
> #### Milestone v2
>
> - `v1.1`
> - `v1.2`
> - `v2.0`

<details>
<summary>See also...</summary>

<p>This scheme is based on <a href='http://semver.org/'>Semantic Versioning</a>, more commontly known as Semver.</p>
</details>

> **Next:** Every version needs [release notes](release_notes.md).
