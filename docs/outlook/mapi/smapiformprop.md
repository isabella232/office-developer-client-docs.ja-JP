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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 73475c5ee4e715796e06642756c05746b271d128
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803946"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**適用されます**: Outlook 
  
フォームで使用される名前付きプロパティをについて説明します。 
  
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
  
> **SMAPIFormProp**構造体の文字列の形式を識別するために使用するフラグ。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式では。 MAPI_UNICODE が設定されていない場合は、ANSI 形式の文字列です。
    
 **nPropType**
  
> 0 に設定する最も重要な単語を名前付きプロパティの型。 
    
 **nmid**
  
> インターフェイス識別子およびフォーム名を表すプロパティ セットが、数値または文字列の値を識別する**GUID**構造体を含む名前付きプロパティの名前です。 
    
 **pszDisplayName**
  
> 名前付きプロパティの表示名へのポインター。
    
 **nSpecialType**
  
> **U**メンバーに含まれるデータの種類を示す数値です。 使用可能な値は次のとおりです。 
    
FPST_VANILLA 
  
> **U**のメンバーは、列挙体には含まれません。 
    
FPST_ENUM_PROP 
  
> **U**のメンバーには、列挙体を記述する構造体が含まれています。 
    
 **u**
  
> 共用体の名前と、名前付きプロパティの数の間の関連付けを記述します。 いくつかのプロパティを使用すると、空では、 **u**のメンバーです。 他のプロパティでは、次のメンバーで構成される構造体で表されます。 
    
 **nmidIdx**
  
> プロパティ セットと名前付きプロパティの識別子を含む[MAPINAMEID](mapinameid.md)構造体です。 
    
 **cfpevAvailable**
  
> **PfpevAvailable**メンバーが指す配列内の[SMAPIFormPropEnumVal](smapiformpropenumval.md)構造体の数です。 
    
 **pfpevAvailable**
  
> それぞれの名前付きプロパティの値を保持する**SMAPIFormPropEnumVal**構造体の配列へのポインター。 
    
## <a name="remarks"></a>備考

**SMAPIFormProp**構造体には、 [IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスの定義の一部として使用されるフォームのプロパティに関する情報が含まれています。**nSpecialType**には、 **SMAPIFormProp**の一部である**u**の和集合に適用されるタグが含まれています。
  
## <a name="see-also"></a>関連項目



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[MAPI の構造](mapi-structures.md)

