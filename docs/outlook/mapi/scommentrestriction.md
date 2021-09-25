---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dbc4de78db26d2e93d34feb5f5846c69a942ce5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609433"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限に注釈を付けるコメント制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>メンバー

 **cValues**
  
> **lpProp** メンバーが指す配列内のプロパティ値の数。 
    
 **lpRes**
  
> [SRestriction](srestriction.md)構造体へのポインター。 
    
 **lpProp**
  
> 名前付きプロパティのプロパティ タグと値を含む [SPropValue](spropvalue.md) 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SCommentRestriction 構造体は**、オブジェクトを名前付きプロパティのセットと関連付ける。 コメントの制限は、評価されないので、他の制限とは異なっています。 つまり [、IMAPITable::Restrict メソッドでは無視](imapitable-restrict.md) されます。 IMAPITable::Restrict 呼び出しが行われた後[、IMAPITable::QueryRows](imapitable-queryrows.md)メソッドによって返される行には影響しません。  
  
**SCommentRestriction 構造** を使用すると、アプリケーション固有の情報をディスクに保存するときに制限を付け続けることができます。 たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントは **、SCommentRestriction** 構造で使用できます。 関連付けられた [SPropertyRestriction](spropertyrestriction.md) 構造体にはプロパティ タグしか保持されないので、プロパティの制限ではプロパティ名を保存できない。 
  
**SCommentRestriction** 構造と制限全般の詳細については、「制限について」[を参照してください](about-restrictions.md)。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI の構造](mapi-structures.md)

