---
title: PidTagConversationKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334700"
---
# <a name="pidtagconversationkey-canonical-property"></a>PidTagConversationKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IPM を検索するときにのみ、Microsoft Outlook で使用される会話キーが含まれ**ます。MessageManager**メッセージ (Post Office Protocol (POP3) アカウントのダウンロード履歴が含まれているメッセージなど)。 このプロパティは、Microsoft Exchange Server では廃止されました。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSATION_KEY  <br/> |
|識別子:  <br/> |0x000B  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

会話として電子メールメッセージにアクセスし、メッセージのプロパティを[トランスポートに中立的なカプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換する場合は、このプロパティを使用しないでください。代わりに、 [PidTagConversationIndex](pidtagconversationindex-canonical-property.md)プロパティと[PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)標準プロパティを使用します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IPM サブツリー](ipm-subtree.md)
  
[MAPI の特殊フォルダー](mapi-special-folders.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

