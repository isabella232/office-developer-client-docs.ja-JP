---
title: PidTagFollowupIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383521"
---
# <a name="pidtagfollowupicon-canonical-property"></a>PidTagFollowupIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ オブジェクトのフラグの色を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|識別子:  <br/> |0x1095  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージ フォルダーの名前を変更します。  <br/> |
   
## <a name="remarks"></a>備考

**PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) プロパティの設定は"followupFlagged"、またはメッセージは、会議に関連する場合を除き、このプロパティが存在する必要があります。 タスク オブジェクトでこのプロパティが存在する必要があります。 その他のメッセージ オブジェクトに設定すると、このプロパティは、次の値のいずれかに設定する必要があります。
  
|**数値**|**名前**|**説明**|
|:-----|:-----|:-----|
|存在しません。  <br/> |N/A  <br/> |色なし  <br/> |
|1  <br/> |followupIcon1  <br/> |紫フラグ  <br/> |
|2  <br/> |followupIcon2  <br/> |オレンジ フラグ  <br/> |
|3  <br/> |followupIcon3  <br/> |緑色の旗  <br/> |
|4  <br/> |followupIcon4  <br/> |黄フラグ  <br/> |
|5  <br/> |followupIcon5  <br/> |青フラグ  <br/> |
|6  <br/> |followupIcon6  <br/> |赤フラグ  <br/> |
   
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

