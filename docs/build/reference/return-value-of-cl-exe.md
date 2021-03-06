---
title: Valor devuelto de cl.exe
ms.date: 09/05/2018
helpviewer_keywords:
- cl.exe compiler, return value
ms.assetid: 7c2d7f33-ee0d-4199-8ef4-75fe2b007670
ms.openlocfilehash: 39b53731d94e3b5ff5fcb666caac6a584c34d287
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50656084"
---
# <a name="return-value-of-clexe"></a>Valor devuelto de cl.exe

cl.exe devuelve cero si es correcto (no tiene errores) y un valor distinto de cero en caso contrario.

El valor devuelto de cl.exe puede ser útil si está compilando un script o un archivo de powershell, .cmd o .bat. Es recomendable que capture el resultado del compilador en caso de que haya errores o advertencias para que pueda resolverlos.

Hay demasiados códigos de salida de error posibles para que cl.exe los muestre todos. Puede buscar un código de error en el archivo winerror.h o ntstatus.h archivos incluyen en el Kit de desarrollo de Software de Windows en la carpeta % (x86) ProgramFiles %\Windows Kits\\<em>versión</em>directory \Include\shared\. Los códigos de error devueltos en formato decimal deben convertirse en formato hexadecimal para poder realizar la búsqueda. Por ejemplo, el valor hexadecimal de un código de error -1073741620 es 0xC00000CC. Este error se encuentra en ntstatus.h, donde el mensaje correspondiente especificado es: "No se puede encontrar en el servidor remoto el nombre compartido especificado". Para obtener una lista descargable de códigos de error de Windows, consulte [ &#91;MS ERREF&#93;: códigos de Error de Windows](https://msdn.microsoft.com/library/cc231196).

También puede usar la utilidad de búsqueda de errores de Visual Studio para averiguar lo que significa un mensaje de error del compilador. En un shell de comandos de Visual Studio, escriba **errlook.exe** para iniciar la utilidad; o en el IDE de Visual Studio, en la barra de menús, elija **herramientas**, **Error Lookup**. Escriba el valor del error para buscar texto descriptivo asociado al error. Para obtener más información, consulte [referencia de ERRLOOK](../../build/reference/errlook-reference.md).

## <a name="remarks"></a>Comentarios

A continuación se muestra un ejemplo de un archivo .bat en el que se utiliza el valor devuelto de cl.exe.

```cmd
echo off
cl /W4 t.cpp
@if ERRORLEVEL == 0 (
   goto good
)

@if ERRORLEVEL != 0 (
   goto bad
)

:good
   echo "clean compile"
   echo %ERRORLEVEL%
   goto end

:bad
   echo "error or warning"
   echo %ERRORLEVEL%
   goto end

:end
```

## <a name="see-also"></a>Vea también

[Sintaxis de la línea de comandos del compilador](../../build/reference/compiler-command-line-syntax.md)