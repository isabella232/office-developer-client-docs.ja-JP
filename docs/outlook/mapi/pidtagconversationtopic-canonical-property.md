---
title: PidTagConversationTopic の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2e656679fcf76992ec0b648274bd5ffa673b4007
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802636"
---
# <a name="pidtagconversationtopic-canonical-property"></a>PidTagConversationTopic の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
会話スレッドの最初のメッセージのトピックが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONVERSATION_TOPIC、PR_CONVERSATION_TOPIC_A、PR_CONVERSATION_TOPIC_W  <br/> |
|識別子:  <br/> |0x0070  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

会話スレッドは、メッセージと返信の系列を表します。 **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティには通常、スレッドの最初のメッセージのこれらのプロパティが設定されています。 スレッド内の後続のメッセージは、変更することがなく同じトピックを使用してください。 
  
**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティでは、後続のメッセージと返信の順序関係を示します。 使用はオプションですが、これらのプロパティを設定します。 
  
メッセージ ストア プロバイダーでは、これらのプロパティは常に受信または送信メッセージに対して設定することを保証オプションがあります。 これらのプロパティが既に設定されている場合それらを変更しないようにします。 それ以外の場合は、 **PR_NORMALIZED_SUBJECT**に設定することができます。 したアクションは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に実行する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

