---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438849"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるドロップダウンリストコントロールについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> 予約済み。0である必要があります。 
    
 **ulprdisplayproperty**
  
> PT_TSTRING 型のプロパティのプロパティタグ。 このプロパティは、 **ulprtablename**メンバーによって識別されるテーブルの列の1つです。 このプロパティの値は、一覧に表示されます。 
    
 **ulprsetproperty**
  
> 任意の型のプロパティのプロパティタグ。 このプロパティは、 **ulprtablename**メンバーによって識別されるテーブルの列の1つです。 リストのユーザーが ulprtablename メンバーによって識別されるテーブルの行から**ulprdisplayproperty**メンバーのプロパティ値**** を選択すると、対応する**ulprsetproperty**メンバーが設定されます。 
    
 **ulprtablename**
  
> **openproperty**呼び出しを使用して開くことができる PT_OBJECT 型のテーブルプロパティのプロパティタグ。 このテーブルには2つの列を指定する必要があります。 **ulprdisplayproperty**および**ulprsetproperty**。 表の行は、リスト内の項目に対応している必要があります。
    
## <a name="remarks"></a>注釈

**dtblddlbx**構造体は、ユーザーがそれを展開することになるまで、1つのアイテムとして表示されるドロップダウンリストコントロールについて説明します。 
  
プロパティタグによって識別される3つのプロパティが連携して、リスト内の情報を表示し、関連するプロパティを設定します。 **ulprtablename**メンバーは、 [imapiprop:: openproperty](imapiprop-openproperty.md)への呼び出しによってアクセスされる table オブジェクトです。 このテーブルには2つの列があります。 **ulprdisplayproperty**メンバーによって識別されるプロパティの1つの列と、 **ulprsetproperty**メンバーによって識別されるプロパティの列は1つです。 
  
**ulprdisplayproperty**プロパティは、リスト表示を駆動します。 ユーザーが表示から値の1つを選択すると、MAPI は[imapiprop:: setprops](imapiprop-setprops.md)を呼び出して、 **ulprsetproperty**メンバーによって識別される対応するプロパティを設定します。 これは、プロパティが選択した表示プロパティと同じ行にあることを意味します。 **ulprsetproperty**メンバーを**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定することはできません。
  
MAPI が、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して**ulprsetproperty**メンバーによって表されるプロパティを取得し、テーブルの行に**ulprsetproperty**メンバーの値を格納している場合は、リストに初期値が表示されます。 最初に表示される値は、構造体の**ulprdisplayproperty**メンバーのプロパティに一致する行からの**ulprdisplayproperty**列の内容です。 **ulprdisplayproperty**メンバーによって識別されるプロパティの**GetProps**によって返される値は、リストが最初に表示されたときに表示される初期値になります。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。 プロパティの種類の詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI の構造](mapi-structures.md)
  
[表示テーブルの実装](display-table-implementation.md)
  
[表の表示](display-tables.md)
  
[MAPI プロパティの種類の概要](mapi-property-type-overview.md)

