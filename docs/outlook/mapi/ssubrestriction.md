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
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Members

 **ulSubObject**
  
> 制限のターゲットとして機能するサブオブジェクトの種類。 指定できる値は次のとおりです。 
    
PR_MESSAGE_RECIPIENTS 
  
> メッセージの受信者テーブルに制限を適用します。 
    
PR_MESSAGE_ATTACHMENTS 
  
>  メッセージの添付ファイル テーブルに制限を適用します。 
    
 **lpRes**
  
> [SRestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

サブオブジェクトの制限は、すべてのテーブルではサポートされていません。 通常、サポートできるのはフォルダー コンテンツ テーブルと検索結果フォルダーのみです。 たとえば、サブオブジェクトの制限は、特定の種類の添付ファイルまたは受信者を持つメッセージを検索するために使用されます。 
  
実装がサブオブジェクト制限をサポートしていない場合は [、IMAPITable::Restrict](imapitable-restrict.md) メソッドまたは [IMAPITable::FindRow](imapitable-findrow.md) メソッドから MAPI_E_TOO_COMPLEX を返します。 
  
制限の動作の一般的な説明については、「 [制限について」を参照してください](about-restrictions.md)。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

