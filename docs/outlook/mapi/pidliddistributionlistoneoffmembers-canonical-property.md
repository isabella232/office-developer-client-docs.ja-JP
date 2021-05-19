---
title: PidLidDistributionListOneOffMembers 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335050"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>PidLidDistributionListOneOffMembers 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用配布リストのメンバーに対応する 1 回限定の EntryId の一覧を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidDLOneOffMembers  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008054  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

これらの 1 回限定の EntryIds は、個人用配布リスト メンバーの表示名と電子メール アドレスをカプセル化します。
  
クライアントまたはサーバーでこのプロパティを設定する場合は **、dispidDLMembers** [(PidLidDistributionListMembers)](pidliddistributionlistmembers-canonical-property.md)プロパティと同期する必要があります **。dispidDLOneOffMembers** プロパティの各エントリに対して **、dispidDLMembers** プロパティ内に同じ位置にエントリが必要です。 
  
**dispidDLOneOffMembers** を設定する場合、クライアントまたはサーバーは、その合計サイズが 15,000 バイト未満のサイズである必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

