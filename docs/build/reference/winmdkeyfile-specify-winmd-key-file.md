---
title: /WINMDKEYFILE (especificar archivo de clave winmd)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.WINMDKeyFile
ms.assetid: 65d88fdc-fff9-49ea-8cfc-b2f408741734
ms.openlocfilehash: 076533278bb9b8ec2838cfb719bcb4df1784b258
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50436796"
---
# <a name="winmdkeyfile-specify-winmd-key-file"></a>/WINMDKEYFILE (especificar archivo de clave winmd)

Especifica una clave o un par de claves para firmar un archivo de metadatos en tiempo de ejecución de Windows (.winmd).

```
/WINMDKEYFILE:filename
```

## <a name="remarks"></a>Comentarios

Es similar a la [/keyfile](../../build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly.md) opción del vinculador que se aplica a un archivo .winmd.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Para establecer esta opción del vinculador en el entorno de desarrollo de Visual Studio

1. Abra el cuadro de diálogo **Páginas de propiedades** del proyecto. Para obtener más información, vea [Trabajar con propiedades del proyecto](../../ide/working-with-project-properties.md).

1. Seleccione el **vinculador** carpeta.

1. Seleccione el **Windows metadatos** página de propiedades.

1. En el **archivo de clave de metadatos de Windows** , escriba la ubicación del archivo.

## <a name="see-also"></a>Vea también

[Establecer las opciones del vinculador](../../build/reference/setting-linker-options.md)<br/>
[Opciones del vinculador](../../build/reference/linker-options.md)