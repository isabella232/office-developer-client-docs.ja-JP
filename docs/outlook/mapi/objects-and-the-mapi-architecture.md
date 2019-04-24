---
title: オブジェクトと MAPI アーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279790"
---
# <a name="objects-and-the-mapi-architecture"></a>オブジェクトと MAPI アーキテクチャ

**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi で定義されているすべてのオブジェクトは、mapi アーキテクチャの1つ以上のレイヤーに分類されます。 クライアントインターフェイスレイヤーには、クライアントアプリケーション、フォームビューアー、またはフォームサーバーが実装できるすべてのオブジェクトが含まれています。 サービスプロバイダインターフェイスレイヤーには、任意の種類のサービスプロバイダーが実装できるオブジェクトが含まれています。 このレイヤーには、アドレス帳、メッセージストア、トランスポートプロバイダー、およびフォームライブラリによって実装されるオブジェクトが含まれます。 MAPI サブシステムを表すレイヤーは、クライアントとサービスプロバイダのインターフェイス層の間に配置されます。 mapi 層には、クライアントまたはサービスプロバイダーが使用するために mapi が実装するすべてのオブジェクトが含まれています。 
  
次の図は、mapi の各オブジェクトが mapi アーキテクチャに適合する場所を示しています。 オブジェクトは、派生したインターフェイスの名前で表されます。 たとえば、アドバイズシンクオブジェクトは[IMAPIAdviseSink: iunknown](imapiadvisesinkiunknown.md)として表示されます。このインターフェイスは、すべてのアドバイズシンクオブジェクトに実装されているので[iunknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から派生しています。 レイヤーをブリッジするインターフェイスは、複数のコンポーネントによって使用されているか、実装されています。 mapi 層は、クライアント層とプロバイダー層を分離して表示されますが、すべての通信は MAPI を経由する必要があるということを意味しますが、そうではありません。 クライアントは、サービスプロバイダオブジェクトに直接通信できます。 
  
**MAPI のオブジェクト レイヤー**
  
![MAPI のオブジェクトレイヤー](media/amapi_38.gif "MAPI のオブジェクトレイヤー")
  
## <a name="see-also"></a>関連項目

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [MAPI のオブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

