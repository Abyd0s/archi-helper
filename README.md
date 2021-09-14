# Archi Helper
Fontosabb assembly utasítások, Dosboxban való programok futtatása.

## Jelek értelmezése az "ArchiHelper.txt" állományban:

|Jelölés|Mit jelent|Példa:|
|----|----|----|
|3 sor '#'|Nagyobb témák elválasztása.|-|
|1 sor '#'|Egy nagy témát több kisebb alrészre bont.|-|
|Szöveg/szám '*' között|Gyors elérésm témák száma, neve. Ezekre ha rákeresünk egyből az adott témához ugorhatunk.|\*6.5\* - \*shr\*|
|Egy sor '.'|Elválasztó jel, 2 ilyen sor között programkód található|-|
|{SZOVEG}|Behelyettesítendő szöveg|shr {MIT},{MENNYIVEL}|
|...|Nem lényeges kód sorok, ez akár több sort is reprezentálhat, de nem lényeges a bemutató szempontjából|...|

## Témák gyors elérése:
### Használata:
Az "ArchiHelper.txt" állományban keressünk rá az adott számú elem számára vagy nevére.

Pl.: Kíváncsiak vagyunk hogy hogyan néz ki a program váza: 
    keresés szövege: \*2\* vagy \*program váz\* vagy \*2\* - \*program váz\*

1. exe létrehozása
1. program váz
1. karakter kiíratás
1. szöveg kiíratás
1. műveletek
    1. mov
    1. add
    1. sub
    1. cmp
    1. jmp
    1. jz
    1. jnz
    1. jc
    1. jnc
    1. többi jump
1. bináris műveletek
    1. and
    1. or
    1. xor
    1. shl
    1. shr
    1. rol
    1. ror

## Dosboxban programok futtatása

1. Hozzunk létre egy mappát a számítógépünkön amiben majd a programunkat fogjuk elkészíteni, ebben a mappában előnyös ha benne van a **masm.exe** és a **link.exe**.
2. Hozzunk létre egy programot **.asm** kiterjesztéssel a mappában.
3. Nyissuk meg a Dosboxot.
4. írjuk be a következőt: **<code>mount c {mappánk elérési utvonala}</code>**
5. Váltsunk a felcsatolt mappába: **<code>C:</code>**
6. (Opcionális) Győződjünk meg hogy az adott filejaink a mappában vannak-e: **<code>dir</code>**
7. EXE létrehozása Dosboxban: **<code>masm.exe program.asm,,,,</code>** majd **<code>link.exe program.obj,,,,</code>**
8. EXE futtatása: **<code>program.exe</code>**

A megosztott mappában tudunk tovább dolgozni, **nem kell minden egyes mappában történő változtatás, fájl létrehozás után újra felcsatolni mount-al**!