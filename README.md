# base-unit-trait-amphibious

The `Amphibious` unit trait: a unit type with it can attack from a ship.

A unit type with this trait may attack a land tile directly from the ship carrying it.

For example: Civ2: flag 2 (Marines).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Amphibious)`:

```ts
import Amphibious from '@civ-clone/base-unit-trait-amphibious/Amphibious';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Amphibious));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
