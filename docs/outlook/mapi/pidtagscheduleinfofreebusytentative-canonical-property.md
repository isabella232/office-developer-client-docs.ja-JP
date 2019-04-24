---
title: PidTagScheduleInfoFreeBusyTentative 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359775"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>PidTagScheduleInfoFreeBusyTentative 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
空き時間情報の状態が [仮承諾] である時間のブロックが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|識別子:  <br/> |0x6852  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値の個数は、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) の値の数と同じです。 各バイナリ値は月を表し、 **PR_SCHDINFO_MONTHS_TENTATIVE**の同じインデックスの値に対応します。 バイナリ値は、 **PR_SCHDINFO_MONTHS_TENTATIVE**の値と同じ順序で並べ替えられます。
  
各バイナリ値には、1つまたは複数の4バイトブロックがあり、それぞれの最初の2バイトの開始時刻と終了時刻はリトルエンディアン形式になっています。 start time は、月の最初の日のグリニッジ標準時 (utc) と、イベントの開始時刻 (utc) の間の時間 (分単位) です。 終了時刻は、月の最初の日の午前0時から utc の終了時刻までの時間を分単位で示します。 4バイトブロックは、昇順で並べ替えられます。
  
時間の連続または重複するブロックは、開始時間が最初のブロックの開始時刻と最後のブロックの終了時刻として、1つのブロックにマージされます。 イベントが複数の月または年にまたがっている場合、イベントは月ごとに1つずつ、複数のブロックに分割されます。 公開範囲に一時的なイベントがない場合は、このプロパティと**PR_SCHDINFO_MONTHS_TENTATIVE**を設定したり、既に存在する場合は削除したりする必要があります。 それ以外の場合は、このプロパティを設定する必要があります。 
  
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

