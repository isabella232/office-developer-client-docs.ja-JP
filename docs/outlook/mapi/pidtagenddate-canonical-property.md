---
title: PidTagEndDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382716"
---
# <a name="pidtagenddate-canonical-property"></a>PidTagEndDate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
終了日と終了スケジュールのアプリケーションによって管理されるように予定の時間が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_END_DATE  <br/> |
|識別子:  <br/> |0x0061  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

アプリケーションをスケジュール設定必要があります ([PidTagStartDate](pidtagstartdate-canonical-property.md))、**単に PR_START_DATE**およびこのプロパティの両方の会議出席依頼を送信するときです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
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

