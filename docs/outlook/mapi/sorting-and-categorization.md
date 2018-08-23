---
title: 並べ替えと分類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 12668cb87f21b56cd398a7b5375f6a4b40c65829
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581532"
---
# <a name="sorting-and-categorization"></a>並べ替えと分類

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルを並べ替えると、そのビューアーに意味のある順序で行が配置されます。 たとえば、1 つのビューアー会話のすべてのスレッドはまとめて別のビューアーはメッセージの送信者の名前で並べ替える必要がありますように、メッセージの件名でソートするフォルダーの内容を表示する方がよい。 必ずしも、新しくインスタンス化されたテーブルは、特定の順序では並べ替えられません。 
  
並べ替えの 2 種類があります。
  
- 標準の並べ替え
    
- 並べ替えの分類 
    
標準的な並べ替え順が、すべての行が並べ替えキーとして 1 つまたは複数の列を使用する単純なリストで表示されます。 分類された並べ替え順では、行が階層で表示される 1 つまたは複数の列の並べ替えキーとして。 カテゴリごとに、次の列を含む特別な見出し行があります。
  
- 列または列の並べ替えキーを構成します。
    
- **PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE**([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
並べ替えキーに一致する値を持つ列を含むテーブルからすべての行は、見出し行の下にインデントします。 これらの行は、リーフ行と呼ばれます。 リーフ行には、マイナス キー列の並べ替えを設定する列のすべての列が含まれています。 
  
フォルダーの内容のテーブルは多くの場合、標準の並べ替えだけでなくカテゴリ別に並べ替えをサポートします。 アドレス帳コンテナーの内容のテーブルは通常、標準的な並べ替えのみをサポートします。 
  
カテゴリが 2 つの状態を持つことができます: が折りたたまれているし、展開します。 カテゴリが折りたたまれた状態のときは、 [IMAPITable::QueryRows](imapitable-queryrows.md)から見出し行のみが返されます。 カテゴリが展開状態にすると、すべてのカテゴリに関連する行が返されます。 これには、見出し行とリーフ行が含まれます。 
  
表形式ビュー内の各カテゴリを展開または個別に折りたたまれています。 は同時に、すべてのカテゴリと同じ状態にする必要がありますは、他のユーザーが展開されている間は、いくつかのカテゴリを折りたたむことができます。 
  
分類されたテーブルのユーザーは、表示方法を決定します。 1 つの一般的なオプションでは、ツリー ビュー コントロールと呼ばれる Windows SDK で提供されているコントロールを使用します。 Treeview コントロールは、ツリーのような構造で情報をサポートするリスト ボックスです。 折りたたまれた状態のカテゴリの見出し行にはプラス記号が付いている間、展開した状態でのカテゴリの見出し行にはマイナス記号が付けられます。 展開されているカテゴリは、リーフ行が見出し行の下にインデントで表示されます。 
  
カテゴリを展開し、クライアント アプリケーションまたはサービス プロバイダーを使用して次[IMAPITable: IUnknown](imapitableiunknown.md)メソッド。 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
並べ替えの詳細については、会話のスレッドでは、次のトピックを参照してください。
  
- [SSortOrder](ssortorder.md)
    
- [PidTagSubject 標準プロパティ](pidtagsubject-canonical-property.md)
    
- [PidTagSubjectPrefix 標準プロパティ](pidtagsubjectprefix-canonical-property.md)
    
- [PidTagNormalizedSubject 標準プロパティ](pidtagnormalizedsubject-canonical-property.md)
    
- [PidTagConversationTopic 標準プロパティ](pidtagconversationtopic-canonical-property.md)
    
- [PidTagConversationIndex 標準プロパティ](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [列および制限の設定後のテーブルの並べ替え](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

