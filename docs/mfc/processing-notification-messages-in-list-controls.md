---
title: Procesar mensajes de notificación en los controles de lista
ms.date: 11/04/2016
helpviewer_keywords:
- processing notifications [MFC]
- CListCtrl class [MFC], processing notifications
ms.assetid: 1f0e296e-d2a3-48fc-ae38-51d7fb096f51
ms.openlocfilehash: 427abe5259334588b566656abd70acf22b923809
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50490095"
---
# <a name="processing-notification-messages-in-list-controls"></a>Procesar mensajes de notificación en los controles de lista

Como los usuarios, haga clic en los encabezados de columna, arrastre los iconos, editar etiquetas y así sucesivamente, el control de lista ([CListCtrl](../mfc/reference/clistctrl-class.md)) envía mensajes de notificación a su ventana primaria. Controle estos mensajes si desea hacer algo en respuesta. Por ejemplo, cuando el usuario hace clic en un encabezado de columna, es posible que desee ordenar los elementos según el contenido de la columna seleccionada, como en Microsoft Outlook.

Procese los mensajes WM_NOTIFY desde el control de lista en la clase de vista o cuadro de diálogo. Utilice la ventana Propiedades para crear un [OnChildNotify](../mfc/reference/cwnd-class.md#onchildnotify) función de controlador con una instrucción switch en función de qué mensaje de notificación que se está controlando.

Para obtener una lista de las notificaciones que puede enviar un control de lista a su ventana primaria, consulte [referencia de Control de vista de lista](/windows/desktop/Controls/list-view-control-reference) en el SDK de Windows.

## <a name="see-also"></a>Vea también

[Uso de CListCtrl](../mfc/using-clistctrl.md)<br/>
[Controles](../mfc/controls-mfc.md)

