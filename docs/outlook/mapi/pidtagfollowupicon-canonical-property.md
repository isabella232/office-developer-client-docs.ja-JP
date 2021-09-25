---
title: PidTagFollowupIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8fb1a570f2bad075c69a9328427de53e86fab938
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563554"
---
# <a name="pidtagfollowupicon-canonical-property"></a>PidTagFollowupIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ オブジェクトのフラグの色を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|識別子:  <br/> |0x1095  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージ フォルダーの名前を変更する  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは **、PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) プロパティの値が "followupFlagged" に設定されている場合、またはメッセージ オブジェクトが会議関連オブジェクトである場合を指定しない限り、存在していなければなりません。 このプロパティは、タスク オブジェクトには存在しません。 他のメッセージ オブジェクトに設定する場合、このプロパティは次のいずれかの値に設定する必要があります。
  
|**数値**|**名前**|**説明**|
|:-----|:-----|:-----|
|存在しない  <br/> |該当なし  <br/> |色なし  <br/> |
|1  <br/> |followupIcon1  <br/> |紫色のフラグ  <br/> |
|2  <br/> |followupIcon2  <br/> |オレンジ 色のフラグ  <br/> |
|3  <br/> |followupIcon3  <br/> |緑のフラグ  <br/> |
|4   <br/> |followupIcon4  <br/> |黄色のフラグ  <br/> |
|5  <br/> |followupIcon5  <br/> |青いフラグ  <br/> |
|6   <br/> |followupIcon6  <br/> |赤いフラグ  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
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

