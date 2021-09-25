---
title: PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9bad8ceba8bc964fcb1d3c531ccb8a4e9d63d386
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587532"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メール受信者を差出人セーフ リストに追加するかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|識別子:  <br/> |0x6103  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>注釈

存在する場合、このプロパティは 0 または 1 に設定する必要があります。 値 1 は、メール受信者が差出人セーフ リストに追加されるかどうかを示します。 値 0 は、メール受信者が差出人セーフ リストに追加されないかどうかを示します。
  
このプロパティに値 1 が指定されている場合は、迷惑メール ルール条件の信頼できる senders 句に電子メール受信者の SMTP アドレスを追加する必要があります。 このプロパティが 0 の場合、アクションは必要ありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
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

