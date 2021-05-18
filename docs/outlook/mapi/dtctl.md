---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421502"
---
# <a name="dtctl"></a>DTCTL

**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるコントロールについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>Members

**ulCtlType**
  
> **ctl** メンバーに含まれるコントロールの種類と、コントロールのプロパティ **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) PR_CONTROL_TYPEに対応します。 指定できる値は次のとおりです。
    
DTCT_LABEL 
  
> ラベル コントロール
    
DTCT_EDIT 
  
> コントロールの編集。
    
DTCT_LBX 
  
> リスト ボックス コントロール。
    
DTCT_COMBOBOX 
  
> コンボ ボックス コントロール。
    
DTCT_DDLBX 
  
> ドロップダウン リスト コントロール。
    
DTCT_CHECKBOX 
  
> チェック ボックス コントロール。
    
DTCT_GROUPBOX 
  
> グループ ボックス コントロール。
    
DTCT_BUTTON 
  
> ボタン コントロール。
    
DTCT_PAGE 
  
> タブ付きページ コントロール。
    
DTCT_RADIOBUTTON 
  
> ラジオ ボタン コントロール。
    
DTCT_MVLISTBOX 
  
> 複数値のリスト コントロール。
    
DTCT_MVDDLBX 
  
> 複数値のドロップダウン リスト コントロール。
    
**ulCtlFlags**
  
> コントロールの機能を説明し、コントロールのプロパティ[(PidTagControlFlags)](pidtagcontrolflags-canonical-property.md)プロパティPR_CONTROL_FLAGS対応するフラグのビットマスク。  これらのフラグは、チェック ボックス、コンボ ボックス、リスト ボックス、および編集コントロールにのみ設定できます。 指定できる値は次のとおりです。
    
DT_ACCEPT_DBCS 
  
> ANSI 形式または DBCS 形式のどちらかが受け入れ可能です。 このフラグは、編集コントロールでのみ有効です。
    
DT_EDITABLE 
  
> ユーザーは、コントロール内のテキストを変更できます。 
    
DT_MULTILINE 
  
> コントロールには、複数のテキスト行を含めできます。 このフラグは、編集コントロールでのみ有効です。
    
DT_PASSWORD_EDIT 
  
> コントロールにはパスワードが含まれている。したがって、コントロールの内容をユーザーに表示する必要があります。 このフラグは、編集コントロールでのみ有効です。
    
DT_REQUIRED 
  
> ダイアログ ボックス コントロールが必要です。 このフラグは、編集およびコンボ ボックス コントロールでのみ有効です。
    
DT_SET_IMMEDIATE 
  
> コントロールの変更時に値を即座に出力できます。 これにより、2 つのコントロール間で依存関係を確立できます。 
    
**lpbNotif**
  
> サービス プロバイダーとコントロールの識別子を表す [GUID](guid.md) 構造で構成される構造体へのポインター。 **lpbNotif** メンバーと **cbNotif** メンバーは、コントロールの **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティに対応し、コントロールを更新する必要があるときにユーザー インターフェイスに通知するために使用されます。
    
**cbNotif**
  
> lpbNotif メンバーが指す構造体 **内のバイト数** 。 
    
**lpszFilter**
  
> 編集またはコンボ ボックス コントロールに入力できる文字を表す文字列へのポインター。 他の種類のコントロールでは **、lpszFilter** メンバーを NULL にできます。 編集およびコンボ ボックス コントロールの場合、一度に 1 文字に適用される正規表現である必要があります。 コントロール内のすべての文字に同じフィルターが適用されます。 フィルター文字列の形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> | 任意の文字を使用できます (たとえば `"*"` )。  <br/> |
| `[ ]` <br/> |文字のセットを定義します (たとえば `"[0123456789]"` 、.)  <br/> |
| `-` <br/> |文字の範囲を示します (たとえば `"[a-z]"` )。  <br/> |
| `~` <br/> |これらの文字は使用できません (たとえば `"[~0-9]")` 、 . <br/>|   
| `\` <br/> |前の記号を引用符で囲む場合に使用します (たとえば `"[\-\\\[\]]"` \, 、-、[、] 文字を使用できます)。  <br/> |
   
**ulItemID**
  
> ダイアログ ボックス リソース内のコントロールを識別する値。 タブ付きページ コントロールの場合 **、ulItemID** DTCT_PAGEを使用して、文字列リソースからページのコンポーネント名を読み込む必要があります。 位置とラベルの情報は、ダイアログ ボックス のリソースから読み取ります。 
    
**ctl**
  
> コントロールのデータを保持し、コントロールのプロパティ ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md) **)** プロパティPR_CONTROL_STRUCTURE対応する構造体。 コントロールの種類ごとに構造が異なります。
    
## <a name="remarks"></a>注釈

**DTCTL 構造体は**、任意の種類の 1 つのコントロールを記述します。 ほとんどのメンバーは、コントロールのプロパティを設定するために使用されます。 
  
**ctl メンバー** は、特定の種類のコントロールに関連する構造体の共用体です。 **たとえば、DTCTL** 構造体が編集コントロールを記述している場合 **、ctl** メンバーは [DTBLEDIT 構造体を指](dtbledit.md)します。 この構造体は、コントロールのプロパティに **PR_CONTROL_STRUCTURE** します。 共用体は、DTCTL 構造体のコンパイル時の初期化を可能にするための LPVOID 型の変数を最初の **メンバーとして持** っています。 
  
[BuildDisplayTable](builddisplaytable.md)関数は、コントロール リソースから表示テーブルを構築するために **DTCTL** 構造を使用しますが **、DTCTL** 構造は表示テーブル自体には表示されません。 この構造体は **、BuildDisplayTable に情報を提供します**。
  
**ulCtlFlags** メンバーでは、4 つのフラグDT_ACCEPT_DBCS、DT_EDITABLE、DT_MULTILINE_and DT_PASSWORD_EDITコントロールにのみ影響します。 他の 2 DT_REQUIREDおよびDT_SET_IMMEDIATE編集可能なコントロールに影響を与えます。 
  
ダイアログ ボックスで使用できるコントロールは、ラベル、テキスト ボックス、インク対応テキスト ボックス、リスト、ドロップダウン リスト、コンボ ボックス、チェック ボックス、グループ ボックス、ボタン、ラジオ ボタン、タブ付きページです。
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [MAPI の構造](mapi-structures.md)

