---
title: Advertencia del compilador de recursos RC4005
ms.date: 11/04/2016
f1_keywords:
- RC4005
helpviewer_keywords:
- RC4005
ms.assetid: 71f03b4a-c9a9-415d-920f-bf2e58507f93
ms.openlocfilehash: 571c4ac285e9477b017dbc21cf9ff733539759d2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50613608"
---
# <a name="resource-compiler-warning-rc4005"></a>Advertencia del compilador de recursos RC4005

'identifier': redefinición de macro

El identificador se define dos veces. El compilador usa la segunda definición de macro.

Esta advertencia puede deberse a la definición de una macro en la línea de comandos y en el código con un `#define` directiva. También puede deberse a macros importadas desde los archivos de inclusión.

Para eliminar la advertencia, quite una de las definiciones o use un `#undef` la directiva antes de la segunda definición.