---
title: Error del compilador C3070
ms.date: 11/04/2016
f1_keywords:
- C3070
helpviewer_keywords:
- C3070
ms.assetid: ac88584d-40a6-4176-90f3-2371c3c935f2
ms.openlocfilehash: 7e1175fc1289a2504795a9d19bcd6274462b7a84
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50677843"
---
# <a name="compiler-error-c3070"></a>Error del compilador C3070

'property': la propiedad no tiene un método 'set'

No se definió el método de descriptor de acceso set de una propiedad. Para obtener más información, consulta [property](../../windows/property-cpp-component-extensions.md).

El ejemplo siguiente genera la advertencia C3070:

```
// C3070.cpp
// compile with: /clr
ref class R {
public:
   R(int size) {
      m_data = gcnew array<int>(size);
   }

   property int % MyProp[int] {
      int% get(int index) {
         return m_data[index];
      }
   }

   property int % MyProp2[int] {
      int% get(int index) {
         return m_data[index];
      }
      void set(int index, int % value) {}
   }

   property const int % MyProp3[int] {
      const int% get(int index) {
         return m_data[index];
      }
      void set(int index, const int % value) {}
   }

private:
   array<int>^ m_data;
};

int main() {
   R^ r = gcnew R(10);
   r->MyProp[4] = 4;   // C3070

   int value = 4;
   r->MyProp2[4] = value;   // OK
   r->MyProp3[4] = 4;   // OK
}
```