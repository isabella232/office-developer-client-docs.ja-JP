---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406326"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイルまたは受信者テーブルの行をフィルター処理するために使用されるサブオブジェクト制限について説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>メンバー

 **ulsubobject の**
  
> 制限のターゲットとして機能するサブオブジェクトの種類。 可能な値は次のとおりです。 
    
PR_MESSAGE_RECIPIENTS 
  
> メッセージの受信者テーブルに制限を適用します。 
    
PR_MESSAGE_ATTACHMENTS 
  
>  メッセージの添付ファイルテーブルに制限を適用します。 
    
 **lpres**
  
> [srestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

サブオブジェクトの制限は、すべてのテーブルでサポートされているわけではありません。 通常、フォルダーの内容のテーブルと検索結果のフォルダーのみがサポートしています。 たとえば、サブオブジェクトの制限を使用して、特定の種類の添付ファイルまたは受信者を持つメッセージを検索します。 
  
実装がサブオブジェクトの制限をサポートしていない場合は、 [IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)メソッドから MAPI_E_TOO_COMPLEX を返します。 
  
制限のしくみについての一般的な説明については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

