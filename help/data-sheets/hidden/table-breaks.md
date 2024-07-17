---
title: Interruzioni di tabella
description: Verifica di interruzioni di tabella diverse
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# Interruzioni di tabella

Non c&#39;è molto da vedere.

## Tabella markdown standard con `<br>`

**CORRETTO`Green<br>Red<br>Blue`**

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Verde<br>Rosso<br>Blu |
| Maria | 23 | Giallo<br>Marrone |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Verde<br>Rosso<br>Blu |
| Maria | 23 | Giallo<br>Marrone |

{style="table-layout:auto"}

## Tabella Markdown con `<br>` doppi

**CORRETTO`Green<br><br>Red<br><br>Blue`**

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Verde<br><br>Rosso<br><br>Blu |
| Maria | 23 | Giallo<br><br>Marrone |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Verde<br><br>Rosso<br><br>Blu |
| Maria | 23 | Giallo<br><br>Marrone |

{style="table-layout:auto"}

## Tabella Markdown con `<p>`

**CORRETTO`Green<p>Red<p>Blue`**

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Verde<p>Rosso<p>Blu |
| Maria | 23 | Giallo<p>Marrone |

{style="table-layout:fixed"}

**AUTO`Green<p>Red<p>Blue`**

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Verde<p>Rosso<p>Blu |
| Maria | 23 | Giallo<p>Marrone |

{style="table-layout:auto"}

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Questo è il colore **verde** ed è destinato a racchiudere in una riga diversa come argomento e/o mezzo di verifica di tali interruzioni di paragrafo. <p>Questo è il colore **rosso** ed è destinato a racchiudere in un&#39;altra riga come argomento e/o mezzo di verifica delle interruzioni di paragrafo sopra indicate. <p>Questo è il colore **blu** ed è destinato a racchiudere in un&#39;altra riga come argomento e/o mezzo di verifica delle interruzioni di paragrafo sopra indicate. |
| Maria | 23 | Giallo<p>Marrone |

{style="table-layout:fixed"}

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Questo è il colore **verde** ed è destinato a racchiudere in una riga diversa come argomento e/o mezzo di verifica di tali interruzioni di paragrafo. <p>Questo è il colore **rosso** ed è destinato a racchiudere in un&#39;altra riga come argomento e/o mezzo di verifica delle interruzioni di paragrafo sopra indicate. <p>Questo è il colore **blu** ed è destinato a racchiudere in un&#39;altra riga come argomento e/o mezzo di verifica delle interruzioni di paragrafo sopra indicate. |
| Maria | 23 | Giallo<p>Marrone |

{style="table-layout:auto"}
