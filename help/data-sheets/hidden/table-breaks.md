---
title: Interruzioni di tabella
description: Verifica di interruzioni di tabella diverse
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# Interruzioni di tabella

## Tabella markdown standard con `<br>`

**FISSO`Green<br>Red<br>Blue`**

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

## Tabella Markdown con doppio `<br>`s

**FISSO`Green<br><br>Red<br><br>Blue`**

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

**FISSO`Green<p>Red<p>Blue`**

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
| Juanya | 17 | Questo è il colore **verde** ed è destinato a racchiudere in una riga diversa come materia e/o mezzo di prova le suddette interruzioni di paragrafo. <p>Questo è il colore **rosso** ed è destinato a racchiudere in una riga diversa come materia e/o mezzo di prova le suddette interruzioni di paragrafo. <p>Questo è il colore **blu** ed è destinato a racchiudere in una riga diversa come materia e/o mezzo di prova le suddette interruzioni di paragrafo. |
| Maria | 23 | Giallo<p>Marrone |

{style="table-layout:fixed"}

|  | Numero | Colori |
|---|---|---|
| Juanya | 17 | Questo è il colore **verde** ed è destinato a racchiudere in una riga diversa come materia e/o mezzo di prova le suddette interruzioni di paragrafo. <p>Questo è il colore **rosso** ed è destinato a racchiudere in una riga diversa come materia e/o mezzo di prova le suddette interruzioni di paragrafo. <p>Questo è il colore **blu** ed è destinato a racchiudere in una riga diversa come materia e/o mezzo di prova le suddette interruzioni di paragrafo. |
| Maria | 23 | Giallo<p>Marrone |

{style="table-layout:auto"}
