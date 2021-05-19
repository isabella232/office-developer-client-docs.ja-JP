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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410960"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 動詞について説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
   
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

 **lVerb**
  
> [IMAPIForm::D oVerb](imapiform-doverb.md)に渡される動詞を表すコードです。 標準動詞は、ヘッダー ファイル Exchform.h で定義されます。
    
 **szVerbname**
  
> フォーム メニューに表示される動詞の名前を表示します。
    
 **fuFlags**
  
> 動詞のフラグ。
    
 **grfAttribs**
  
> 動詞の属性。 
    
 **ulFlags**
  
> 動詞の表示名の形式を示すフラグを設定します。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 表示名は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、表示名は ANSI 形式になります。
    
## <a name="remarks"></a>注釈

**SMAPIVerb 構造体** は、次のメソッドでパラメーターとして渡されます。 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[CbMessageClassArray](cbmessageclassarray.md)


[MAPI の構造](mapi-structures.md)

