# Magic: the Gathering draft scoring

## Winchester Draft

- 1/n points for picking a card
- 1 point / color in your picked cards (maybe for best two colors only?)
- negative points for skipped cards? 1 or 1/n?

Calculate value of the stacks for AI and human, take the one with biggest
combined value (with a factor controlling the amount of hate drafting).

## Grid Draft

Similar scoring, but I guess always 1 point for picking a card is enough.
Negative point if neither player picks the card.

For color matching, also notice the mana symbols in card text to account
for mana fixing.

- 18 packs with 9 cards each.
- Four-color grid draft: 16 packs


## Data structure

- Cube
	- List of cards in the cube
		- Name
		- Drafting value
	- Drafts
		- Draft status: active | finished
		- Draft set (list of card names)
		- Player A picks
			- Deck
			- Sideboard
		- Player B picks
			- Deck
			- Sideboard
		- Point values for the drafted cards
		- Log of picks

When a draft is finished, the point values are merged with the overall cube
values.