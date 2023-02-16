# RegEx
## Rechercher toutes les chaînes sans param protégés sql
`([\S\s])*(\s)*[=<>]+(\s)*[^:]

## Rechercher tous les endroits où il manque un await pour une fonction donnée
^[^=]*[=]+\s*((?!await).)*cleanTemplateData\S*$

## Rechercher les messages traduits avec arguments
MESSAGES.[0-9A-Z._]*,\W*\{

## Recherche et remplace regex
^([0-9A-z ]*,){4}
$0non,

^(((?!\+ADs-).)*\+ADs-){4}
$0non+ADs-

## Recherche de "lot" ou "lots" dans des strings
["'`].*\slot[s|^s]*\s


              '<td style=\\"padding: 8px 16px; text-align: left; border-bottom: 1px solid #153843; overflow-wrap: break-word;\\">\\s*001BatchTest342\\s*</td>',


              '<td style=\\"padding: 8px 16px; text-align: left; border-bottom: 1px solid #153843; overflow-wrap: break-word;\\">\\s*Product C\\s*</td>\\s*<td style=\\"padding: 8px 16px; text-align: left; border-bottom: 1px solid #153843; overflow-wrap: break-word;\\">\\s*</td>',


color: #f4664f">((?!<\/tr))*Product((?!<\/tr))*<\/tr