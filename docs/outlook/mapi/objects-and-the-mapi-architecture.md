---
title: オブジェクトと MAPI アーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f37b5bd452f35e54edee6f98387c6f39d284106
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561181"
---
# <a name="objects-and-the-mapi-architecture"></a>オブジェクトと MAPI アーキテクチャ

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI で定義されるオブジェクトはすべて、MAPI アーキテクチャの 1 つ以上のレイヤーに含まれます。 クライアント インターフェイス層には、クライアント アプリケーション、フォーム ビューアー、またはフォーム サーバーが実装できるすべてのオブジェクトが含まれています。 サービス プロバイダー インターフェイス層には、任意の種類のサービス プロバイダーが実装できるオブジェクトが含まれています。 このレイヤーには、アドレス帳、メッセージ ストア、トランスポート プロバイダー、フォーム ライブラリによって実装されたオブジェクトが含まれます。 MAPI サブシステムを表すレイヤーは、クライアント インターフェイス層とサービス プロバイダー インターフェイス層の間に配置されます。 MAPI レイヤーには、MAPI がクライアントまたはサービス プロバイダーが使用するために実装するオブジェクトすべてが含まれています。 
  
次の図は、各 MAPI オブジェクトが MAPI アーキテクチャに適合する場所を示しています。 オブジェクトは、派生インターフェイスの名前で表されます。 たとえば、アドバイス シンク オブジェクトは [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) [、IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) から派生するインターフェイス、およびすべてのアアドバイス シンク オブジェクトが実装するインターフェイスとして表示されます。 ブリッジ 層を構成するインターフェイスは、複数のコンポーネントで使用または実装されます。 MAPI レイヤーは、クライアント層とプロバイダー層を分離する場合に表示されます。つまり、すべての通信が MAPI を経由する必要があります。これは当てはめではありません。 クライアントは、サービス プロバイダー オブジェクトと直接通信できます。 
  
**MAPI のオブジェクト レイヤー**
  
![MAPI のオブジェクト レイヤー](media/amapi_38.gif "MAPI のオブジェクト レイヤー")
  
## <a name="see-also"></a>関連項目

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

