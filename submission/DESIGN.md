<!-- For my own reference: https://discordapp.com/channels/772968587060445244/772968587060445251/813166983364739095 -->
# Kitties Pallet Design

This is a design document submitted for substrate developer academy assignment 4 (Kitties Pallet)

## Storage (decl_storage!)

    * kitties: double_map (kitty_dna: u128, owner: AccountId )  => kitty_id:u32
<!-- types look like TS, not RUST but made it to convey better -->

## Events (decl_event!)

    * KittyTransferred(AccountId, AccountId, u128),
<!-- [from, to, kitty_id] -->

## Errors (decl_error!)

    * NotTheOwnerOfKitty,

## Calls (decl_module!)

    * fn trasnsfer(origin, kitty_id: u32, to: AccountId)
