---
title: Advertencia del compilador (nivel 4) C4019
ms.date: 11/04/2016
f1_keywords:
- C4019
helpviewer_keywords:
- C4019
ms.assetid: 4ecfe85d-673f-4334-8154-36fe7f0b3444
ms.openlocfilehash: d2bfec799b8b2981914b76839e51b7a0d09b30ee
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50465382"
---
# <a name="compiler-warning-level-4-c4019"></a>Advertencia del compilador (nivel 4) C4019

instrucción vacía en ámbito global

Un punto y coma en el ámbito global no está precedido por una instrucción.

Esta advertencia se puede corregir si se quita el punto y coma adicional.

## <a name="example"></a>Ejemplo

```
// C4019.c
// compile with: /Za /W4
#define declint( varname ) int varname;
declint( a );   // C4019, int a;;
declint( b )   // OK, int b;

int main()
{
}
```