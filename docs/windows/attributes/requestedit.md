---
title: requestedit (atributo de COM de C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.requestedit
helpviewer_keywords:
- requestedit attribute
ms.assetid: b3c24790-3c4a-4646-8722-03d7b51172ee
ms.openlocfilehash: 27e6190cbb5908d46150acb758e2b4d5efaff1bb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50611594"
---
# <a name="requestedit"></a>requestedit

Indica que la propiedad admite la `OnRequestEdit` notificación.

## <a name="syntax"></a>Sintaxis

```cpp
[requestedit]
```

## <a name="remarks"></a>Comentarios

El **requestedit** atributo de C++ tiene la misma funcionalidad que el [requestedit](/windows/desktop/Midl/requestedit) atributo MIDL.

## <a name="example"></a>Ejemplo

Vea el ejemplo de [enlazable](bindable.md) para un ejemplo de uso de **requestedit**.

## <a name="requirements"></a>Requisitos

### <a name="attribute-context"></a>Contexto de atributo

|||
|-|-|
|**Se aplica a**|Método de interfaz|
|**Reiterativo**|No|
|**Atributos requeridos**|Ninguna|
|**Atributos no válidos**|Ninguna|

Para obtener más información acerca de los contextos de atributo, consulte [Contextos de atributo](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>Vea también

[Atributos IDL](idl-attributes.md)<br/>
[Atributos de método](method-attributes.md)<br/>
[Atributos de miembros de datos](data-member-attributes.md)<br/>
[defaultbind](defaultbind.md)<br/>
[displaybind](displaybind.md)<br/>
[immediatebind](immediatebind.md)