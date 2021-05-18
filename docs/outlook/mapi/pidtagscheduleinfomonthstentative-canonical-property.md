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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359760"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>PidTagScheduleInfoMonthsTentative 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
空き時間情報メッセージに仮のマークが付いた月を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|識別子:  <br/> |0x6851  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値の数は **、0** から発行範囲でカバーされる月数 (PR_FREEBUSY_PUBLISH_START ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) プロパティと PR_FREEBUSY_PUBLISH_END **(** [PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) プロパティの間の期間である必要があります。
  
このプロパティの各値には、月と年がエンコードされています。 これは、年と月がグレゴリオ暦に基づく "年 × 16 + 月" という式を使用して計算されます。 値は昇順で並べ替え、リトル エンド形式でエンコードされます。 イベントが複数の月または複数の年にまたがっている場合は、発行範囲に含める各月に 1 つの値が必要です。 発行範囲に仮イベントがない場合は、このプロパティと **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) を設定したり、既に存在する場合は削除する必要があります。 それ以外の場合は、このプロパティを設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの可用性を公開します。
    
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

