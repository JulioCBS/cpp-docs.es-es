---
title: _com_error::Error
ms.date: 11/04/2016
f1_keywords:
- _com_error::Error
- Error
helpviewer_keywords:
- Error method [C++]
ms.assetid: b53a15fd-198e-4276-afcd-13439c4807f7
ms.openlocfilehash: 606f553060e71ece18b3d48159ec40133be28965
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50465473"
---
# <a name="comerrorerror"></a>_com_error::Error

**Específicos de Microsoft**

Recupera el valor HRESULT pasado al constructor.

## <a name="syntax"></a>Sintaxis

```
HRESULT Error( ) const throw( );
```

## <a name="return-value"></a>Valor devuelto

Elemento HRESULT sin formato pasado al constructor.

## <a name="remarks"></a>Comentarios

Recupera el elemento HRESULT encapsulado en un `_com_error` objeto.

**FIN de Específicos de Microsoft**

## <a name="see-also"></a>Vea también

[_com_error (Clase)](../cpp/com-error-class.md)