---
title: 制限を作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799745"
---
# <a name="building-a-restriction"></a>制限を作成します。

**適用されます**: Outlook 
  
制限を作成するには、クライアント アプリケーションは、さまざまな種類の 1 つまたは複数の制限の構造の階層を作成して、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)メソッドを階層構造にポインターを渡します。 次の図および[制限のサンプル コード](sample-restriction-code.md)のサンプル コードは、さまざまな種類の構造体をリンクの制限を持つ標準的な制限を実装する方法をデモンストレーションします。 

この例では、クライアント アプリケーションのユーザーは、件名に「バレーボール」という単語が含まれているし、、Sam から政美に送信されたすべてのメッセージを検索するとしています。 最初に[SRestriction](srestriction.md)ジェネリック構造体が割り当てられます。 この構造体の他の[MAPIFreeBuffer](mapifreebuffer.md)を 1 回の呼び出しでリンクされている[SRestriction](srestriction.md)と[SPropValue](spropvalue.md)構造体を解放することができますを作成する[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しの基盤となります。 一連のメッセージに適用する基準が 3 つの部分にあるため、最上位レベル制限構造は、**および**制限です。 [SAndRestriction](sandrestriction.md)構造体の**cRes**のメンバーは、評価するために 3 つの制限を示すために 3 に設定されてし、 **lpRes**メンバーが**SRestriction**構造体の 3 つのメンバーの配列を設定します。 
  
特定の受信者に送信されたメッセージを検索するには、メッセージ自体ではなく、各メッセージの受信者テーブルを検索する必要があります。 サブオブジェクトの制限を使用して、受信者テーブルの検索を実行します。 したがって、 [SSubRestriction](ssubrestriction.md)構造体を配列の要素の最初のメンバーの**ulSubObject**のメンバーでは、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定します。 次に、受信者テーブル内で検索するアイテムを指定するには、コンテンツの制限を使用します。 
  
配列の 2 番目と 3 番目のメンバーより簡単です。 両方ともは、コンテンツの制限、構造体、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティが設定された"Sam"と**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティに設定されているメッセージを検索する 1 つをポイント」バレーボール。」
  
**制限の実装**
  
![制限の実装](media/amapi_61.gif "制限の実装")
  
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

