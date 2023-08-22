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


## Rechercher un bout de code similaire à 

curr.id !== row.id &&
          curr.productReference === row.productReference &&
          (!curr.batchId || curr.batchId === row.batchId)

\s*\w*[.]id\s*!==\s*\w*.id\s*&&\s*\w*.\w*eference\s*===\s*\w*.\w*eference\s*&&\s*\(!\w*.batchId\s*\|\|\s*\w*.batchId\s*===\s*\w*.batchId\s*\)

## Recherche SELECT content 

SELECT(((?!FROM).)*)FROM

/SELECT(((?!FROM).)*)FROM/gm


\)\s*\.end.*\W*try \{


8-62	)
        .end((error, response) => {
          try {

done\(\);\W*catch \(expectError\)\W*done\(expectError\);\s*\}\s*\}\);


229-325	done();
          } catch (expectError) {
            done(expectError);
          }
        });