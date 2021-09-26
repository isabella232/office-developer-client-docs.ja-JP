---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68c77f60abdb00a9df4aed4afd60401bad239756
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629565"
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

## <a name="members"></a>メンバー

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

