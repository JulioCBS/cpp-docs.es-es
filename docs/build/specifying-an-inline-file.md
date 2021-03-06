---
title: Especificar un archivo insertado
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, inline files
- inline files [C++], specifying NMAKE
- files [C++], inline
ms.assetid: 393eccfb-3fc9-4bac-a30c-8ac8d221cca3
ms.openlocfilehash: 8f8868ce3755bd47f779576a7e44125f53314606
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50648705"
---
# <a name="specifying-an-inline-file"></a>Especificar un archivo insertado

Especificar dos corchetes angulares (<<) en el comando donde *filename* va a aparecer. Los corchetes angulares no puede ser una expansión de macro.

## <a name="syntax"></a>Sintaxis

```
<<[filename]
```

## <a name="remarks"></a>Comentarios

Cuando se ejecuta el comando, los corchetes angulares se reemplazan por *filename*, si se especifica, o por un nombre único generado por NMAKE. Si se especifica, *filename* debe seguir los corchetes angulares sin un espacio o tabulación. Se permite una ruta de acceso. Se necesita ninguna extensión o se supone que. Si *filename* se especifica, se crea el archivo actual o el directorio especificado, reemplazando los archivos con ese nombre; en caso contrario, se crea en el directorio TMP (o el directorio actual, si la variable de entorno TMP no está definido). Si una anterior *filename* es volver a usar, NMAKE reemplaza el archivo anterior.

## <a name="see-also"></a>Vea también

[Archivos insertados en un archivo MAKE](../build/inline-files-in-a-makefile.md)