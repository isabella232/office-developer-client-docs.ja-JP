---
title: PidTagConversationTopic 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f49bc6988ff7f7f06c22882e19d54dde6af44ce0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583513"
---
# <a name="pidtagconversationtopic-canonical-property"></a>PidTagConversationTopic 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会話スレッドの最初のメッセージのトピックを含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSATION_TOPIC、PR_CONVERSATION_TOPIC_A、PR_CONVERSATION_TOPIC_W  <br/> |
|識別子:  <br/> |0x0070  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

会話スレッドは、一連のメッセージと返信を表します。 これらのプロパティは、スレッド内の最初のメッセージに対して設定され、通常は PR_NORMALIZED_SUBJECT **(** [PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) プロパティに設定されます。 スレッド内の後続のメッセージでは、変更せずに同じトピックを使用する必要があります。 
  
プロパティ **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティは、後続のメッセージと返信の順序関係を示します。 これらのプロパティが設定されている場合でも、その使用はオプションです。 
  
メッセージ ストア プロバイダーには、これらのプロパティが常に受信メッセージまたは送信メッセージに設定されるのを保証するオプションがあります。 これらのプロパティが既に設定されている場合は、変更する必要があります。 指定しない場合は、これらの値を [PR_NORMALIZED_SUBJECT] **に設定できます**。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に、すべてのアクションを実行する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

