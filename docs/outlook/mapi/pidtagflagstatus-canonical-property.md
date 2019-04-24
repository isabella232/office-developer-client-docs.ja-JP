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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316297"
---
# <a name="pidtagflagstatus-canonical-property"></a>PidTagFlagStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
message オブジェクトのフラグの状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FLAG_STATUS  <br/> |
|識別子:  <br/> |0x1090  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、会議関連オブジェクトに存在してはならず、task オブジェクトに存在してはなりません。 他のメッセージオブジェクトに設定されている場合、このプロパティは次のいずれかの値に設定する必要があります。
  
|**数値**|**[名前]**|**[説明]**|
|:-----|:-----|:-----|
|存在しない  <br/> |該当なし  <br/> |なし  <br/> |
|0x00000001  <br/> |手順  <br/> |フラグの完了  <br/> |
|0x00000002  <br/> |このフラグ  <br/> |Flagged  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
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

