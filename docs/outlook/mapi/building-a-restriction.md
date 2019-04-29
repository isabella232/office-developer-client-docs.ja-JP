---
title: 制限の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422511"
---
# <a name="building-a-restriction"></a>制限の作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
制限を構築するために、クライアントアプリケーションは、さまざまな種類の1つ以上の制限構造から成る階層構造を作成し、その階層へのポインターを[imapitable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)メソッドに渡します。 次の図と[サンプル](sample-restriction-code.md)コードのコードサンプルでは、さまざまな種類のリンクされた制限構造を使用して一般的な制限を実装する方法について説明します。 

この例では、クライアントアプリケーションのユーザーが、題名行に "" という単語 "を含むすべてのメッセージを検索しようとしていますが、Sam から政美に送信されています。 最初に、一般的な[srestriction](srestriction.md)構造が割り当てられます。 この構造体は、 [MAPIFreeBuffer](mapifreebuffer.md)への1回の呼び出しで解放できるリンクされた[srestriction](srestriction.md)および[spropvalue](spropvalue.md)構造を作成するための、 [MAPIAllocateMore](mapiallocatemore.md)関数への他の呼び出しの基礎となります。 一連のメッセージに適用する条件は3つの部分に分けられるため、最上位の制限構造は、**および**制限です。 [SAndRestriction](sandrestriction.md)構造体の**cres**メンバーは3に設定されており、評価する3つの制限を示し、その**lpres**メンバーは、**制限**構造の3つのメンバー配列に設定されています。 
  
特定の受信者に送信されたメッセージを検索するには、メッセージ自体ではなく、メッセージごとに受信者テーブルを検索する必要があります。 サブテーブルの制限は、受信者テーブルの検索を実行するために使用されます。 そのため、配列の最初のメンバーは、ulsubmember を**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定した**** [ssubrestriction](ssubrestriction.md)構造体を指します。 次に、recipient テーブルで検索する内容を指定するために、コンテンツ制限が使用されます。 
  
配列の2番目と3番目のメンバーは、より簡単です。 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティが "Sam" に設定されており、もう一方が**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティが "" に設定されている別のメッセージを検索するために、コンテンツ制限構造をポイントしています。""
  
**実装の制限**
  
![制限の実装](media/amapi_61.gif "制限の実装")
  
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

