---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309500"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームで使用される名前付きプロパティについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> **smapiformprop**構造体の文字列の書式を識別するために使用されるフラグです。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE が設定されていない場合、文字列は ANSI 形式になります。
    
 **nproptype**
  
> 最も重要な単語が0に設定されている、名前付きプロパティの型。 
    
 **nmid**
  
> 名前付きプロパティの名前。プロパティセットを識別する**GUID**構造、およびインターフェイス識別子とフォーム名を表す数値または文字列値のいずれかが含まれます。 
    
 **pszdisplayname**
  
> 名前付きプロパティの表示名へのポインター。
    
 **nの種類**
  
> **u**メンバに含まれるデータの種類を示す値。 可能な値は次のとおりです。 
    
FPST_VANILLA 
  
> **u**メンバに列挙が含まれていません。 
    
FPST_ENUM_PROP 
  
> **u**メンバーには、列挙を記述する構造体が含まれています。 
    
 **u**
  
> 名前と名前付きプロパティの番号の関連付けを説明する共用体。 一部のプロパティを使用すると、 **u**メンバーが空になります。 その他のプロパティの場合は、次のメンバーで構成される構造で表されます。 
    
 **nmidIdx**
  
> 名前付きプロパティのプロパティセットと識別子を含む[mapinameid](mapinameid.md)構造。 
    
 **cfpevavailable**
  
> **pfpevavailable**メンバーによって示されている配列内の[smapiformpropenumval](smapiformpropenumval.md)構造体の数。 
    
 **pfpevavailable**
  
> **smapiformpropenumval**構造体の配列へのポインター。それぞれには、名前付きプロパティの値が格納されています。 
    
## <a name="remarks"></a>解説

**smapiformprop**構造体には、 [imapiforminfo](imapiforminfoimapiprop.md)インターフェイスの定義の一部として使用されるフォームプロパティに関する情報が含まれています。**nの種類**には、 **smapiformprop**の一部である**u**共用体に適用されるタグが含まれています。
  
## <a name="see-also"></a>関連項目



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI の構造](mapi-structures.md)

