---
title: PidTagControlStructure 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c5317bd7b7c423b69333f1ee35a5086c0d7b3646
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563729"
---
# <a name="pidtagcontrolstructure-canonical-property"></a>PidTagControlStructure 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログ ボックスで使用されるコントロールの構造へのポインターを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_STRUCTURE  <br/> |
|識別子:  <br/> |0x3F01  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、コントロール構造の 1 つにキャストされる長いポインターを表します。 コントロール構造には、次のものが含まれます。
  
|||
|:-----|:-----|
|[DTBLBUTTON](dtblbutton.md) <br/> |[DTBLCHECKBOX](dtblcheckbox.md) <br/> |
|[DTBLCOMBOBOX](dtblcombobox.md) <br/> |[DTBLDDLBX](dtblddlbx.md) <br/> |
|[DTBLEDIT](dtbledit.md) <br/> |[DTBLGROUPBOX](dtblgroupbox.md) <br/> |
|[DTBLLABEL](dtbllabel.md) <br/> |[DTBLLBX](dtbllbx.md) <br/> |
|[DTBLMVDDLBOX](dtblmvddlbox.md) <br/> |[DTBLMVLISTBOX](dtblmvlistbox.md) <br/> |
|[DTBLPAGE](dtblpage.md) <br/> |[DTBLRADIOBUTTON](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a>関連リソース

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

