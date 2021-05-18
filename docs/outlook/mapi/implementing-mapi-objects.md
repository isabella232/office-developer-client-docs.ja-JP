---
title: MAPI オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310172"
---
# <a name="implementing-mapi-objects"></a>MAPI オブジェクトの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI オブジェクトは、クライアントまたはサービス プロバイダーが使用している言語と API セットに応じて、C++ クラスまたは C データ構造を使用して実装できます。 サービス プロバイダーは、MAPI サービス プロバイダー インターフェイスを使用して C または C++ で記述できます。クライアント アプリケーションは、C または C++ を使用できます。 可能であれば、オブジェクト指向プログラミング インターフェイスを使用するクライアントとサービス プロバイダーは C++ を使用する必要があります。 
  
MAPI はオブジェクト指向のテクノロジであり、C++ はオブジェクト指向の開発に容易に対応できるので、C++ が推奨される選択肢です。 結果として得られるコードは、より簡単で簡単になり、保守が容易になります。 MAPI ドキュメントは、主に C++ 開発者向けです。このリファレンスの MAPI インターフェイス メソッドの構文の説明はすべて C++ です。
  
開発者は、MAPI Microsoft Visual Studioソリューションを開発するために、サードパーティの開発ツールを使用できます。 開発者は C またはアンマネージ C++を使用する必要がありますが、MAPI ソリューションを記述するには管理 C++ を使用しない必要があります。
  
MAPI オブジェクトを実装すると、クライアントまたはサービス プロバイダーは、すべてのインターフェイス メソッドのコード、実装に固有のプライベート メソッドのコード、および状態情報を維持するためのプライベート データ メンバーをサポートするコードを作成します。 インターフェイス メソッドのコードは、MAPI によって発行された仕様に従って、予期される動作を文書化する必要があります。 
  
Mapidefs.h ヘッダー ファイルと OLE ヘッダー ファイルには、クライアントとサービス プロバイダーが MAPI オブジェクトの定義を支援するために使用できるマクロが多数存在します。 たとえば、各 MAPI インターフェイスのメソッドを定義するマクロがあります。 [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを定義するマクロは、Mapidefs.h に次のように表示されます。 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>関連項目



[MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

