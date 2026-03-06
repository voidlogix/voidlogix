# voidkit

> *A toolkit for the unrepresented in computation.*

---

## what is this

Most languages give you `null`, `undefined`, `NaN` — tokens that say *"something went wrong"* or *"nothing is here"*.

But they don't give you a vocabulary for **absence as a first-class concept**.

`voidkit` is a TypeScript toolkit that treats the unrepresented not as an error state, but as a **design primitive**.

---

## status

```
⬛ in design
```

Core primitives are being defined. The first release will focus on:

- `Void<T>` — a type that distinguishes *absence* from *null*
- `unrendered()` — marks values that exist in intent but not yet in form
- `preRuntime<T>` — typed placeholders for values that will exist at execution time
- `trace()` — logs what *didn't* happen, not just what did

---

## philosophy

```typescript
// null says: "nothing is here"
// Void says: "something should be here, and its absence is meaningful"

const value = Void.of<UserConfig>({
  reason: "not yet initialized",
  trace: "boot.sequence"
})
```

The goal is not to replace error handling — it is to make **intentional absence** legible to the type system, the runtime, and the developer.

---

## related

- [Conflux MCP Server](https://github.com/voidlogix/conflux-mcp) — the MCP server where these primitives are first applied
- [voidlogix.github.io](https://voidlogix.github.io) — the broader context

---

## license

MIT

---

```
// this space is intentionally unrendered.
// the rest is yours to define.
```
