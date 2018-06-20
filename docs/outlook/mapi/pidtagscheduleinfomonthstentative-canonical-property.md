---
title: PidTagScheduleInfoMonthsTentative の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803477"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>PidTagScheduleInfoMonthsTentative の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
仮の予定の空き時間情報メッセージにマークされている月が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|識別子:  <br/> |0x6851  <br/> |
|データを入力します。  <br/> |PT_MV_LONG  <br/> |
|領域:  <br/> |空き/予約済み  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値の数が 0 と**PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) と**PR_FREEBUSY_PUBLISH_END の間の期間は、公開の範囲は、対象とする月の数との間にする必要があります。**([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) のプロパティです。
  
このプロパティの各値は、月と年のことでエンコードが。 これは、グレゴリオ暦の年と月を基づく年 × 16 + 月の式を使用して計算されます。 値は昇順で並べ替えられます、リトル エンディアン形式でエンコードされます。 イベントは、複数の月または複数年にわたって分散は、公開の範囲に該当する月の 1 つの値が必要があります。 公開の範囲内に仮の予定のイベントがない場合は、し、このプロパティは、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) 設定する必要がないまたは既に存在する場合に削除する必要があります。 それ以外の場合、このプロパティを設定する必要があります。
  
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

