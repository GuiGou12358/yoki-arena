# yoki-arena

From misty temples to blazing dojos, each arena has its own properties and influences. Exploit affinities, anticipate synergies, and let your creatures fully unleash their power in dynamic battles.

As you accumulate victories, you grow as an onmyoji — earning titles, climbing ranks, and unlocking recognition on-chain. Your Yoki themselves evolve through **fusion**: combine two Yoki of the same element and level to forge a more powerful one at the next tier.

Battles are entirely simulated by advanced **artificial intelligence**. The AI does not treat both sides equally: it accounts for the raw power of your Yoki, the bonuses granted by your equipment, but also your accumulated experience as an onmyoji and your tactical knowledge of the spirits and artifacts you have encountered. The deeper your mastery, the sharper your edge. Every action and result is **transparent, traceable, and secured via blockchain**: you remain the true owner of your Yoki and their equipment.

Dive into an experience where collection, strategy, and competition converge in a rich visual universe inspired by Japanese manga aesthetics.

## World Regions

The onmyoji travels across different regions of the world, each with arenas, Yoki, and items tied to a specific visual and cultural identity:

- Asia *(available)*
- Europa *(coming later)*
- Latin America *(coming later)*

In each region, the onmyoji can:

- mint new Yoki specific to that region
- mint additional items that can be equipped to Yoki and used in battles
- fuse two Yoki of the same element and level to obtain a stronger one
- register their Yoki for combat

All NFTs are region-specific.

## Tournament System

Battles in the arena are organized as tournaments.

- Format: `1v1`, `2v2`, `3v3`
- Winners advance round after round until the final
- Equipment attached to a Yoki remains active for the entire duration of a tournament
- Equipment can only be used in a single tournament at a time
- Yoki and equipment are held in on-chain custody by the Arena during the tournament

## Yoki Core Design

Each Yoki type is defined by:

- one elemental type: `WATER`, `FIRE`, `AIR`, `NATURE`, `SHADOW`, `LIGHT`
- a `level`: `0, 1, 2, 3, 4, 5` *(configurable maximum)*
- a specific home region

All Yoki of the same element and level are identical — same stats, same token ID.

Yoki evolves through **fusion**: burn two Yoki of identical element and level to receive one Yoki of the same element at the next level.

### Primary Attributes

- `atk`: Attack, damage output
- `def`: Defense, damage reduction
- `spd`: Speed, action order and dodge impact
- `spirit`: Spiritual Power, used for special and magical abilities

### Secondary Attributes

- `critChance`: critical hit probability
- `critDamage`: critical hit multiplier
- `accuracy`: hit chance versus evasion
- `evasion`: dodge chance
- `energy`: resource used for skills

## Arenas

Each arena has its own eligibility rules:
- Allowed Yoki contracts (by address)
- Allowed equipment contracts (by address)
- Allowed element types (optional filter)
- Level range (optional filter)
- Maximum equipment items per Yoki (configurable)

### Asia

- **Sacred Mist Sanctuary**: A sacred temple hidden within drifting mists, where spirits blur the line between illusion and reality. Only the most perceptive onmyoji can read the battlefield.
- **Eternal Flame Dojo**: An ancient dojo engulfed in eternal fire, where every clash ignites the air. Strength and timing decide who emerges from the flames.
- **Whispering Falls Garden**: A tranquil sanctuary of flowing water and living nature, where gentle currents conceal powerful forces waiting to be unleashed.

### Europa *(coming later)*

- **Celestial Citadel**: A majestic castle rising above the clouds, where ancient magic flows through its walls.
- **Emerald Grove Sanctuary**: A sacred forest bathed in eternal twilight, where nature spirits silently watch every move.
- **Frostveil Cathedral**: A forgotten cathedral frozen in time, covered in ice and sacred runes.

### Latin America *(coming later)*

- **Sunfire Pyramid**: An ancient pyramid bathed in golden sunlight, where forgotten rituals still echo.
- **Verdant Spirit Jungle**: A lush, living jungle filled with hidden spirits and vibrant energy.
- **Temple of Tidal Echoes**: A sacred coastal temple where waves crash in rhythmic pulses.

## Onmyoji Mastery & Player Identity

Every onmyoji carries a **Soulbound Token (SBT)** — a non-transferable, on-chain identity that grows with them throughout their journey. This permanent record cannot be sold or transferred: it is proof of who you are as a player.

### Experience Points

Every meaningful action earns **XP**, stored directly on the SBT:

| Action | XP earned |
|---|---|
| Mint a Yoki | +1 XP |
| Mint an equipment item | +1 XP |
| Fuse two Yoki | +1 XP |
| Survive a tournament round | +100 XP per round reached |

XP accumulates over time and reflects the depth of engagement with the game world. The tournament champion earns the most: every round survived compounds their experience.

### Knowledge Base

Each time a Yoki or equipment item is minted, that discovery is permanently recorded on-chain in the player's **Knowledge Base**. Fusing two Yoki also adds the resulting Yoki to the player's knowledge. This record spans every spirit and artifact the onmyoji has ever owned.

The Knowledge Base is not merely cosmetic — it directly influences how the AI combat engine evaluates the player's tactical mastery.

### AI-Driven Combat & Tactical Advantage

Battles are fully simulated off-chain by an advanced AI agent. The engine does not treat both sides equally. For each match it evaluates:

- **Yoki stats** — element type, level, and all base attributes (ATK, DEF, SPD, SPIRIT, CRIT CHANCE, CRIT DMG, ACCURACY, EVASION, ENERGY)
- **Equipment bonuses** — base stat bonuses, plus element affinities and arena affinities that activate when conditions are met
- **Player experience** — accumulated XP and tournament history stored on the SBT; a seasoned onmyoji commands their Yoki with greater precision
- **Knowledge advantage** — the AI cross-references each player's Knowledge Base against the opponent's Yoki and equipment; a player who has previously owned the opponent's Yoki understands its patterns and weaknesses; a player facing an unknown Yoki must adapt in real time and operates with less tactical clarity

This system rewards deep engagement: the more you explore, mint, fuse, and compete, the richer your tactical profile — and the more effectively the AI can simulate your onmyoji's mastery.

### On-Chain Player Record

The SBT also tracks milestone statistics and badges:

- **Tournament stats**: number of tournaments played, top-8 finishes, championships won
- **Badges**: Yoki Origins veteran, Yoki Legacy veteran, Genesis player status
- **Rank and titles**: updated by the backend as the player progresses through seasons

## Fee and Rewards

- Minting fees can be configured for each season, using either ETH or any ERC20 token.
- Arena entry fees contribute to a shared prize pool used to reward the winners.
- Each tournament can be sponsored to offer more attractive rewards.

## Existing NFT integration

Any existing NFT could potentially become either a fighter or an item of equipment. The possibilities are endless!

## Link
- **Presentation video** : https://youtu.be/IkLeJocfBpw
- **dApp on testnet** : https://yoki-battle-ui.vercel.app/

Git repositories *(private for the time being)*:
- **Smart contracts** : https://github.com/GuiGou12358/yoki-battle-contracts-v2
- **UI** : https://github.com/GuiGou12358/yoki-battle-ui
- **Worker** : https://github.com/GuiGou12358/yoki-battle-worker