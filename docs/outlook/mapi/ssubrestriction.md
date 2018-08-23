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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 152f3032876d6473f1716afa46507196cd5ecc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804001"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**適用対象**: Outlook 
  
メッセージの添付ファイルや受信者テーブルの行をフィルター処理に使用されるサブ オブジェクトの制限について説明します。
  
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
  
> 制限の対象となる下位のオブジェクトの種類です。 使用可能な値は次のとおりです。 
    
PR_MESSAGE_RECIPIENTS 
  
> メッセージの受信者テーブルに制限を適用します。 
    
PR_MESSAGE_ATTACHMENTS 
  
>  メッセージの添付ファイル テーブルに制限を適用します。 
    
 **lpRes**
  
> [SRestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

サブ オブジェクトの制限事項は、すべてのテーブルではサポートされていません。 通常、だけフォルダーの内容をテーブルと、検索結果のフォルダーでは、それらをサポートします。 などの特定の種類の添付ファイル、または受信者がメッセージを検索するのには下位のオブジェクトの制限が使用されます。 
  
実装が下位のオブジェクトの制限をサポートしていない場合、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドまたは[IMAPITable::FindRow](imapitable-findrow.md)メソッドから MAPI_E_TOO_COMPLEX を返します。 
  
制限のしくみの概要については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

