---
title: PidTagScheduleInfoAutoAcceptAppointments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330094"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>PidTagScheduleInfoAutoAcceptAppointments 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
出席者またはリソースのすべての会議出席依頼に対してクライアントまたはサーバーが自動的に応答する場合は、TRUE を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|識別子:  <br/> |0x686d  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>解説

**PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) または PR_SCHDINFO_DISALLOW_ によって指定された追加の制約がない限り、応答する場合は、応答を受け入れる必要があります。 **OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) のプロパティは満たされています。 値が FALSE の場合、またはこのプロパティが存在しない場合は、クライアントまたはサーバーが会議出席依頼を自動的に承諾してはいけないことを示します。 これは必須のプロパティではありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの空き時間情報を公開します。
    
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

