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
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334721"
---
# <a name="pidtagconversationindex-canonical-property"></a>PidTagConversationIndex 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会話スレッド内でこのメッセージの相対位置を示すバイナリ値を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|識別子:  <br/> |0x0071  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

会話スレッドは、一連のメッセージと返信を表します。 このプロパティは、通常、連結されたタイムスタンプ値を使用して実装されます。 **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) が設定されている場合でも、この use はオプションです。 
  
MAPI では、スレッドインデックスを作成または更新する[ScCreateConversationIndex](sccreateconversationindex.md)関数が提供されています。 関数は、現在のインデックス値を、カウントされたバイト配列として取得し、最後にタイムスタンプが連結されたインデックス値を返します。 他のメッセージへの返信を表すメッセージでは、 **ScCreateConversationIndex**を使用してこのプロパティを更新する必要があります。 
  
メッセージストアプロバイダーには、 **PR_CONVERSATION_INDEX**が受信または送信メッセージで常に設定されることを保証するオプションがあります。 これを行うには、このプロパティが設定されている場合は既存の値、そうでない場合は NULL を使用して、 **ScCreateConversationIndex**を呼び出します。 このアクションは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出される前に実行する必要があります。 
  
**PR_CONVERSATION_TOPIC**の同じ値を持つすべてのメッセージをこのプロパティで並べ替えて、メッセージの階層的な関係を示すことができます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

