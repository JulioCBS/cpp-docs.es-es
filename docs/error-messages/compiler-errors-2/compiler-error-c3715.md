---
title: Error del compilador C3715
ms.date: 11/04/2016
f1_keywords:
- C3715
helpviewer_keywords:
- C3715
ms.assetid: ee5dce88-ddc4-4bdb-9464-47467ce1674f
ms.openlocfilehash: 94a451bbe936507ac3b33747065a9b6aac9edd02
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50660621"
---
# <a name="compiler-error-c3715"></a>Error del compilador C3715

'pointer': debe ser un puntero a 'class'

Se especificó un puntero en [__hook](../../cpp/hook.md) o [__unhook](../../cpp/unhook.md) que no señala a una clase válida. Para corregir este error, asegúrese de que su `__hook` y `__unhook` llamadas especifican punteros a clases válidas.