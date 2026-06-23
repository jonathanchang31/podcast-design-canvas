# Speaker Role Mapping

Speaker roles should make imported tracks behave predictably across presets, canvas layouts, captions, and templates.

## User Goal

A creator should be able to map each imported track to a clear podcast role, then trust the product to place and label each speaker correctly throughout the episode.

## Relationship To Episode Setup

Speaker role mapping should stay connected to the creator-facing workflow that already uses those roles:

- imported speaker buckets from `docs/episode-ingest-readiness.md`
- preset preview and first-look layout decisions from `docs/preset-style-picker.md`
- speaker labels in captions from `docs/speaker-attribution-review.md`
- reusable role behavior in future episodes from `docs/show-template-adaptation.md`

Role confirmation should happen before presets, captions, or template adaptation depend on the wrong speaker identity. This keeps role mapping inside episode setup instead of turning it into a detached track-management screen.

## Core Roles

Use simple role options:

- host
- co-host
- guest
- panelist
- producer or off-camera voice
- narrator or voiceover

Roles should remain editable after ingest. Changing a role should update layouts, lower-thirds, captions, and template adaptation previews where appropriate.

## Role Signals

The product can suggest roles from:

- file names
- speaker names
- Riverside track labels
- social links
- transcript introductions
- recurring show template settings

Suggestions should be reversible and visible. Do not silently assign a guest as a host just because they speak first.

## Layout Effects

Roles should influence:

- default frame prominence
- lower-third priority
- caption attribution
- title card wording
- b-roll and callout placement
- host-only or guest-only visual treatments

The product should avoid treating every speaker equally when the show format clearly has a host-led structure.

Role-based layout issues that would affect the chosen export destination should surface in `docs/export-readiness-review.md` Speaker Framing Warnings.

## Edge Cases

Support common podcast setups:

- solo host
- two-person interview
- rotating co-hosts
- panel episodes
- producer voice without camera
- guest joins late or leaves early

## Review And Confirm

Before styling starts, the creator should be able to confirm every track's role at a glance and fix the ones that look wrong without restarting ingest.

Each track should show a clear role state:

- confirmed — the creator has accepted the role
- suggested — the product proposed a role with visible reasoning
- needs review — low-confidence or conflicting signals
- unassigned — no role chosen yet

Keep the corrections direct:

- accept a suggested role in one action
- change a role from the short list of podcast roles
- swap two speakers' roles when tracks were mixed up
- mark a track as off-camera or voiceover
- set a guest who joins late or leaves early without breaking the layout
- reset a track to its suggested role

Confirming a role should update that speaker's framing, lower-third, and caption attribution in the live preview, so the creator sees the result before moving on. A track should never be silently locked into a role the creator has not seen.

## Maintainer Acceptance Notes

Accept work that makes speaker roles durable across ingest, presets, canvas editing, captions, and templates. Close work that treats tracks as anonymous media files or hard-codes one show format for every podcast.
