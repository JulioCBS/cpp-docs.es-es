---
title: Error del compilador C2377
ms.date: 11/04/2016
f1_keywords:
- C2377
helpviewer_keywords:
- C2377
ms.assetid: f7660965-bf4c-4cd9-8307-1bd7016678a1
ms.openlocfilehash: b4789469fe27dafb2fb13bf3db085958db8d1478
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50528770"
---
# <a name="compiler-error-c2377"></a>Error del compilador C2377

'identifier': nueva definición; typedef no se puede sobrecargar con ningún otro símbolo

Se redefinió un identificador `typedef` .

El ejemplo siguiente genera la advertencia C2377:

```
// C2377.cpp
// compile with: /c
typedef int i;
int i;   // C2377
int j;   // OK
```