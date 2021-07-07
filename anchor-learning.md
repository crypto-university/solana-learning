## Anchor Learning

### Storing String

We can store a string in an associated account, 

Please note below that DataAccount is an associated account and in order to put an associated account, we need `system_program`

```rs
use anchor_lang::prelude::*;

#[program]
mod basic_1 {
    use super::*;

    pub fn initialize(ctx: Context<Initialize>, data: String) -> ProgramResult {
        let data_account = &mut ctx.accounts.data_account;
        data_account.data = data;
        Ok(())
    }
}

#[derive(Accounts)]
pub struct Initialize<'info> {
    #[account(init, associated = my_account, space = 112)]
    data_account: ProgramAccount<'info, DataAccount>,
    #[account(signer)]
    my_account: AccountInfo<'info>,
    rent: Sysvar<'info, Rent>,
    system_program: AccountInfo<'info>,
}

#[associated]
pub struct DataAccount {
    pub data: String,
}
```
