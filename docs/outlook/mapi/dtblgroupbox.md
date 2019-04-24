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
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338662"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるグループボックスコントロールを表します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulblpszlabel**
  
> グループボックスに付属する文字列のメモリ内での位置を指定します。 ラベルが表示されている場合は、ボックスの左上に表示されます。
    
 **ulFlags**
  
> **ulblpszlabel**メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。
    
## <a name="remarks"></a>解説

**dtblgroupbox**構造体は、ダイアログボックス内の他のコントロールを視覚的に関連付けるために使用されるグループボックスコントロールを表します。 強調表示の方法では、他のコントロールをボックスで囲む必要があります。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

