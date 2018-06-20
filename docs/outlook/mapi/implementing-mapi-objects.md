---
title: MAPI オブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d53304dd74a0e54974d479c66637079cd48b2fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800931"
---
# <a name="implementing-mapi-objects"></a>MAPI オブジェクトを実装します。

  
  
**適用されます**: Outlook 
  
MAPI オブジェクトは、C++ のクラスや言語によっては、C のデータ構造を使用して実装できる API のクライアントの設定やサービス プロバイダーを使用します。 MAPI サービス プロバイダー インターフェイスと C または C++ でサービス プロバイダーを記述できます。クライアント アプリケーションは、C または C++ を使用することもできます。 可能であれば、クライアントとオブジェクト指向プログラミング ・ インタ フェースを使用するサービス プロバイダーは、C を使用する必要があります。 
  
C++ は、MAPI は、オブジェクト指向のテクノロジでは、および C++ に適していますより簡単にオブジェクト指向開発のための優先の選択です。 生成されるコードよりシンプルかつ簡単に維持するために簡単にします。 C++ 開発者は主に MAPI ドキュメントが書き込まれますC++ ではすべてこのリファレンスでは、MAPI インターフェイス メソッドの構文の説明です。
  
開発者は、MAPI を呼び出すためのソリューションを開発するのには、Microsoft Visual Studio、サードパーティ製の開発ツールを使用できます。 開発者が C またはアンマネージ C++ を使用する必要がありますが、MAPI のソリューションを作成するのには C++ が管理されていないことに注意してください。
  
MAPI オブジェクトが実装されている場合、クライアントまたはサービス プロバイダーはインターフェイスのメソッド、プライベート メソッドの実装に固有のコードと状態情報を維持するためのプライベート データ メンバーをサポートするためのコードのすべてのコードを作成します。 インターフェイス メソッドのコードは、正常な動作を文書化する MAPI によって公開された仕様に従う必要があります。 
  
Mapidefs.h ヘッダー ファイルとクライアントとのいずれかの言語サービス プロバイダーを使用して MAPI オブジェクトの定義に役立つ OLE ヘッダー ファイル内の多くのマクロがあります。 などの MAPI インターフェイスの各メソッドを定義するマクロがあります。 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを定義するマクロは、Mapidefs.h に次のように表示されます。 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>関連項目



[MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

