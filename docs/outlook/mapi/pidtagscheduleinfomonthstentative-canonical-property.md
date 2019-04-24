---
title: PidTagScheduleInfoMonthsTentative 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359760"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>PidTagScheduleInfoMonthsTentative 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
空き時間情報メッセージで仮の予定としてマークされた月を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|識別子:  <br/> |0x6851  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値の数は、0から、公開範囲で指定されている月数 ( **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) と PR_FREEBUSY_PUBLISH_END の間の期間) にする必要があります。 ****([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) プロパティ。
  
このプロパティの各値には、月と年がエンコードされています。 これは、"year × 16 + 月" という式を使用して計算されます。ここでは、年と月はグレゴリオ暦に基づいています。 値は昇順で並べ替えられ、リトルエンディアン形式でエンコードされます。 イベントが複数の月または複数年にわたる場合は、発行範囲に含まれる各月に1つの値が含まれている必要があります。 発行範囲に一時的なイベントがない場合は、このプロパティと**PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) を設定しないでください。または、既に存在する場合は削除する必要があります。 それ以外の場合は、このプロパティを設定する必要があります。
  
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

