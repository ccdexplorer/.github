## README for usecases.json
In order to add/update usecase information, please create a pull request.

### Schema
The `usecases.json` file is a dictionary, where every entry is a new usecase.

```
class UseCase:
    usecase_id: str
    display_name: str
    url: Optional[str] = None
    description: Optional[str] = None
    logo_url: Optional[str] = None
    mainnet: Optional[list[UseCaseAddress]] = None
```

With addresses being defined as:

```
class UseCaseAddress:
    type: str  # account_address or contract_address
    account_index: Optional[int] = None  # only for account_address
    account_address: Optional[str] = None  # only for account_address
    contract_index: Optional[int] = None  # only for contract_address
    contract_address: Optional[str] = None  # only for contract_address
```

