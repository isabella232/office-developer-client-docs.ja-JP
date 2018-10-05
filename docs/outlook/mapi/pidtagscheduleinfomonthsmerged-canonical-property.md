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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383822"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>PidTagScheduleInfoMonthsMerged 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ タイプを使用中の空き時間情報データや、不在 (時 OOF) の月の空き時間メッセージにリストが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|識別子:  <br/> |0x684F  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |空き/予約済み  <br/> |
   
## <a name="remarks"></a>備考

仮の予定の空き時間情報の種類のイベントは、このプロパティには含まれません。 構文と形式およびこのプロパティの制約は、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダー オブジェクトの不在時または取り込み中にマークされている予定を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの可用性を発行します。
    
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

