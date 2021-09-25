---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 69bf149f4d70c34212ecea4c0ea4c55f25d0fc2a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578593"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームで使用される名前付きプロパティについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
   
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
  
> **SMAPIFormProp** 構造体の文字列の形式を区別するために使用されるフラグ。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このMAPI_UNICODE設定されていない場合、文字列は ANSI 形式です。
    
 **nPropType**
  
> 最も重要な単語が 0 に設定された名前付きプロパティの種類。 
    
 **nmid**
  
> プロパティ セットを識別する **GUID** 構造と、インターフェイス識別子とフォーム名を表す数値または文字列値を含む、名前付きプロパティの名前。 
    
 **pszDisplayName**
  
> 名前付きプロパティの表示名へのポインター。
    
 **nSpecialType**
  
> u メンバーに含まれるデータの種類を表す **値** 。 指定できる値は次のとおりです。 
    
FPST_VANILLA 
  
> **u メンバー** には列挙体が含めではありません。 
    
FPST_ENUM_PROP 
  
> **u メンバー** には、列挙を記述する構造が含まれる。 
    
 **u**
  
> 名前付きプロパティの名前と番号の関連付けを表す共用体。 一部のプロパティを使用すると **、u** メンバーは空になります。 他のプロパティでは、次のメンバーで構成される構造で表されます。 
    
 **nmidIdx**
  
> 名前付 [きプロパティの](mapinameid.md) プロパティ セットと識別子を含む MAPINAMEID 構造体。 
    
 **cfpevAvailable**
  
> pfpevAvailable メンバーが指す配列内の [SMAPIFormPropEnumVal](smapiformpropenumval.md) **構造体の** 数。 
    
 **pfpevAvailable**
  
> **SMAPIFormPropEnumVal** 構造体の配列へのポインターで、それぞれ名前付きプロパティの値を保持します。 
    
## <a name="remarks"></a>注釈

**SMAPIFormProp** 構造体には [、IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスの定義の一部として使用されるフォーム プロパティに関する情報が含まれる。**nSpecialType** には **、SMAPIFormProp** の一部である **u** 共用体に適用されるタグが含まれる。
  
## <a name="see-also"></a>関連項目



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI の構造](mapi-structures.md)

