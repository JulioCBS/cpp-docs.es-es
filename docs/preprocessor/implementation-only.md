---
title: implementation_only
ms.date: 11/04/2016
f1_keywords:
- implementation_only
helpviewer_keywords:
- implementation_only attribute
ms.assetid: d8cabc86-4425-45a0-9587-d57536980088
ms.openlocfilehash: 9bc083b78cd0c3bd39241de2815580c9eca6a207
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50654446"
---
# <a name="implementationonly"></a>implementation_only
**Específicos de C++**

Suprime la generación de archivos de encabezado .tlh (el archivo de encabezado principal).

## <a name="syntax"></a>Sintaxis

```
implementation_only
```

## <a name="remarks"></a>Comentarios

Este archivo contiene todas las declaraciones utilizadas para exponer el contenido de la biblioteca de tipos. El archivo de encabezado .tli, con las implementaciones de las funciones miembro del contenedor, se genera y se incluye en la compilación.

Cuando se especifica este atributo, el contenido del encabezado .tli está en el mismo espacio de nombres que el utilizado normalmente en el encabezado .tlh. Además, las funciones miembro no se declaran como alineadas.

El **implementation_only** atributo está pensado para su uso junto con el [no_implementation](../preprocessor/no-implementation.md) atributo como una manera de mantener las implementaciones fuera del archivo de encabezado precompilado (PCH). Una instrucción `#import` con el atributo `no_implementation` se coloca en la región de origen usada para crear el PCH. Varios archivos de código fuente utilizan el PCH resultante. Un `#import` instrucción con el **implementation_only** , a continuación, se usa el atributo fuera de la región PCH. Debe usar esta instrucción una sola vez en uno de los archivos de código fuente. Esto generará todas las funciones miembro del contenedor necesarias sin necesidad de recompilación adicional para cada archivo de código fuente.

> [!NOTE]
> El **implementation_only** atributo en uno `#import` instrucción debe usarse junto con otra `#import` instrucción de la misma biblioteca de tipos, con el `no_implementation` atributo. De lo contrario, se generarán errores de compilador. Esto es porque las definiciones de clase de contenedor generan por el `#import` instrucción con el `no_implementation` atributo son necesarias para compilar las implementaciones generadas por el **implementation_only** atributo.

**FIN de específicos de C++**

## <a name="see-also"></a>Vea también

[atributos #import](../preprocessor/hash-import-attributes-cpp.md)<br/>
[directiva #import](../preprocessor/hash-import-directive-cpp.md)