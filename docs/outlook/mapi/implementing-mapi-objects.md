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
  
MAPI オブジェクトは、言語およびクライアントまたはサービスプロバイダーが使用している API セットに応じて、C++ のクラスまたは C データ構造を使用して実装できます。 サービスプロバイダーは、MAPI サービスプロバイダインターフェイスを使用して C または C++ で記述できます。クライアントアプリケーションは C または C++ を使用することもできます。 可能な場合は、オブジェクト指向プログラミングインターフェイスを使用するクライアントおよびサービスプロバイダーに C++ を使用する必要があります。 
  
c++ は、MAPI はオブジェクト指向のテクノロジであり、c++ はオブジェクト指向の開発にもより容易に使用できるため、推奨される選択です。 生成されるコードはシンプルでわかりやすく、保守が容易になります。 MAPI ドキュメントは、主に C++ 開発者向けに記述されています。このリファレンスに記載されている MAPI インターフェイスメソッドのすべての構文の説明は、C++ に含まれています。
  
開発者は、Microsoft Visual Studio およびサードパーティの開発ツールを使用して MAPI を呼び出すソリューションを開発できます。 開発者は c またはアンマネージ c++ を使用する必要がありますが、管理された c++ を使用して MAPI ソリューションを記述することはできません。
  
MAPI オブジェクトが実装されている場合、クライアントまたはサービスプロバイダーは、すべてのインターフェイスメソッドのコード、実装に固有のプライベートメソッドのコード、および状態情報を保持するためのプライベートデータメンバーをサポートするコードを作成します。 インターフェイスメソッドのコードは、予期される動作を文書化する MAPI によって発行された仕様に従う必要があります。 
  
mapidefs.h ヘッダーファイルと OLE ヘッダーファイルには多数のマクロがあり、どちらの言語のクライアントとサービスプロバイダーも MAPI オブジェクトの定義を支援するために使用できます。 たとえば、各 MAPI インターフェイスのメソッドを定義するマクロがあります。 [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを定義するマクロは、mapidefs.h で次のように表示されます。 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>関連項目



[MAPI のオブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

