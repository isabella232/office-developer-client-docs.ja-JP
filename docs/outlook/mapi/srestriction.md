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
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803998"
---
# <a name="srestriction"></a>SRestriction

  
  
**適用対象**: Outlook 
  
特定の行をテーブルの表示を制限するフィルターについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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
  
> 制限の種類です。 使用可能な値は次のとおりです。 
    
RES_AND 
  
> ビットごとの**AND**演算が適用される制限**と**制限します。 
    
RES_BITMASK 
  
> ビットマスク制限ビットマスク プロパティの値が適用されます。
    
RES_COMMENT 
  
> コメント制限、制限付きのコメントを関連付けます。
    
RES_COMPAREPROPS 
  
> 2 つのプロパティ値を比較する、プロパティの比較制限です。
    
RES_CONTENT 
  
> コンテンツ制限、特定のコンテンツのプロパティ値を検索します。
    
RES_EXIST 
  
> プロパティがサポートされているかどうかを決定する既存の制限します。
    
RES_NOT 
  
> **しない**制限、制約を論理**NOT**演算を適用します。 
    
RES_OR 
  
> **または**制限、制約を論理**OR**演算が適用されます。 
    
RES_PROPERTY 
  
> プロパティ制限プロパティの値が特定の値と一致するかどうかを決定します。
    
RES_SIZE 
  
> サイズの制限、プロパティの値が特定のサイズであるかどうかを決定します。
    
RES_SUBRESTRICTION 
  
> サブ オブジェクト制限メッセージの添付ファイル、または受信者に制限を適用します。
    
 **res**
  
> 制限構造のフィルターを記述するのに適用する共用体です。 **Res**のメンバーに含まれている特定の構造は、 **rt**のメンバーの値によって異なります。 制限の種類と構造間のマッピングは、次の表に表示されます。 
    
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
   
## <a name="remarks"></a>注釈

クライアントは、数とそれぞれのテーブルのビュー内の行の種類を制限して、フォルダー内の特定のメッセージを検索するに**SRestriction**構造体を使用します。 テーブルの制限を適用するには、クライアントは、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)のいずれかを呼び出します。 フォルダーの制限を課すには、クライアントは、フォルダーの[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出します。 
  
テーブルの制限を使用する方法の詳細については、[制限の詳細](about-restrictions.md)を参照してください。 
  
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

