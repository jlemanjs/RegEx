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


\.expect\((\d*), done\)


75-93	.expect(401, done)
83-86	401

;\nexpect(response.status).toBe($1)

\);\n[\t ]*\n[\t ]*expect


## Replace for add auto fieldNames:
\$\{sv\}\."(\w*)"

${sv}."${StockViewFieldNames.$1}"


@ApiProperty([^\}]*)\}\)

Better version : 
@ApiProperty\(\{([^\}]|\n)*\}\)


## Found the last number collumn of a csv file

(,[0-9]*\n)

can be replace by

,1\n

for have 1 instead of existing value

## Replace in code

await queryRunner\.query\(`ALTER TABLE "([a-zA-Z_]*)" DROP COLUMN "([a-zA-Z_]*)"`\);

can be replaced by:
await this.convertDatesToDatesWithTimezone('$1', '$2', queryRunner);


await queryRunner\.query\(\W*`ALTER TABLE "([a-zA-Z_]*)" ADD "([a-zA-Z_]*)" [A-Z ()]*`\W*\);\n
Can be replace by nothing

## Replace xxx={1} by xxx="1"

([a-zA-Z]*)={([0-9]*)}

can be replace by

$1="$2"