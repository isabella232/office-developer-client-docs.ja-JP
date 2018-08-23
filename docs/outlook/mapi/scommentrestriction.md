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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589183"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
制限の注釈を付けるためには、コメントの制限について説明します。 
  
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

## <a name="members"></a>Members

 **あう**
  
> **LpProp**メンバーが指す配列内のプロパティ値の数です。 
    
 **lpRes**
  
> [SRestriction](srestriction.md)構造体へのポインター。 
    
 **lpProp**
  
> プロパティ タグと名前付きプロパティの値をそれぞれ含む[SPropValue](spropvalue.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SCommentRestriction**構造体は、一連の名前付きプロパティとオブジェクトを関連付けます。 コメントの制限は他の制限とは異なりは評価されません。 [IMAPITable::Restrict](imapitable-restrict.md)メソッドによって、それらは無視されます。 **IMAPITable::Restrict**の呼び出しが行われた後に、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドによって返された行には影響はありません。 
  
ディスクに保存するときに、制限のあるアプリケーション固有の情報を保持する**SCommentRestriction**構造体を使用できます。 たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントことができますでこれを**SCommentRestriction**構造体。 プロパティ タグのみが関連する[SPropertyRestriction](spropertyrestriction.md)構造体に格納されているために、プロパティの名前を保存するプロパティの制限のことはできません。 
  
**SCommentRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[MAPI の構造](mapi-structures.md)

