---
title: Error del compilador C2462
ms.date: 11/04/2016
f1_keywords:
- C2462
helpviewer_keywords:
- C2462
ms.assetid: a8601bf8-f5ce-41de-9117-e2632bd4996b
ms.openlocfilehash: 0b342f8b878c48a77336fab4921cf4a668e248ab
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50607059"
---
# <a name="compiler-error-c2462"></a>Error del compilador C2462

'identifier': no se puede definir un tipo en una expresión' new'

No se puede definir un tipo en el campo de operando la `new` operador. Coloque la definición de tipo en una instrucción independiente.

El ejemplo siguiente genera C2462:

```
// C2462.cpp
int main() {
   new struct S { int i; };   // C2462
}
```