---
title: PidTagScheduleInfoMonthsMerged 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336478"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>PidTagScheduleInfoMonthsMerged 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
空き時間情報メッセージに、空き時間情報の種類または不在時 (OOF) メッセージが存在する月の一覧が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|識別子:  <br/> |0x684 f  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>解説

空き時間情報タイプの仮のイベントは、このプロパティには含まれません。 このプロパティの構文/書式と制約は、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) と同じですが、関連付けられた予定表オブジェクトの OOF または Busy に設定されている予定を参照しています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
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

