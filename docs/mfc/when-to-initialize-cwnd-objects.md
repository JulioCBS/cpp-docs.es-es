---
title: Cuándo inicializar los objetos CWnd
ms.date: 11/04/2016
helpviewer_keywords:
- window objects [MFC], when to initialize CWnd
- initializing CWnd objects [MFC]
- initializing objects [MFC], CWnd
- CWnd objects [MFC], when HWND is attached
- HWND, when attached to CWnd object
- CWnd objects [MFC], when to initialize
ms.assetid: 4d31bcb1-73db-4f2f-b71c-89b087569a10
ms.openlocfilehash: c75745547846fbf6c7e01ecf473d4d6f366bd264
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50548556"
---
# <a name="when-to-initialize-cwnd-objects"></a>Cuándo inicializar los objetos CWnd

No se puede crear sus propios secundarios windows o llamar a las funciones de API de Windows en el constructor de un `CWnd`-objeto derivado. Esto es porque el `HWND` para el `CWnd` objeto aún no se ha creado. Inicialización de Windows más específico, como agregar ventanas secundarias, debe realizarse dentro de un [OnCreate](../mfc/reference/cwnd-class.md#oncreate) controlador de mensajes.

## <a name="what-do-you-want-to-know-more-about"></a>¿Qué desea saber más sobre

- [Crear ventanas de marco de documento](../mfc/creating-document-frame-windows.md)

- [Crear documentos y vistas](../mfc/document-view-creation.md)

## <a name="see-also"></a>Vea también

[Uso de ventanas de marco](../mfc/using-frame-windows.md)

