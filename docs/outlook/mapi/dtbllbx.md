---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c14f79914619471e864968214e93a51d3e19f9db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588120"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるリストについて説明します。
  
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

## <a name="members"></a>メンバー

 **ulFlags**
  
> リストから水平または垂直のスクロール バーを削除するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NO_HBAR 
  
> リストに水平スクロール バーを表示する必要はありません。
    
MAPI_NO_VBAR 
  
> リストに垂直スクロール バーを表示する必要はありません。
    
 **ulPRSetProperty**
  
> 任意の種類のプロパティのプロパティ タグ。 このプロパティは、ulPRTableTable メンバーによって識別されるテーブル **内の列の 1** つです。 
    
 **ulPRTableName**
  
> **OpenProperty** 呼び出しを使用して開くことができるPT_OBJECTのテーブル プロパティのプロパティ タグ。 テーブルに含む列の数は、リストが 1 つの選択リストか複数選択リストかによって異なります。 **ulPRSetProperty** メンバーが PR_NULL **(** [PidTagNull)](pidtagnull-canonical-property.md)に設定されている場合、リストでは複数の選択が可能です。
    
## <a name="remarks"></a>注釈

**DTBLLBX** 構造は、複数のアイテムを表示し、ユーザーが 1 つ以上のアイテムを選択するために使用するコントロールをリストに記述します。 
  
**ulPRSetProperty メンバーと** **ulPRTableName** メンバーが一緒に動作します。テーブルから 1 つの値を選択すると、ダイアログ ボックスが閉じらば **ulPRSetProperty** に書き戻されます。 
  
flags 値は、水平スクロール バーと垂直スクロール バーをリストと一緒に表示するかどうかを示します。 既定では、必要に応じてスクロール バーの種類が表示されます。 サービス プロバイダーは、水平方向MAPI_NO_HBARを抑制し、垂直スクロール バーを非表示MAPI_NO_VBARを設定できます。 
  
2 つのプロパティ タグ メンバーが連携して、リスト内の値を表示し、リスト内のアイテムが選択されている場合に対応するプロパティを設定します。 MAPI が最初にリストを表示すると **、IMAPIProp 実装** の **OpenProperty** メソッドを呼び出して **、ulPRTableName** メンバーで識別されたテーブルを取得します。 表内の列数は **、ulPRSetProperty** メンバーの値によって異なります。 **ulPRSetProperty** が **PR_NULL** に設定されている場合、リストは、アドレス帳コンテナー、メッセージの受信者テーブル、配布リストのコンテンツ テーブルなど、受信者を含むオブジェクトに基づく複数の選択リストです。 
  
複数の選択リストのテーブルには、次の列が含まれる必要があります。
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) および最大 5 つの他の複数値文字列プロパティを、必要な 3 つの列と一緒に表示することもできます。 
  
**ulPRSetProperty** メンバーが設定されていない場合PR_NULLリストは 1 つの選択リストです。 **ulPRSetProperty の初期値は**、最初に選択した行を決定します。 ユーザーが行のいずれかを選択すると **、ulPRSetProperty** メンバーが選択した値に設定され、この値は [IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出してプロパティ インターフェイスの実装に書き戻されます。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

