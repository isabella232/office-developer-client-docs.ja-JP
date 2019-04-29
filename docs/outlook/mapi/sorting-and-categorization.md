---
title: 並べ替えと分類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418485"
---
# <a name="sorting-and-categorization"></a>並べ替えと分類

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルを並べ替えると、表示されるのがわかりやすい順序で行が配置されます。 たとえば、ある閲覧者は、メッセージの件名で並べ替えたフォルダーの内容テーブルを表示して、会話のすべてのスレッドが一緒に表示されるようにしたり、別の閲覧者が送信者の名前で並べ替えられたメッセージを表示したりできるようにしたい場合があります。 新たにインスタンス化されたテーブルは、必ずしも特定の順序で並べ替えられるとは限りません。 
  
並べ替えには、次の2種類があります。
  
- 標準の並べ替え
    
- 分類された並べ替え 
    
標準の並べ替えでは、1つまたは複数の列を並べ替えキーとして使用して、すべての行がフラットリストに表示されます。 分類された並べ替えの場合、行は、並べ替えキーとして1つまたは複数の列と共に階層的に表示されます。 各カテゴリ内には、次の列を含む特別な見出し行があります。
  
- 並べ替えキーを構成する列 (複数の場合があります)
    
- **PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE**([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
見出し行の下のインデントは、並べ替えキーと一致する値を持つ列を含むテーブルのすべての行です。 これらの行はリーフ行と呼ばれます。 リーフ行には、列セットのすべての列と並べ替えキー列が含まれています。 
  
フォルダーの内容の表は、通常、標準の並べ替えに加えて、分類された並べ替えをサポートします。 通常、アドレス帳コンテナーのコンテンツテーブルは標準の並べ替えのみをサポートします。 
  
カテゴリには、折りたたまれて展開される2つの状態があります。 カテゴリが折りたたまれた状態の場合は、見出し行のみが[IMAPITable:: QueryRows](imapitable-queryrows.md)から返されます。 カテゴリが展開された状態になると、そのカテゴリに関連するすべての行が返されます。 これには、見出し行とリーフ行が含まれます。 
  
テーブルビューの各カテゴリは個別に展開または折りたたむことができます。 つまり、すべてのカテゴリが同時に同じ状態である必要はありません。一部のカテゴリは折りたたむことができ、他のカテゴリは展開されます。 
  
分類されたテーブルのユーザーが、表示方法を決定します。 1つの一般的なオプションは、treeview コントロールと呼ばれる Windows SDK で提供されるコントロールを使用することです。 Treeview コントロールは、ツリーに似た構造の情報をサポートするリストボックスです。 展開された状態のカテゴリの見出し行には、マイナス記号が付いています。折りたたまれた状態のカテゴリの見出し行には、プラス記号が付いています。 展開されたカテゴリは、列見出しの下にあるリーフ行と共に表示されます。 
  
カテゴリを折りたたむと展開するために、クライアントアプリケーションまたはサービスプロバイダーは、次の[IMAPITable: IUnknown](imapitableiunknown.md)メソッドを使用します。 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
会話のスレッドの並べ替えの詳細については、以下のトピックを参照してください。
  
- [SSortOrder](ssortorder.md)
    
- [PidTagSubject 標準プロパティ](pidtagsubject-canonical-property.md)
    
- [PidTagSubjectPrefix 標準プロパティ](pidtagsubjectprefix-canonical-property.md)
    
- [PidTagNormalizedSubject 標準プロパティ](pidtagnormalizedsubject-canonical-property.md)
    
- [PidTagConversationTopic 標準プロパティ](pidtagconversationtopic-canonical-property.md)
    
- [PidTagConversationIndex 標準プロパティ](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [列と制限の設定後のテーブルの並べ替え](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

