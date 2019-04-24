---
title: MAPI オブジェクトの継承階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345842"
---
# <a name="mapi-object-inheritance-hierarchy"></a>MAPI オブジェクトの継承階層

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI オブジェクトによって実装されるすべてのインターフェイスは、オブジェクトの通信を可能にする OLE インターフェイスである[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から継承されます。 ほとんどのインターフェイスは**IUnknown**から直接継承しますが、他の2つの基本インターフェイスのいずれかを継承します。 [imapiprop: IUnknown](imapipropiunknown.md)または[IMAPIContainer: imapiprop](imapicontainerimapiprop.md)。 次の図は、MAPI の完全な継承階層を示しています。
  
**MAPI 継承階層**
  
![MAPI 継承階層](media/amapi_06.gif "MAPI 継承階層")
  
## <a name="see-also"></a>関連項目

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [MAPI のオブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

