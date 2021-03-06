---
title: MMWORD
ms.date: 08/30/2018
f1_keywords:
- MMWORD
helpviewer_keywords:
- MMWORD directive
ms.assetid: b4c5a104-9078-4fb4-afc3-d1e63abe562a
ms.openlocfilehash: e4ebaa9d47a569bc9cf7d843d3ddb54ca5d713a0
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/09/2018
ms.locfileid: "51328232"
---
# <a name="mmword"></a>MMWORD

Se usa para los operandos multimedios de 64 bits con las instrucciones MMX y SSE (XMM).

## <a name="syntax"></a>Sintaxis

> MMWORD

## <a name="remarks"></a>Comentarios

`MMWORD` es un tipo.  Antes de MMWORD se agrega a MASM, una funcionalidad equivalente se podría haber conseguido con:

```asm
    mov mm0, qword ptr [ebx]
```

Aunque ambas instrucciones funcionan en los operandos de 64 bits, `QWORD` es el tipo de enteros sin signo de 64 bits y `MMWORD` es el tipo para un valor multimedia de 64 bits.

`MMWORD` está diseñado para representar el mismo tipo que [__m64](../../cpp/m64.md).

## <a name="example"></a>Ejemplo

```asm
    movq     mm0, mmword ptr [ebx]
```