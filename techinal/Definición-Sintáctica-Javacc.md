[[_TOC_]]

## Jflex

En esta sección agregue prácticamente copy and paste de javacc y describí cada parte, pero no es lo solicitado.
Pero adjunto como en el markdown se puede agregar còdigo java y que reconozca la sintaxis para que visualmetne se vea bien.

``` java
Program PROGRAM() :
{Program toReturn; List<ASTNode> list;}
{
    try{
        list = STATEMENT_LIST() <EOF> { return new Program(new StatementBlock(list,0,0)); }
    }catch (ParseException e) {
          addError(e);
          return null;
    }

}
```
