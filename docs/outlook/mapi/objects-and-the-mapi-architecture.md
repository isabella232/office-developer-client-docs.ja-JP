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
  
MAPI で定義されるオブジェクトはすべて、MAPI アーキテクチャの 1 つ以上のレイヤーに含まれます。 クライアント インターフェイス層には、クライアント アプリケーション、フォーム ビューアー、またはフォーム サーバーが実装できるすべてのオブジェクトが含まれています。 サービス プロバイダー インターフェイス層には、任意の種類のサービス プロバイダーが実装できるオブジェクトが含まれています。 このレイヤーには、アドレス帳、メッセージ ストア、トランスポート プロバイダー、フォーム ライブラリによって実装されたオブジェクトが含まれます。 MAPI サブシステムを表すレイヤーは、クライアント インターフェイス層とサービス プロバイダー インターフェイス層の間に配置されます。 MAPI レイヤーには、MAPI がクライアントまたはサービス プロバイダーが使用するために実装するオブジェクトすべてが含まれています。 
  
次の図は、各 MAPI オブジェクトが MAPI アーキテクチャに適合する場所を示しています。 オブジェクトは、派生インターフェイスの名前で表されます。 たとえば、アドバイス シンク オブジェクトは [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) [、IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) から派生するインターフェイス、およびすべてのアアドバイス シンク オブジェクトが実装するインターフェイスとして表示されます。 ブリッジ 層を構成するインターフェイスは、複数のコンポーネントで使用または実装されます。 MAPI レイヤーは、クライアント層とプロバイダー層を分離する場合に表示されます。つまり、すべての通信が MAPI を経由する必要があります。これは当てはめではありません。 クライアントは、サービス プロバイダー オブジェクトと直接通信できます。 
  
**MAPI のオブジェクト レイヤー**
  
MAPI![の MAPI オブジェクト](media/amapi_38.gif "レイヤー内のオブジェクトレイヤー")
  
## <a name="see-also"></a>関連項目

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

