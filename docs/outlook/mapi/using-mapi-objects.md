---
title: MAPI オブジェクトの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6ffa5403121ba86d113647e4da47cdfd8b18eb71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619492"
---
# <a name="using-mapi-objects"></a>MAPI オブジェクトの使用

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントとサービス プロバイダーは、インターフェイスの実装でメソッドを呼び出すことによって MAPI オブジェクトを使用します。 これは、MAPI オブジェクトを使用できる唯一の方法です。MAPI インターフェイスの外部のオブジェクトによって実装されるメソッドは、パブリックにアクセスできない。 オブジェクトのすべてのインターフェイスは継承によって関連付け可能なので、オブジェクトのユーザーは、基本インターフェイスまたは継承されたインターフェイスの 1 つのメソッドを、同じインターフェイスに属している場合と同様に呼び出す可能性があります。 
  
オブジェクトのユーザーがメソッドを呼び出し、そのオブジェクトが継承によって関連する複数のインターフェイスを実装する場合、ユーザーはメソッドが属するインターフェイスを知る必要はありません。 ユーザーは、オブジェクトへの 1 つのポインターを使用して、インターフェイス上の任意のメソッドを呼び出します。 たとえば、次の図は、クライアント アプリケーションがフォルダー オブジェクトを使用する方法を示しています。 フォルダー オブジェクトは [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) インターフェイスを実装します [。IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) から [IMAPIProp : IUnknown](imapipropiunknown.md) と [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)を介して間接的に継承されます。 クライアントは [、IMAPIProp::GetProps](imapiprop-getprops.md)などの **IMAPIProp** メソッドのいずれかを呼び出し、IMAPIFolder : [IMAPIContainer メソッド (IMAPIFolder::CreateMessage](imapifolder-createmessage.md)など) を同じ方法で同じオブジェクト ポインターで呼び出します。 [](imapifolderimapicontainer.md) クライアントは、これらの呼び出しが異なるインターフェイスに属しているという事実に気づいても影響を受けもしません。
  
**クライアントがフォルダー オブジェクトを使用**
  
![クライアントがフォルダー オブジェクトを使用](media/amapi_40.gif "クライアントがフォルダー オブジェクトを使用")
  
これらの呼び出しは、呼び出しを行うクライアントが C または C++ で記述されるかどうかによって異なるコードに変換されます。 メソッドを呼び出す前に、インターフェイス実装へのポインターを取得する必要があります。 インターフェイス ポインターは、次の方法で取得できます。
  
- 別のオブジェクトでメソッドを呼び出す。
    
- API 関数の呼び出し。
    
- ターゲット オブジェクト [で IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) メソッドを呼び出します。 
    
MAPI には、インターフェイス実装へのポインターを返すいくつかのメソッドと API 関数が提供されています。 たとえば、クライアントは [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) メソッドを呼び出して [、IMAPITable : IUnknown](imapitableiunknown.md) インターフェイスを介してメッセージ ストア プロバイダー情報へのアクセスを提供するテーブル オブジェクトへのポインターを取得できます。 サービス プロバイダーは、API 関数 CreateTable を呼 [び出して](createtable.md) 、テーブル データ オブジェクトへのポインターを取得できます。 使用可能な関数またはメソッドが存在し、クライアントまたはサービス プロバイダーがオブジェクトへのポインターを既に持っている場合は、オブジェクトの **QueryInterface** メソッドを呼び出して、オブジェクトのインターフェイス実装の別のポインターを取得できます。 
  
## <a name="see-also"></a>関連項目

- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

