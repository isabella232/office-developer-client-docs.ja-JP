---
title: PidTagFlagStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390556"
---
# <a name="pidtagflagstatus-canonical-property"></a>PidTagFlagStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ オブジェクトのフラグの状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FLAG_STATUS  <br/> |
|識別子:  <br/> |0x1090  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、会議に関連するオブジェクトに存在する必要があり、task オブジェクト上に存在する必要があります。 他のメッセージ オブジェクトに設定すると、このプロパティは、次の値のいずれかに設定する必要があります。
  
|**数値**|**名前**|**説明**|
|:-----|:-----|:-----|
|存在しません。  <br/> |N/A  <br/> |フラグなし  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |完了のフラグを設定  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Flagged  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
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

