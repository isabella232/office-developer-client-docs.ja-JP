---
title: PidTagScheduleInfoFreeBusyTentative の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a00505b765abdcb7b8fe9d68052774b30bbdf692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803480"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>PidTagScheduleInfoFreeBusyTentative の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
空き/予約済み状態の仮の予定の時間のブロックが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|識別子:  <br/> |0x6852  <br/> |
|データを入力します。  <br/> |PT_MV_BINARY  <br/> |
|領域:  <br/> |空き/予約済み  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) の値の数だけの値を持ちます。 各バイナリ値は、1 か月を表し、 **PR_SCHDINFO_MONTHS_TENTATIVE**で同じインデックス位置の値に対応します。 バイナリ値は、 **PR_SCHDINFO_MONTHS_TENTATIVE**の値と同じ順序に並べ替えられます。
  
バイナリの値ごとに 1 つまたは複数の 4 バイトのブロックと、それぞれは、最初の 2 バイトの開始時刻と終了時刻をリトル エンディアン形式で 2 番目の 2 バイトで含まれています。 開始時刻は、午前 0 時、月の最初の日の世界協定時刻 (UTC) と UTC でのイベントの開始時刻との間の分の数です。 終了時刻は、UTC、月の最初の日の午前 0 時と終了時刻 (utc) イベントの間隔を分単位の数です。 4 バイトのブロックは、昇順に並べ替えられます。
  
連続または重複する時間帯は、ブロックの最初と最後のブロックの終了時刻と終了時刻の開始時刻と開始時刻を 1 つのブロックにマージされます。 イベントは、複数の月または年の間で分散が場合、は、イベントが 1 か月のいずれか、複数のブロックに分割されます。 公開の範囲内に仮の予定のイベントがない場合は、し、このプロパティは、 **PR_SCHDINFO_MONTHS_TENTATIVE**設定する必要がないまたは既に存在する場合に削除する必要があります。 それ以外の場合、このプロパティを設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの可用性を発行します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

