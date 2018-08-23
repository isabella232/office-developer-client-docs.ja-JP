---
title: PidTagFlagCompleteTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e1c2783abd186146fe738a3396e098711893d3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583983"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>PidTagFlagCompleteTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
世界協定世界時 (UTC) メッセージ オブジェクトが完了したものとしてフラグが設定では、日付と時刻を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|識別子:  <br/> |0x1091  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ オブジェクトが完全なフラグが設定されない場合、このプロパティは削除されます。 時間の最小解像度は、(値は 600,000,000 の倍数である必要があります) の分である必要があります。 このプロパティは、オブジェクトでは、会議に関連するオブジェクトおよび task オブジェクト上に存在する必要がある場合に存在する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
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

