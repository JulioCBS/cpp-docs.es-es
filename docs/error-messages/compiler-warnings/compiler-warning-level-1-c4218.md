---
title: Advertencia del compilador (nivel 1) C4218
ms.date: 11/04/2016
f1_keywords:
- C4218
helpviewer_keywords:
- C4218
ms.assetid: d6c3cd90-4518-49e9-ae86-4ba9e2761d98
ms.openlocfilehash: 36d5de3b1270b41edfc391df960a556aca207709
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50555303"
---
# <a name="compiler-warning-level-1-c4218"></a>Advertencia del compilador (nivel 1) C4218

extensión no estándar utilizada: debe especificar al menos una clase de almacenamiento o un tipo

Con las extensiones de Microsoft (/Ze), puede declarar una variable sin especificar una clase de almacenamiento o tipo. El tipo predeterminado es `int`.

## <a name="example"></a>Ejemplo

```
// C4218.c
// compile with: /W4
i;  // C4218

int main()
{
}
```

Estas declaraciones no son válidas en la compatibilidad con ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).