# two-novelists

A two-author relay short story. Two novelists write parallel POV
threads (Ada and Bram) that converge by the end of chapter 2. A
worldbuilder maintains canon in a shared vector memory.

## Layout

- `CANON.md` — facts the worldbuilder declares binding (one per line,
  prefixed `FACT:` or `RULING:`)
- `chapters/` — POV files (`ch{N}-{ada|bram}.md`)

## Rules

1. Novelists must call `recall_memories(agent_id="two-novelists-canon")`
   before writing and treat results as binding.
2. Any new world fact a novelist invents must be both `store_memory`'d
   under the same agent_id AND `send_message`'d to the sibling novelist.
3. Contradictions are resolved by the worldbuilder between chapters,
   never by either novelist unilaterally.
