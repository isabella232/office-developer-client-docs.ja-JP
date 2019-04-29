---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430610"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限に注釈を付けるために使用されるコメント制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>メンバー

 **cvalues**
  
> **lpprop**メンバーによって参照されている配列内のプロパティ値の数。 
    
 **lpres**
  
> [srestriction](srestriction.md)構造体へのポインター。 
    
 **lpprop**
  
> [spropvalue](spropvalue.md)構造体の配列へのポインター。それぞれには、プロパティタグと、名前付きプロパティの値が含まれています。 
    
## <a name="remarks"></a>注釈

**sコメント制限**構造は、オブジェクトを一連の名前付きプロパティに関連付けます。 コメント制限は、評価されないため、他の制限とは異なります。 つまり、 [IMAPITable:: Restrict](imapitable-restrict.md)メソッドでは無視されます。 **imapitable:: Restrict**呼び出しが行われた後、 [imapitable:: QueryRows](imapitable-queryrows.md)メソッドによって返される行には影響はありません。 
  
**sコメント制限**構造を使用すると、アプリケーション固有の情報をディスクに保存するときに制限を設定できます。 たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントは、 **sコメント制限**構造でそのようにすることができます。 プロパティの制限でプロパティ名を保存することはできません。これは、関連付けられた[spropertyrestriction](spropertyrestriction.md)構造体には property タグのみが含まれるためです。 
  
詳細については**** 、「制限[につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI の構造](mapi-structures.md)

