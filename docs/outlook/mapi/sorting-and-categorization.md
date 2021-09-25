---
title: 並べ替えと分類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: f7431bf9b6212ebda0a590962a7a74b2945ae6f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578565"
---
# <a name="sorting-and-categorization"></a>並べ替えと分類

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルを並べ替えると、ビューワーに合った順序で行が表示されます。 たとえば、ある閲覧者がメッセージの件名で並べ替えたフォルダーのコンテンツ テーブルを表示して、会話のすべてのスレッドが一緒に表示され、別のビューアーがメッセージを送信者の名前で並べ替えたい場合があります。 新しくインスタンス化されたテーブルは、必ずしも特定の順序で並べ替える必要があります。 
  
並べ替えには次の 2 種類があります。
  
- 標準の並べ替え
    
- 分類された並べ替え 
    
標準の並べ替えでは、1 つ以上の列を並べ替えキーとして使用して、すべての行がフラット リストに表示されます。 分類された並べ替えでは、1 つ以上の列を並べ替えキーとして階層的に表示します。 各カテゴリ内には、次の列を含む特別な見出し行があります。
  
- 並べ替えキーを作成する列または列
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
見出し行の下にインデントは、並べ替えキーに一致する値を持つ列を含むテーブルのすべての行です。 これらの行はリーフ行と呼ばれる。 リーフ行には、列セット内のすべての列から並べ替えキー列を差し引いた列が含まれます。 
  
多くの場合、フォルダーのコンテンツ テーブルでは、標準の並べ替えに加えて分類された並べ替えをサポートしています。 アドレス帳コンテナーのコンテンツ テーブルは、通常、標準の並べ替えのみをサポートします。 
  
カテゴリには、折りたたみと展開の 2 つの状態を指定できます。 カテゴリが折りたたみ状態の場合 [、IMAPITable::QueryRows](imapitable-queryrows.md)から見出し行だけが返されます。 カテゴリが展開状態の場合、そのカテゴリに関連する行すべてが返されます。 これには、見出し行とリーフ行が含まれます。 
  
テーブル ビュー内の各カテゴリは、個別に展開または折りたたみできます。 つまり、すべてのカテゴリが同時に同じ状態である必要があります。一部のカテゴリは折りたたむ可能性があります。他のカテゴリは展開されます。 
  
分類されたテーブルのユーザーは、表示方法を決定します。 一般的なオプションの 1 つは、ツリー ビュー コントロールと呼Windows SDK で提供されるコントロールを使用する方法です。 Treeview コントロールは、ツリーのような構造の情報をサポートするリスト ボックスです。 展開された状態のカテゴリの見出し行にはマイナス記号が付き、折りたたみ状態のカテゴリの見出し行にはプラス記号が付けられます。 展開されたカテゴリは、見出し行の下にインデントされたリーフ行で表示されます。 
  
カテゴリを折りたたみ、展開するには、クライアント アプリケーションまたはサービス プロバイダーが次の [IMAPITable : IUnknown](imapitableiunknown.md) メソッドを使用します。 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
スレッドのスレッドの並べ替えの詳細については、次のトピックを参照してください。
  
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

