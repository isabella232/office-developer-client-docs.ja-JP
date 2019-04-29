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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438569"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるリストを表します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> リストから水平または垂直スクロールバーを削除するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NO_HBAR 
  
> リストに水平スクロールバーを表示する必要はありません。
    
MAPI_NO_VBAR 
  
> リストに垂直スクロールバーを表示する必要はありません。
    
 **ulprsetproperty**
  
> 任意の型のプロパティのプロパティタグ。 このプロパティは、 **ulprtabletable**メンバーで識別されるテーブルの列の1つです。 
    
 **ulprtablename**
  
> **openproperty**呼び出しを使用して開くことができる PT_OBJECT 型のテーブルプロパティのプロパティタグ。 表に含める必要のある列の数は、リストが単一または複数の選択リストであるかによって決まります。 **ulprsetproperty**メンバーが**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定されている場合、リストは複数の項目を選択できます。
    
## <a name="remarks"></a>注釈

**dtbllbx**構造体は、複数のアイテムを表示するために使用されるコントロールのリストを記述し、ユーザーが1つ以上のアイテムを選択できるようにします。 
  
**ulprsetproperty**メンバーと**ulprsetproperty**メンバーは連携して動作します。テーブルから1つの値が選択されている場合、ダイアログボックスが閉じられたときに**ulprsetproperty**に書き戻されます。 
  
flags 値は、水平または垂直のスクロールバーを一覧と共に表示するかどうかを示します。 既定では、必要に応じてスクロールバーの種類を表示します。 サービスプロバイダーは、MAPI_NO_HBAR を設定して、水平スクロールバーと MAPI_NO_VBAR を非表示にし、垂直スクロールバーを非表示にすることができます。 
  
2つのプロパティタグメンバーは連携してリスト内の値を表示し、リスト内の項目が選択されたときに対応するプロパティを設定します。 MAPI が最初にリストを表示するときは、 **imapiprop**実装の**openproperty**メソッドを呼び出して、 **ulprtablename**メンバーで識別されたテーブルを取得します。 テーブル内の列数は、 **ulprsetproperty**メンバーの値に応じて異なります。 **ulprsetproperty**が**PR_NULL**に設定されている場合、リストは、アドレス帳コンテナー、メッセージの受信者テーブル、配布リストのコンテンツテーブルなど、受信者を含むオブジェクトに基づいて複数の選択リストになります。 
  
複数選択リストのテーブルには、次の列が含まれている必要があります。
  
 **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) およびその他の最大5つの複数値文字列プロパティを、3つの必須列と共に表示することもできます。 
  
**ulprsetproperty**メンバーが**PR_NULL**に設定されていない場合、リストは単一の選択一覧になります。 **ulprsetproperty**の初期値は、最初に選択された行を決定します。 ユーザーがいずれかの行を選択すると、 **ulprsetproperty**メンバーが選択された値に設定され、この値は、 [imapiprop:: setprops](imapiprop-setprops.md)を呼び出すことでプロパティインターフェイスの実装に書き戻されます。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

