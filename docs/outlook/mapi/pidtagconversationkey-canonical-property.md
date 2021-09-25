---
title: PidTagConversationKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c6e6825c0e899693d47457dff8d922db67f3adbb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555455"
---
# <a name="pidtagconversationkey-canonical-property"></a>PidTagConversationKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IpM の検索時にのみ、Microsoft Outlook会話キーが **格納されます。Post Office** プロトコル (POP3) アカウントのダウンロード履歴を含むメッセージなど、MessageManager メッセージ。 このプロパティは、このプロパティのMicrosoft Exchange Server。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONVERSATION_KEY  <br/> |
|識別子:  <br/> |0x000B  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

電子メール メッセージに会話としてアクセスし、メッセージ プロパティを [Transport-Neutral カプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換する場合は、このプロパティを使用しません。代わりに [、PidTagConversationIndex および](pidtagconversationindex-canonical-property.md) [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) 標準プロパティを使用します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのMicrosoft Exchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IPM サブツリー](ipm-subtree.md)
  
[MAPI の特別なフォルダー](mapi-special-folders.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

