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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334721"
---
# <a name="pidtagconversationindex-canonical-property"></a>PidTagConversationIndex 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会話スレッド内のこのメッセージの相対位置を示すバイナリ値を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|識別子:  <br/> |0x0071  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

会話スレッドは、一連のメッセージと返信を表します。 このプロパティは、通常、連結されたタイム スタンプ値を使用して実装されます。 この使用は省略可能です [(pidTagConversationTopic](pidtagconversationtopic-canonical-property.md) **)** がPR_CONVERSATION_TOPIC設定されている場合でも使用できます。 
  
MAPI は [、会話インデックスを作成または更新する ScCreateConversationIndex](sccreateconversationindex.md) 関数を提供します。 この関数は、現在のインデックス値をカウントされたバイト配列として受け取り、タイムスタンプが末尾に連結されたインデックス値を返します。 別のメッセージへの返信を表すメッセージは **、ScCreateConversationIndex** を使用してこのプロパティを更新する必要があります。 
  
メッセージ ストア プロバイダーには、受信メッセージまたは送信メッセージに **PR_CONVERSATION_INDEXメッセージが** 常に設定されるのを保証するオプションがあります。 これを行うには **、ScCreateConversationIndex** を呼び出し、このプロパティが設定されている場合は既存の値を指定するか、設定されていない場合は NULL を指定します。 このアクションは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) が呼び出される前に実行する必要があります。 
  
このプロパティで同じ値を持 **PR_CONVERSATION_TOPIC** メッセージを並べ替え、メッセージの階層的な関係を表示できます。 
  
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

