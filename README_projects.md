## README for projects.json
In order to add/update usecase information, please create a pull request.

### Schema
The `projects.json` file is a dictionary, where every entry is a project.

```
class Project:
    project_id: str
    display_name: str
    url: Optional[str] = None
    description: Optional[str] = None
    logo_url: Optional[str] = None
    mainnet: Addresses
```

With addresses being defined as:


```
class Addresses:
    account_addresses: list[AccountAddress]
    contract_addresses: list[ContractAddress]

class AccountAddress:
    account_index: int
    account_address: str
    
class ContractAddress:
    contract_index: int
    contract_subindex: int

```

