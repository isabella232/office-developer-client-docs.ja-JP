---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436833"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるチェック ボックスに関する情報が含まれる。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> チェック ボックスと一緒に表示される文字列のメモリ内の位置。 
    
 **ulFlags**
  
> チェック ボックス ラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulPRPropertyName**
  
> 型のプロパティのプロパティ タグPT_BOOLEAN。 このプロパティの値は、チェック ボックスの状態の影響を受けます。
    
## <a name="remarks"></a>注釈

**DTBLCHECKBOX** 構造体は、有効 (チェック ボックス) または無効 (空のボックス) の 2 つの状態のいずれかを反映するコントロールのチェック ボックスを表します。 
  
**ulPRPropertyName** メンバーは、チェック ボックスの状態を変更することによって値が操作されるブール型 (Boolean) のプロパティを表します。 チェック ボックスが最初に表示される場合、MAPI は、表示テーブルに関連付けられている **IMAPIProp** 実装の **GetProps** メソッドを呼び出して、一連の既定のプロパティを取得します。 プロパティの 1 つが **DTBLCHECKBOX** 構造体のプロパティ タグにマップされている場合、そのプロパティの値がチェック ボックスの初期値として表示されます。 
  
チェック ボックス コントロールは変更可能です。 これにより、ユーザーは状態を変更できます。 変更可能なチェック ボックスは [、DTCTL](dtctl.md)構造の **ulCtlFlags** メンバーおよび PR_CONTROL_FLAGS ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに **DT_EDITABLE** フラグを設定します。 チェック ボックスの状態が変更されると、MAPI は [IMAPIProp::SetProps](imapiprop-setprops.md) を呼び出して **、DTBLCHECKBOX** 構造体のプロパティ タグ メンバーで識別されるプロパティを新しい状態に設定します。 
  
**たとえば、アドレス** 帳プロバイダーの構成ダイアログ ボックスに変更可能なチェック ボックス コントロールを含め、受信者の PR_SEND_RICH_INFO ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティの設定を調整できます。 ユーザーがチェック ボックスをオンにすると、MAPI は、このプロパティを TRUE に設定します。 チェック ボックスがオフの場合、プロパティは FALSE に設定されます。
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。 プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

