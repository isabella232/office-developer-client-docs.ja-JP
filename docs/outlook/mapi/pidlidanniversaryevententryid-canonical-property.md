---
title: PidLidAnniversaryEventEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335575"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a>PidLidAnniversaryEventEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先の記念日を表す予定のエントリ id を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidAnniversaryEventEID  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x0000804E  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

**dispidAnniversaryEventEID**プロパティによって指定された予定は、 **dispidcontactlinkentry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md))、 **dispidcontactlinksearchkey** ([ ) を使用して、この連絡先にリンクされている必要があります。PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md))、および**dispidcontactname** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) の各プロパティ (「 [OXCMSG](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)」で説明されています)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

