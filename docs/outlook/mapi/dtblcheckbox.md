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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287270"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるチェックボックスに関する情報を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
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

 **ulblpszlabel**
  
> チェックボックスと共に表示される文字列のメモリ内での位置を指定します。 
    
 **ulFlags**
  
> チェックボックスラベルの書式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulprpropertyname**
  
> PT_BOOLEAN 型のプロパティのプロパティタグ。 このプロパティの値は、チェックボックスの状態によって影響を受けます。
    
## <a name="remarks"></a>解説

**dtblcheckbox**構造体は、2つの状態 (オンボックス) または無効 (空のボックス) のいずれかを反映するコントロールのチェックボックスを記述します。 
  
**ulprpropertyname**メンバーは、チェックボックスの状態を変更することによって値を操作する Boolean プロパティを記述します。 チェックボックスが最初に表示されると、MAPI は、表示テーブルに関連付けられている**imapiprop**実装の**GetProps**メソッドを呼び出して、一連の既定のプロパティを取得します。 プロパティのいずれかが**dtblcheckbox**構造体の property タグにマップされている場合、そのプロパティの値はチェックボックスの初期値として表示されます。 
  
チェックボックスコントロールを変更できます。 これにより、ユーザーは自分の状態を変更できます。 変更可能なチェックボックスでは、 [DTCTL](dtctl.md)構造の**ulCtlFlags**メンバーおよび**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに DT_EDITABLE フラグを設定します。 チェックボックスの状態が変化すると、MAPI は[imapiprop:: setprops](imapiprop-setprops.md)を呼び出して、 **dtblcheckbox**構造のプロパティタグメンバーで識別されたプロパティを新しい状態に設定します。 
  
たとえば、アドレス帳プロバイダーでは、受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティの設定を調整するために、変更可能なチェックボックスコントロールを構成ダイアログボックスに含めることができます。 ユーザーがチェックボックスをオンにすると、MAPI はこのプロパティを TRUE に設定します。 チェックボックスが選択されていない場合、このプロパティは FALSE に設定されます。
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。 プロパティの種類の詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

