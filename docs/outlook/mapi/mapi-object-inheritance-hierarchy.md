---
title: MAPI オブジェクトの継承階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: af56854905b05f8b2c878f98c3e3c1c17971fc4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567173"
---
# <a name="mapi-object-inheritance-hierarchy"></a>MAPI オブジェクトの継承階層

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI オブジェクトによって実装されたインターフェイスはすべて、最終的に [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)(オブジェクトの通信を可能にする OLE インターフェイス) から継承されます。 ほとんどのインターフェイスは **IUnknown** から直接継承しますが [、IMAPIProp : IUnknown](imapipropiunknown.md) または [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). 次の図は、MAPI の完全な継承階層を示しています。
  
**MAPI 継承階層**
  
![MAPI 継承階層](media/amapi_06.gif "MAPI 継承階層")
  
## <a name="see-also"></a>関連項目

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

