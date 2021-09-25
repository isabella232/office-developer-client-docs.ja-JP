---
title: 制限の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5036a4989c8a25cecbe31c20512f8f46fec80c54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556925"
---
# <a name="building-a-restriction"></a>制限の作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
制限を構築するために、クライアント アプリケーションは、さまざまな種類の 1 つ以上の制限構造の階層を作成し、階層へのポインターを [IMAPITable::Restrict](imapitable-restrict.md) メソッドまたは [IMAPITable::FindRow](imapitable-findrow.md) メソッドに渡します。 次の図とサンプル制限コードのコード[](sample-restriction-code.md)サンプルは、さまざまな種類のリンクされた制限構造で一般的な制限がどのように実装されるのか示しています。 

この例では、クライアント アプリケーションのユーザーが、件名行に "バレー" という単語を含み、Sam から Sue に送信されたメッセージを検索します。 最初に、 [汎用の SRestriction 構造体](srestriction.md) が割り当てられている。 この構造体は[、MAPIAllocateMore](mapiallocatemore.md)関数への他の呼び出しの基礎になり[、MAPIFreeBuffer](mapifreebuffer.md)への 1 回の呼び出しで解放できるリンク[された SRestriction](srestriction.md)構造体と[SPropValue](spropvalue.md)構造体を作成します。 メッセージのセットに適用する条件は 3 つの部分にあるため、トップ レベルの制限構造は **AND** 制限です。 [SAndRestriction](sandrestriction.md)構造体の **cRes** メンバーは 3 に設定され、評価する 3 つの制限を示し **、lpRes** メンバーは **SRestriction** 構造体の 3 つのメンバー配列に設定されます。 
  
特定の受信者に送信されるメッセージを検索するには、メッセージ自体ではなく、メッセージごとに受信者テーブルを検索する必要があります。 サブオブジェクトの制限は、受信者テーブルの検索を実行するために使用されます。 したがって、配列の最初のメンバーは **、ulSubObject** メンバーが PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)に設定された [SSubRestriction](ssubrestriction.md)構造体をポイントします。 次に、受信者テーブルで検索する内容を指定するために、コンテンツ制限が使用されます。 
  
配列の 2 番目と 3 番目のメンバーは、より簡単です。 どちらもコンテンツ制限構造を指し示し、PR_SENDER_NAME ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティが "Sam" に設定されているメッセージと **、PR_SUBJECT** **(** [PidTagSubject](pidtagsubject-canonical-property.md)) プロパティが "バレーボール" に設定されているメッセージを検索します。
  
**実装の制限**
  
![実装の制限](media/amapi_61.gif "実装の制限")
  
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

