---
---

# find_champion

Given the name of a champion, returns a dictionary containing the `name`, `role`, and `origin` of the champion.

## Usage
-	find_champion(`<champ_name>`)
## Parameters
- `<champ_name>`  - string, required.
  
The name of the champion.
## Response
- [{'name': `<champ_name>`, 'role': `<champ_role>`, 'origin': `<champ_origin>`}

If the parameter is anything other than a single valid champion name, the function will return either an empty list, or a list of all the dictionaries of the champions.


## Code
   
   

    champion_data = [
      {
        'name': 'ahri',
        'role':  'mid lane',
        'origin': 'vastaya'
      },
      {
        'name': 'teemo',
        'role': 'top lane',
        'origin': 'bandle city'
      },
      {
        'name':'gangplank',
        'role': 'top lane',
        'origin': 'bilgewater'
      },
      {
        'name': 'sona',
        'role': 'support',
        'origin': 'ionia'
      },
      {
        'name': 'miss fortune',
        'role': 'marksman',
        origin': 'bilgewater'
      }
]


        def find_champion(name=None, role=None, origin=None):
         champion_suggestions = []
         for champ in champion_data:
           if name:
             if champ['name'] == name:
               return [champ]
           if role:
             if champ['role'] != role:
               continue
           if origin:
             if champ['origin'] != origin:
               continue
           champion_suggestions.append(champ)
         return champion_suggestions
