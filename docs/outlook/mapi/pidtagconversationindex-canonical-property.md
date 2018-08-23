---
title: PidTagConversationIndex 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bddb667cba99e240a6ce182c9c1c8ed47f467e15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802630"
---
# <a name="pidtagconversationindex-canonical-property"></a>PidTagConversationIndex 標準プロパティ

  
  
**適用対象**: Outlook 
  
会話スレッド内でこのメッセージの相対的な位置を示すバイナリ値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|識別子:  <br/> |0x0071  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

会話スレッドは、メッセージと返信の系列を表します。 通常連結されたタイムスタンプ値を使用してこのプロパティが実装されます。 **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) が設定されている場合でもの使用はオプションですが。 
  
MAPI には、作成または会話のインデックスを更新する[ScCreateConversationIndex](sccreateconversationindex.md)関数が用意されています。 関数は、長さのバイト配列として現在のインデックス値を受け取るし、最後に連結するタイムスタンプを持つインデックス値を返します。 別のメッセージへの応答を表すメッセージは、このプロパティを更新するのには**ScCreateConversationIndex**を使用する必要があります。 
  
メッセージ ストア プロバイダーでは、 **PR_CONVERSATION_INDEX**は常に受信または送信メッセージに対して設定することを保証オプションがあります。 この**ScCreateConversationIndex**では、このプロパティが設定されている場合は、既存の値または NULL でない場合のいずれかを実行できます。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に、このアクションを実行する必要があります。 
  
**PR_CONVERSATION_TOPIC**に対して同じ値を持つすべてのメッセージは、メッセージの階層関係を表示するには、このプロパティで並べ替えることができます。 
  
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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

