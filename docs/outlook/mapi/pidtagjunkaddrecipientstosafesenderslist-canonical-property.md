---
title: PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394014"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>PidTagJunkAddRecipientsToSafeSendersList 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メール受信者が差出人セーフ リストに追加するかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|識別子:  <br/> |0x6103  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>備考

存在する場合、このプロパティが 0 または 1 に設定する必要があります。 1 の値は、メール受信者が差出人セーフ リストに追加することを示します。 0 の値は、メール受信者が差出人セーフ リストに追加されないことを示します。
  
このプロパティが 1 の値である場合は、迷惑メールのルールの条件の句を差出人セーフ リストに電子メールの受信者の SMTP アドレスを追加しなければなりません。 このプロパティが 0 の場合は、操作する必要はありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。
    
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

