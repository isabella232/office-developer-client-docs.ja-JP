---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576317"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ディスプレイ テーブルから作成されたダイアログ ボックスで使用するグループ ボックス コントロールについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> グループ ボックスに付属している文字列のメモリ内の位置。 表示されている場合は、ボックスの上端、左側にあるラベルが表示されます。
    
 **ulFlags**
  
> **UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> ラベルは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。
    
## <a name="remarks"></a>注釈

**DTBLGROUPBOX**構造体では、ダイアログ ボックスで他のコントロールを視覚的に関連付けるために使用される、グループ ボックス コントロールについて説明します。 強調表示の方法は、ボックスで他のコントロールを囲む必要があります。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

