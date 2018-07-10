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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2db95697cd98e66da9fb3d0cd0180b238c0a8dff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799971"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**適用されます**: Outlook 
  
ダイアログ ボックスが表示テーブルの構築に使用するドロップダウン リスト コントロールについて説明します。
  
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
  
> 予約済み、0 でなければなりません。 
    
 **ulPRDisplayProperty**
  
> 型 PT_TSTRING のプロパティのプロパティ タグです。 このプロパティは、 **ulPRTableName**のメンバーで識別されるテーブル内の列のいずれかです。 このプロパティの値は、一覧に表示されます。 
    
 **ulPRSetProperty**
  
> 任意の型のプロパティのプロパティ タグです。 このプロパティは、 **ulPRTableName**のメンバーで識別されるテーブル内の列のいずれかです。 **UlPRTableName**メンバーで識別されるテーブルの行から**ulPRDisplayProperty**のメンバーのリストのユーザーがプロパティの値を選択すると、対応する**ulPRSetProperty**のメンバーが設定されます。 
    
 **ulPRTableName**
  
> PT_OBJECT、 **OpenProperty**を使用して開くことができる種類のテーブルのプロパティのプロパティ タグを呼び出します。 テーブルが 2 つの列を持つ必要があります: **ulPRDisplayProperty**と**ulPRSetProperty**。 テーブルの行は、リスト内の項目に対応します。
    
## <a name="remarks"></a>備考

**DTBLDDLBX**構造体では、展開するまでに、1 つの項目として表示されているドロップダウン リスト コントロールについて説明します。 
  
プロパティ タグで識別される 3 つのプロパティが連携する情報が一覧に表示し、関連するプロパティを設定します。 **UlPRTableName**メンバーは、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出すことによってアクセスされているテーブル オブジェクトです。 テーブルには 2 つの列: **ulPRDisplayProperty**メンバーと**ulPRSetProperty**のメンバーによって識別されるプロパティによって識別されるプロパティの 1 つの列です。 
  
**UlPRDisplayProperty**プロパティは、リストの表示をドライブします。 ユーザーは、表示値のいずれかを選択すると、MAPI は、 **ulPRSetProperty**のメンバーで識別される、対応するプロパティを設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出します。 つまり、選択した表示のプロパティとして同じ行のプロパティです。 **UlPRSetProperty**メンバーは、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定できません。
  
初期値は、MAPI が[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すことによって**ulPRSetProperty**のメンバーによって表されるプロパティを取得し、 **ulPRSetProperty**メンバーの値を持つテーブルの行を配置する場合、一覧に表示されます。 最初に表示される値は、 **ulPRDisplayProperty** 、 **ulPRDisplayProperty**構造体のメンバーのプロパティに一致する行をその列の内容です。 リストが最初に表示されるときに表示される初期値を**GetProps** **ulPRDisplayProperty**メンバーで識別されるプロパティの戻り値になります。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。 プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[MAPI の構造](mapi-structures.md)
  
[表示テーブルの実装](display-table-implementation.md)
  
[テーブルを表示します。](display-tables.md)
  
[MAPI プロパティの型の概要](mapi-property-type-overview.md)
