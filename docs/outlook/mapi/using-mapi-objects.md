---
title: MAPI オブジェクトを使用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a355faf85a44f6257b77b7171aa965faabf57fe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804210"
---
# <a name="using-mapi-objects"></a>MAPI オブジェクトを使用します。

**適用対象**: Outlook 
  
クライアントとサービス ・ プロバイダーは、そのインターフェイスの実装でのメソッドの呼び出しによって MAPI オブジェクトを使用します。 MAPI オブジェクトを使用することができることの唯一の方法は、このMAPI インターフェイスの外部オブジェクトによって実装されるメソッドは、パブリックにアクセス可能ではありません。 すべてのオブジェクトのインターフェイスは継承によって関連しているために、オブジェクトのユーザーは同じインターフェイスに属しているかのように基本インターフェイスまたは継承されたインターフェイスのいずれかのいずれかのメソッドを呼び出すことができます。 
  
メソッドへの呼び出しを実行しようとしているオブジェクトのユーザーと、そのオブジェクトには、継承によって関連するいくつかのインターフェイスが実装されて、ユーザー知る必要はありませんどのインタ フェースにメソッドが属しています。 ユーザーは、オブジェクトへのポインターを 1 つのインターフェイスのいずれかの任意のメソッドを呼び出すことができます。 たとえば、次の図では、folder オブジェクトをクライアント アプリケーションが使用する方法を示しています。 フォルダー オブジェクトの実装、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)から間接的に[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から継承するインターフェイスは、 [IMAPIProp: IUnknown](imapipropiunknown.md)と[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)。 **IMAPIProp**メソッドで、 [IMAPIProp::GetProps](imapiprop-getprops.md)などの 1 つは、いずれかのクライアントが呼び出すことができます、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)などのメソッドを[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)、同じオブジェクトへのポインターと同じようにします。 クライアントは、、またはこれらの呼び出しは、別のインターフェイスに属しているという事実によって影響を受ける。
  
**クライアントがフォルダー オブジェクトを使用**
  
![クライアントは、フォルダー オブジェクトの使用](media/amapi_40.gif "クライアントは、フォルダー オブジェクトの使用")
  
これらの呼び出しは、C または C++ の呼び出しを行うクライアントを作成するかどうかに応じて異なる方法でコードに変換します。 メソッドへの呼び出しをする前に、インターフェイスの実装へのポインターを取得する必要があります。 インターフェイス ポインターは、次の方法で入手できます。
  
- 別のオブジェクトのメソッドを呼び出しています。
    
- API 関数を呼び出しています。
    
- ターゲット オブジェクトの[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出しています。 
    
MAPI には、いくつかのメソッドとインターフェイスの実装へのポインターを返す API 関数が用意されています。 クライアントが、メッセージ ストア プロバイダーの情報へのアクセスを提供するテーブル オブジェクトへのポインターを取得するために[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを呼び出すことができますたとえば、 [IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースです。 サービス プロバイダーは、 [CreateTable](createtable.md)をテーブルのデータ オブジェクトへのポインターを取得するために API 関数を呼び出すことができます。 ない関数またはメソッドと、クライアントまたはサービス プロバイダー オブジェクトへのポインターがある、それらオブジェクトのインターフェイスの実装のもう 1 つへのポインターを取得するオブジェクトの**QueryInterface**メソッドを呼び出せます。 
  
## <a name="see-also"></a>関連項目

- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

