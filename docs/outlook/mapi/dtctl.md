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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ce379ac70f140aae24880b118ca7293f2e72aa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574714"
---
# <a name="dtctl"></a>DTCTL

**適用されます**: Outlook 2013 |Outlook 2016 
  
ディスプレイ テーブルから作成されたダイアログ ボックスで使用するコントロールについて説明します。 
  
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
  
> **Ctl**のメンバーに含まれているし、コントロールの**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) のプロパティに対応するコントロールの種類です。 使用可能な値は次のとおりです。
    
DTCT_LABEL 
  
> ラベル コントロール
    
DTCT_EDIT 
  
> コントロールを編集します。
    
DTCT_LBX 
  
> リスト ボックス コントロールです。
    
DTCT_COMBOBOX 
  
> コンボ ボックス コントロールです。
    
DTCT_DDLBX 
  
> ドロップダウン リスト コントロール。
    
DTCT_CHECKBOX 
  
> チェック ボックスをコントロールします。
    
DTCT_GROUPBOX 
  
> ボックス コントロールをグループ化します。
    
DTCT_BUTTON 
  
> コントロールのボタンをクリックします。
    
DTCT_PAGE 
  
> タブ付きページのコントロールです。
    
DTCT_RADIOBUTTON 
  
> オプション ボタン コントロールです。
    
DTCT_MVLISTBOX 
  
> 複数値を持つリスト コントロール。
    
DTCT_MVDDLBX 
  
> 複数値ドロップダウン リスト コントロール。
    
**ulCtlFlags**
  
> コントロールの機能について説明し、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) のプロパティに対応するフラグのビットマスクです。 これらのフラグは、チェック ボックス、コンボ ボックス、リスト ボックスに設定できるし、コントロールのみを編集します。 使用可能な値は次のとおりです。
    
DT_ACCEPT_DBCS 
  
> ANSI または DBCS のいずれかの形式が用意されています。 このフラグは、エディット コントロールでのみ有効です。
    
DT_EDITABLE 
  
> ユーザーは、コントロール内のテキストを変更できます。 
    
DT_MULTILINE 
  
> コントロールは、複数のテキスト行を含めることができます。 このフラグは、エディット コントロールでのみ有効です。
    
DT_PASSWORD_EDIT 
  
> コントロールには、パスワードが含まれています。したがって、コントロールの内容がユーザーに表示されない必要があります。 このフラグは、エディット コントロールでのみ有効です。
    
DT_REQUIRED 
  
> ダイアログ ボックスのコントロールは、必要があります。 このフラグは、編集し、コンボ ボックス コントロールに対してのみ有効です。
    
DT_SET_IMMEDIATE 
  
> コントロールの変更時に値の直接の出力を有効にします。 こうと、依存関係を 2 つのコントロール間で確立することができます。 
    
**lpbNotif**
  
> サービス プロバイダーと、コントロールの識別子を表す[GUID](guid.md)構造体で構成される構造体へのポインター。 **LpbNotif**と**cbNotif**のメンバーでは、 **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) のプロパティに対応しているし、コントロールを更新するときに、ユーザー ・ インタ フェースを通知するために使用されます。
    
**cbNotif**
  
> **LpbNotif**メンバーが指す構造体のバイト数をカウントします。 
    
**lpszFilter**
  
> 文字を記述する文字列へのポインターは、エディット コントロールまたはコンボ ボックス コントロールに入力できます。 その他の種類のコントロールでは、NULL **lpszFilter**メンバーがあります。 編集コントロールとコンボ ボックス コントロールには、一度に 1 つの文字に適用する正規表現をしてください。 コントロール内のすべての文字には、同じフィルターが適用されます。 フィルター文字列の形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> | 任意の文字が許可される (たとえば、 `"*"`)。  <br/> |
| `[ ]` <br/> |文字のセットを定義 (たとえば、 `"[0123456789]"`.)  <br/> |
| `-` <br/> |文字の範囲を示します (たとえば、 `"[a-z]"`)。  <br/> |
| `~` <br/> |これらの文字が許可されていないことを示します (たとえば、 `"[~0-9]")`。 <br/>|   
| `\` <br/> |従来の記号のいずれかを引用するために使用 (たとえば、`"[\-\\\[\]]"`意味の\,[と] 文字は使用)。  <br/> |
   
**ulItemID**
  
> ダイアログ ボックスのリソース内のコントロールを識別する値です。 DTCT_PAGE **ulItemID**の種類のタブ付きページのコントロールに、必要に応じてページのコンポーネントの名前を文字列リソースからロードするにメンバーが使用されます。 位置およびラベル情報は、ダイアログ ボックスのリソースから読み込まれます。 
    
**ctl**
  
> コントロールのデータを保持し、 **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) のプロパティに対応する構造体です。 コントロールの種類ごとには、さまざまな構造体があります。
    
## <a name="remarks"></a>注釈

**DTCTL**構造体では、任意の型の 1 つのコントロールについて説明します。 ほとんどのメンバーを使用して、コントロールのプロパティを設定します。 
  
**Ctl**のメンバーは、特定の種類のコントロールに関連する構造体の共用体です。 **DTCTL**構造体は、エディット コントロールを記述するが場合、は、 [DTBLEDIT](dtbledit.md)構造体に、 **ctl**メンバーがポイントします。 この構造体は、コントロールの**PR_CONTROL_STRUCTURE**プロパティに対応します。 **DTCTL**構造体のコンパイル時の初期化を許可するマーシャルの型の変数、その最初のメンバーとして、共用体があります。 
  
[BuildDisplayTable](builddisplaytable.md)関数では、 **DTCTL**構造体を使用して、コントロールのリソースから表示された表を作成するため、表示された表自体のことはありません**DTCTL**構造体が表示されます。 この構造体は、単に**BuildDisplayTable**の情報を提供します。
  
**UlCtlFlags**メンバーでは、DT_ACCEPT_DBCS、DT_EDITABLE、DT_MULTILINE_and DT_PASSWORD_EDIT に影響を与える 4 つのフラグは、コントロールを編集します。 編集可能な任意のコントロールに影響を与える他の 2 つ DT_REQUIRED と DT_SET_IMMEDIATE。 
  
ダイアログ ボックスで使用できるコントロールは、ラベル、テキスト ボックス、インク対応テキスト ボックス、リスト、」ドロップ ダウン リスト、コンボ ボックス、チェック ボックスをオン、グループ ボックス、ボタン、ラジオ ボタン、およびタブ付きページです。
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
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

