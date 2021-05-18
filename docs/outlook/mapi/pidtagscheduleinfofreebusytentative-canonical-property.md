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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359775"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>PidTagScheduleInfoFreeBusyTentative 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
空き時間情報の状態が暫定的な時間のブロックを含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|識別子:  <br/> |0x6852  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値の数は、PR_SCHDINFO_MONTHS_TENTATIVE **(** [PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) です。 各バイナリ値は月を表し、同じインデックスの値に **対応** PR_SCHDINFO_MONTHS_TENTATIVE。 バイナリ値は、バイナリの値と同じ順序で並 **べPR_SCHDINFO_MONTHS_TENTATIVE。**
  
各バイナリ値には 1 つ以上の 4 バイト ブロックが含まれます。各ブロックには、最初の 2 バイトの開始時刻と、2 番目の 2 バイトの終了時刻がリトル エンド形式で含まれます。 開始時刻は、月の最初の日の午前 0 時の協定世界時 (UTC) から UTC でのイベントの開始時刻の間の分数です。 終了時刻は、月の最初の日の午前 0 時 UTC から UTC でのイベントの終了時刻の間の分数です。 4 バイト ブロックは昇順に並べ替えます。
  
連続または重複する時間ブロックは、最初のブロックの開始時刻として開始時刻を、最後のブロックの終了時刻として終了時刻として 1 つのブロックに結合されます。 イベントが複数の月または年にまたがっている場合、イベントは月ごとに 1 つ、複数のブロックに分割されます。 発行範囲に仮イベントがない場合は、このプロパティと PR_SCHDINFO_MONTHS_TENTATIVE を設定しないか、既に存在する場合は削除する必要があります。 それ以外の場合は、このプロパティを設定する必要があります。 
  
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

