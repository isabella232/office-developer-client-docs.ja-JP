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
  
表示テーブルから作成されたダイアログ ボックスで使用されるドロップダウン リスト コントロールについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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
  
> 予約済みで、ゼロである必要があります。 
    
 **ulPRDisplayProperty**
  
> 型のプロパティのプロパティ タグPT_TSTRING。 このプロパティは、ulPRTableName メンバーによって識別されるテーブル **内の列の 1** つです。 このプロパティの値が一覧に表示されます。 
    
 **ulPRSetProperty**
  
> 任意の種類のプロパティのプロパティ タグ。 このプロパティは、ulPRTableName メンバーによって識別されるテーブル **内の列の 1** つです。 リストのユーザーが **ulPRTableName** メンバーによって識別される表の行から **ulPRDisplayProperty** メンバーのプロパティ値を選択すると、対応する **ulPRSetProperty** メンバーが設定されます。 
    
 **ulPRTableName**
  
> **OpenProperty** 呼び出しを使用して開くことができるPT_OBJECTのテーブル プロパティのプロパティ タグ。 表には **、ulPRDisplayProperty** と **ulPRSetProperty の 2 つの列が必要です**。 テーブルの行は、リスト内のアイテムに対応する必要があります。
    
## <a name="remarks"></a>注釈

**DTBLDDLBX** 構造体は、ユーザーが展開を選択するまで、1 つのアイテムとして表示されるドロップダウン リスト コントロールを表します。 
  
プロパティ タグで識別される 3 つのプロパティは、一覧に情報を表示し、関連するプロパティを設定するために連携します。 **ulPRTableName** メンバーは [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)の呼び出しを介してアクセスされるテーブル オブジェクトです。 表には **、ulPRDisplayProperty** メンバーによって識別されるプロパティの列と **、ulPRSetProperty** メンバーによって識別されるプロパティの列の 2 つの列があります。 
  
**ulPRDisplayProperty プロパティは**、リスト表示を駆動します。 ユーザーが表示から値の 1 つを選択すると、MAPI は [IMAPIProp::SetProps](imapiprop-setprops.md) を呼び出して、対応するプロパティを **ulPRSetProperty** メンバーによって識別される値として設定します。 これは、選択した表示プロパティと同じ行のプロパティを意味します。 **ulPRSetProperty メンバー** は、PR_NULL **(** [PidTagNull ) に設定できません](pidtagnull-canonical-property.md)。
  
MAPI が [IMAPIProp::GetProps](imapiprop-getprops.md)の呼び出しを通じて **ulPRSetProperty** メンバーによって表されるプロパティを取得し **、ulPRSetProperty** メンバーの値を持つテーブル内の行を見つけた場合、初期値がリストに表示されます。 最初に表示される値は、構造の **ulPRDisplayProperty** メンバーのプロパティに一致する、その行の **ulPRDisplayProperty** 列の内容です。 **ulPRDisplayProperty** メンバーによって識別されるプロパティの **GetProps** によって返される値は、リストが最初に表示されると表示される初期値になります。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。 プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI の構造](mapi-structures.md)
  
[表示テーブルの実装](display-table-implementation.md)
  
[テーブルの表示](display-tables.md)
  
[MAPI プロパティの種類の概要](mapi-property-type-overview.md)

