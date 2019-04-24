---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341742"
---
# <a name="srestriction"></a>SRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の行にテーブルのビューを制限するためのフィルターを記述します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a>Members

 **rt**
  
> 制限の種類。 可能な値は次のとおりです。 
    
RES_AND 
  
> or **** 制限。これは、制限にビット単位の**and**演算を適用します。 
    
RES_BITMASK 
  
> ビットマスク制限。これは、プロパティ値にビットマスクを適用します。
    
RES_COMMENT 
  
> コメント制限。コメントを制限に関連付けます。
    
RES_COMPAREPROPS 
  
> 2つのプロパティ値を比較するプロパティ比較制限。
    
RES_CONTENT 
  
> コンテンツ制限。特定のコンテンツのプロパティ値を検索します。
    
RES_EXIST 
  
> プロパティがサポートされているかどうかを判断する、存在する制限。
    
RES_NOT 
  
> 制限を適用**せず**、制限に対する論理**not**演算を適用します。 
    
RES_OR 
  
> **or**制限。これは、制限に対して論理**or**演算を適用します。 
    
RES_PROPERTY 
  
> プロパティの値が特定の値と一致するかどうかを決定するプロパティ制限。
    
RES_SIZE 
  
> サイズ制限。プロパティ値が特定のサイズかどうかを決定します。
    
RES_SUBRESTRICTION 
  
> サブオブジェクト制限。これは、メッセージの添付ファイルまたは受信者に制限を適用します。
    
 **res**
  
> 適用するフィルターを記述する制限構造の和集合。 **res**メンバーに含まれる特定の構造体は、 **rt**メンバーの値に依存します。 次の表に、制限の種類と構造の間のマッピングを示します。 
    
|||
|:-----|:-----|
|**制限の種類** <br/> |**制限構造** <br/> |
|RES_AND  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|RES_BITMASK  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|RES_COMMENT  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|RES_COMPAREPROPS  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|RES_CONTENT  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|RES_EXIST  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|RES_NOT  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|RES_OR  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|RES_PROPERTY  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|RES_SIZE  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|RES_SUBRESTRICTION  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>解説

クライアントは、 **srestriction**構造を使用して、テーブルのビュー内の行の数と種類を制限したり、フォルダー内の特定のメッセージを検索したりします。 テーブルに制限を課すために、クライアントは[IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)を呼び出します。 フォルダーに制限を課すために、クライアントはフォルダーの[IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出します。 
  
テーブルで制限を使用する方法については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SAndRestriction](sandrestriction.md)
  
[SBitMaskRestriction](sbitmaskrestriction.md)
  
[SCommentRestriction](scommentrestriction.md)
  
[SComparePropsRestriction](scomparepropsrestriction.md)
  
[SContentRestriction](scontentrestriction.md)
  
[SExistRestriction](sexistrestriction.md)
  
[SNotRestriction](snotrestriction.md)
  
[SOrRestriction](sorrestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SSizeRestriction](ssizerestriction.md)
  
[SSubRestriction](ssubrestriction.md)


[MAPI の構造](mapi-structures.md)

