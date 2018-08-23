---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569765"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するリストについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Members

 **ulFlags**
  
> リストからの水平方向または垂直方向のスクロール バーを排除するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_NO_HBAR 
  
> 水平スクロール バーは必要があります、ボックスの一覧に表示されません。
    
MAPI_NO_VBAR 
  
> 垂直スクロール バーは必要があります、ボックスの一覧に表示されません。
    
 **ulPRSetProperty**
  
> 任意の型のプロパティのプロパティ タグです。 このプロパティは、 **ulPRTableTable**のメンバーで識別されるテーブル内の列のいずれかです。 
    
 **ulPRTableName**
  
> PT_OBJECT、 **OpenProperty**を使用して開くことができる種類のテーブルのプロパティのプロパティ タグを呼び出します。 テーブルに含める列の数は、リストの 1 つまたは複数選択リストがかどうかによって異なります。 **UlPRSetProperty**メンバーは、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定されている場合は、一覧は、複数選択できます。
    
## <a name="remarks"></a>注釈

**DTBLLBX**構造体では、複数のアイテムを表示して、ユーザーが 1 つまたは複数の項目を選択するようにするために使用されるコントロールの一覧について説明します。 
  
メンバーの**ulPRSetProperty**と**ulPRTableName**のメンバーが連携します。テーブルから 1 つの値を選択すると、それに書き戻さ**ulPRSetProperty** ] ダイアログ ボックスが閉じられるとき。 
  
フラグ値は、水平方向または垂直方向のスクロール バーをリストに表示するかどうを示します。 既定では、スクロール バーが必要な場合を表示の種類が存在します。 サービス プロバイダーには、水平スクロール バーを非表示にする MAPI_NO_HBAR と垂直スクロール バーを非表示にする MAPI_NO_VBAR を設定できます。 
  
2 つのプロパティ タグのメンバーが連携して、ボックスの一覧で値を表示し、リスト内のアイテムを選択すると、対応するプロパティを設定します。 MAPI には、まず、一覧が表示されるとき、に、 **ulPRTableName**メンバーで識別されたテーブルを取得するための**IMAPIProp**実装の**OpenProperty**メソッドを呼び出します。 テーブル内の列の数は、 **ulPRSetProperty**メンバーの値によって異なります。 **UlPRSetProperty**は、 **PR_NULL**に設定されている場合は、受信者、アドレス帳コンテナーである、メッセージの受信者テーブルまたは配布リストの内容のテーブルなどが含まれているオブジェクトを基に複数選択リストは、リスト。 
  
複数選択リストのテーブルには、次の列を含める必要があります。
  
 **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) と、他の 5 つの複数値を持つ文字列プロパティの最大は、3 つの必須の列を表示することもできます。 
  
**UlPRSetProperty**メンバーが**PR_NULL**に設定されていない場合、リスト、単一選択リストです。 **UlPRSetProperty**の初期値は、選択されている最初の行を決定します。 ユーザーは、行のいずれかを選択して**ulPRSetProperty**のメンバーは、選択した値に設定されてこの値が[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出して、プロパティのインターフェイスの実装に書き戻す。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

