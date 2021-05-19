---
title: PidLidDistributionListMembers 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335071"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>PidLidDistributionListMembers 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用配布リストのメンバーに対応するオブジェクトの EntryIds の一覧を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidDLMembers  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008055  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

個人用配布リストのメンバーには、他の個人用配布リスト、連絡先に含まれる電子アドレス、グローバル アドレス一覧のユーザーまたは配布リスト、または 1 回限定の電子メール アドレスを指定できます。 各 EntryId の形式は [、[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) で指定されている 1 回限りの EntryId か、ラップされた EntryId のいずれかである必要があります。 
  
このプロパティを設定する場合、クライアントまたはサーバーは、その合計サイズが 15,000 バイト未満である必要があります。
  
このプロパティは、個人用配布リストのメンバーに対応する 1 回限定の EntryId の一覧を指定します。 これらの 1 回限定の EntryIds は、個人用配布リスト メンバーの表示名と電子メール アドレスをカプセル化します。
  
クライアントまたはサーバーでこのプロパティを設定する場合は **、dispidDLOneOffMembers** [(PidLidDistributionListOneOffMembers)](pidliddistributionlistoneoffmembers-canonical-property.md)プロパティ内の各エントリについて、このプロパティ **dispidDLOneOffMembers と同期する必要があります。dispidDLOneOffMembers** 内に同じ位置にエントリが必要です。 
  
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

