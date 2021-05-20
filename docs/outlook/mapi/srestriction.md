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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439360"
---
# <a name="srestriction"></a>SRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルのビューを特定の行に制限するフィルターについて説明します。 
  
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
  
> 制限の種類。 指定できる値は次のとおりです。 
    
RES_AND 
  
> **AND 制限**。これは、ビットワイズ **AND** 操作を制限に適用します。 
    
RES_BITMASK 
  
> ビットマスクの制限 。これは、プロパティ値にビットマスクを適用します。
    
RES_COMMENT 
  
> コメントの制限。コメントを制限に関連付ける。
    
RES_COMPAREPROPS 
  
> 2 つのプロパティ値を比較するプロパティ比較の制限。
    
RES_CONTENT 
  
> 特定のコンテンツのプロパティ値を検索するコンテンツ制限。
    
RES_EXIST 
  
> プロパティがサポートされているかどうかを決定する存在制限。
    
RES_NOT 
  
> NOT **制限** 。これは、論理 NOT 操作 **を制限** に適用します。 
    
RES_OR 
  
> 論理 **OR** 操作を制限に適用 **する OR** 制限。 
    
RES_PROPERTY 
  
> プロパティの値が特定の値と一致するかどうかを決定するプロパティ制限。
    
RES_SIZE 
  
> プロパティの値が特定のサイズであるかどうかを決定するサイズ制限。
    
RES_SUBRESTRICTION 
  
> メッセージの添付ファイルまたは受信者に制限を適用するサブオブジェクト制限。
    
 **res**
  
> 適用するフィルターを記述する制限構造の一体。 **res** メンバーに含まれる特定の構造は **、rt** メンバーの値によって異なります。 制限の種類と構造のマッピングを次の表に示します。 
    
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

クライアントは **、SRestriction** 構造を使用して、テーブルのビュー内の行の数と種類を制限し、フォルダー内の特定のメッセージを検索します。 テーブルに制限を適用するには、クライアントは [IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow を呼び出します](imapitable-findrow.md)。 フォルダーに制限を適用するには、クライアントはフォルダーの [IMAPIContainer::SetSearchCriteria メソッドを呼び出](imapicontainer-setsearchcriteria.md) します。 
  
テーブルで制限を使用する方法については、「制限について [」を参照してください](about-restrictions.md)。 
  
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

