---
title: Error del compilador C3911
ms.date: 11/04/2016
f1_keywords:
- C3911
helpviewer_keywords:
- C3911
ms.assetid: b786da59-0e99-479d-bc0d-551126e940f2
ms.openlocfilehash: 6c00a3bb388130d9a570e9fd731a9ed1200ed179
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50622188"
---
# <a name="compiler-error-c3911"></a>Error del compilador C3911

'event_accessor_method': función debe tener el tipo 'firma'

Método de descriptor de acceso de un evento no se declaró correctamente.

Para obtener más información, consulte [eventos](../../windows/event-cpp-component-extensions.md).

El ejemplo siguiente genera C3911:

```
// C3911.cpp
// compile with: /clr
using namespace System;
delegate void H(String^, int);

ref class X {
   event H^ E1 {
      void add() {}   // C3911
      // try the following line instead
      // void add(H ^ h) {}

      void remove(){}
      // try the following line instead
      // void remove(H ^ h) {}

      void raise(){}
      // try the following line instead
      // void raise(String ^ s, int i) {}
   };
};
```