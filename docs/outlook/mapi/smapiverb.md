---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309486"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI の動詞を記述します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a>Members

 **lverb**
  
> imapiform に渡される動詞を表すコード[::D overb](imapiform-doverb.md) 標準動詞は、ヘッダーファイルの exchform .h で定義されています。
    
 **szVerbname**
  
> フォームメニューに表示される動詞の表示名。
    
 **futex フラグ**
  
> 動詞のフラグです。
    
 **grfAttribs**
  
> 動詞の属性。 
    
 **ulFlags**
  
> 動詞の表示名の形式を示すフラグです。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 表示名は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、表示名は ANSI 形式になります。
    
## <a name="remarks"></a>解説

**smapiverb**構造体は、次のメソッドのパラメーターとして渡されます。 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[CbMessageClassArray](cbmessageclassarray.md)


[MAPI の構造](mapi-structures.md)

