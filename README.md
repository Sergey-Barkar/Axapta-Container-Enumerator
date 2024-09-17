# Container enumerator for Microsoft Dynamics AX

## Standard way to get a value from a container looks like:<br/>
```
container con = [1,2,'3'];
int       j,
          jMax = conLen(con);
;

for (j = 1; j <= jMax; j++)
{
    ... = conPeek(con, j);
}
```
## The container enumerator adds the new convenient way:
```
ConEnumerator enumerator = new ConEnumerator([1, 2, '3']);
;

while (enumerator.moveNext())
{
    ... = enumerator.current();
}
```
Exist one "but" - this new way have slow performance in compare with the standard one.
Use or not - up to you.
