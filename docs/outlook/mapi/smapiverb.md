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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803976"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**適用されます**: Outlook 
  
MAPI 動詞をについて説明します。
  
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
  
> [IMAPIForm::DoVerb](imapiform-doverb.md)に渡される動詞を表すコードです。 標準動詞は、Exchform.h ヘッダー ファイルで定義されます。
    
 **szVerbname**
  
> フォーム] メニューに表示される動詞の名前を表示します。
    
 **fuFlags**
  
> 動詞のフラグです。
    
 **grfAttribs**
  
> 動詞の属性。 
    
 **ulFlags**
  
> 動詞の表示名の形式を示すフラグを設定します。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 表示名は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の表示名です。
    
## <a name="remarks"></a>備考

**SMAPIVerb**構造体は、次のメソッドのパラメーターとして渡されます。 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[CbMessageClassArray](cbmessageclassarray.md)


[MAPI の構造](mapi-structures.md)

