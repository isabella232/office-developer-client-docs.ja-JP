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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799964"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**適用対象**: Outlook 
  
ダイアログ ボックスが表示テーブルの構築に使用するチェック ボックスに関する情報が含まれています。 
  
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
  
> チェック ボックスが表示されている文字の文字列のメモリ内の位置。 
    
 **ulFlags**
  
> チェック ボックスのラベルの書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> ラベルは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。
    
 **ulPRPropertyName**
  
> 型 PT_BOOLEAN のプロパティのプロパティ タグです。 このプロパティの値は、チェック ボックスの状態の影響を受けます。
    
## <a name="remarks"></a>注釈

**DTBLCHECKBOX**構造体が 2 つの状態を反映するコントロールのチェック ボックスを示します: (チェック ボックス) を有効になっているか、(空のボックス) を無効にします。 
  
**UlPRPropertyName**メンバーは、ブール型のプロパティ値は、チェック ボックスの状態を変更することで操作を説明します。 チェック ボックスが最初に表示されると、MAPI は、既定のプロパティのセットを取得するために表示された表に関連付けられている**IMAPIProp**実装の**GetProps**メソッドを呼び出します。 **DTBLCHECKBOX**構造体のプロパティ タグのプロパティのいずれかのマップ、そのプロパティの値がチェック ボックスの初期値として表示されます。 
  
チェック ボックス コントロールは、変更可能なことができます。 これにより、ユーザーの状態を変更します。 変更可能] チェック ボックスは、 **ulCtlFlags** 、 [DTCTL](dtctl.md)構造体のメンバーでは、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) のプロパティに DT_EDITABLE フラグを設定します。 チェック ボックスの状態が変更されるとき、MAPI は、プロパティ タグの**DTBLCHECKBOX**構造体のメンバーを新しい状態で識別されるプロパティを設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出します。 
  
たとえば、アドレス帳プロバイダーと、受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティの設定を調整するのには、[構成] ダイアログ ボックスで、変更可能なチェック ボックス コントロール場合があります。 ユーザーは、チェック ボックスを選択すると、MAPI はこのプロパティを TRUE に設定します。 チェック ボックスが選択されているプロパティが FALSE に設定します。
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。 プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

