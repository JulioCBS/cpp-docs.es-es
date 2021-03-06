---
title: Advertencia de la línea de comandos D9025
ms.date: 11/04/2016
f1_keywords:
- D9025
helpviewer_keywords:
- D9025
ms.assetid: 6edff72c-1508-46c2-99f4-0e4b3c5e60c9
ms.openlocfilehash: fb9ab3152efe565501e91fbad5ebb279c4396968
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50652431"
---
# <a name="command-line-warning-d9025"></a>Advertencia de la línea de comandos D9025

reemplazando 'opción1' con 'opción2'

El *opción1* se especificó la opción pero, a continuación, se reemplazó por *opción2*. El *opción2* usó la opción.

Si dos opciones especifican directivas contradictorias o incompatibles, se usa la directiva especificadas o implícitas en la opción situado más a la derecha en la línea de comandos.

Si aparece esta advertencia al compilar desde el entorno de desarrollo y no está seguro de dónde proceden las opciones en conflicto, tenga en cuenta lo siguiente:

- Una opción puede especificarse en el código o en la configuración del proyecto. Si observa el compilador [páginas de propiedades de línea de comandos](../../ide/command-line-property-pages.md) y si ve las opciones en conflicto en el **todas las opciones** , a continuación, se establecen las opciones de páginas de propiedades del proyecto, en caso contrario, las opciones de campo se establecen en el código fuente.

   Si las opciones se establecen en páginas de propiedades del proyecto, busque en la página de propiedades preprocesador del compilador (con el nodo del proyecto seleccionado en el Explorador de soluciones).  Si no ve la opción definida allí, revise la configuración de la página de propiedades preprocesador para cada archivo de código fuente (en el Explorador de soluciones) para asegurarse de que no se agrega no existe.

   Si las opciones se establecen en el código se podría establecer en el código o en los encabezados de windows.  Puede intentar crear un archivo preprocesado ([/P](../../build/reference/p-preprocess-to-a-file.md)) y buscar el símbolo.