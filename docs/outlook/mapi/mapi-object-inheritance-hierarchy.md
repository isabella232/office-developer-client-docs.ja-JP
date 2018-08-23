---
title: MAPI オブジェクトの継承階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4b2b9971677312dbea297c9fe2d29ba65174904d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588791"
---
# <a name="mapi-object-inheritance-hierarchy"></a>MAPI オブジェクトの継承階層

**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI オブジェクトによって実装されるすべてのインタ フェースは、最終的には、 [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)を通信するためにオブジェクトを有効にする OLE インターフェイスから継承します。 ほとんどのインターフェイスは、 **IUnknown**から直接継承するが、他の 2 つの基本インターフェイスのいずれかの一部を継承: [IMAPIProp: IUnknown](imapipropiunknown.md)または[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)。 次の図では、MAPI の完全な継承階層を示します。
  
**MAPI 継承階層**
  
![MAPI の継承の階層構造](media/amapi_06.gif "MAPI の継承の階層構造")
  
## <a name="see-also"></a>関連項目

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

