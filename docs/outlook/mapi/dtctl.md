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
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339411"
---
# <a name="dtctl"></a>DTCTL

**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるコントロールを表します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **ctl**メンバーに含まれているコントロールの種類で、コントロールの**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) プロパティに対応しています。 可能な値は次のとおりです。
    
DTCT_LABEL 
  
> ラベル コントロール
    
DTCT_EDIT 
  
> 編集コントロール
    
DTCT_LBX 
  
> リストボックスコントロール
    
DTCT_COMBOBOX 
  
> コンボボックスコントロール
    
DTCT_DDLBX 
  
> ドロップダウンリストコントロール。
    
DTCT_CHECKBOX 
  
> チェックボックスコントロール。
    
DTCT_GROUPBOX 
  
> グループボックスコントロール。
    
DTCT_BUTTON 
  
> [ボタン] コントロール
    
DTCT_PAGE 
  
> タブ付きページコントロール。
    
DTCT_RADIOBUTTON 
  
> ラジオボタンコントロール。
    
DTCT_MVLISTBOX 
  
> 複数値リストコントロール。
    
DTCT_MVDDLBX 
  
> 複数値ドロップダウンリストコントロール。
    
**ulCtlFlags**
  
> コントロールの機能を説明し、コントロールの**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに対応するフラグのビットマスク。 これらのフラグは、チェックボックス、コンボボックス、リストボックス、編集コントロールに対してのみ設定できます。 可能な値は次のとおりです。
    
DT_ACCEPT_DBCS 
  
> ANSI または DBCS 形式のいずれかが受け入れられます。 このフラグは、編集コントロールに対してのみ有効です。
    
DT_EDITABLE 
  
> ユーザーは、コントロール内のテキストを変更できます。 
    
DT_MULTILINE 
  
> コントロールには複数のテキスト行を含めることができます。 このフラグは、編集コントロールに対してのみ有効です。
    
DT_PASSWORD_EDIT 
  
> コントロールにはパスワードが含まれています。そのため、コントロールの内容をユーザーに表示しないようにする必要があります。 このフラグは、編集コントロールに対してのみ有効です。
    
DT_REQUIRED 
  
> ダイアログボックスコントロールが必要です。 このフラグは、編集コントロールとコンボボックスコントロールに対してのみ有効です。
    
DT_SET_IMMEDIATE 
  
> コントロールが変更されたときに、値の出力を即時に有効にします。 これにより、2つのコントロール間の依存関係を確立することができます。 
    
**lpbNotif**
  
> サービスプロバイダおよびコントロールの識別子を表すための[GUID](guid.md)構造で構成される構造体へのポインター。 **lpbNotif**および**cbNotif**メンバーは、コントロールの**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティに対応し、コントロールを更新する必要があるときに、ユーザーインターフェイスに通知するために使用されます。
    
**cbNotif**
  
> **lpbNotif**メンバーが指す構造体のバイト数。 
    
**lpszfilter**
  
> 編集コントロールまたはコンボボックスコントロールに入力できる文字を示す文字列へのポインター。 その他の種類のコントロールについては、 **lpszfilter**メンバーを NULL にすることができます。 エディットコントロールおよびコンボボックスコントロールの場合、一度に1文字に適用される正規表現である必要があります。 コントロール内のすべての文字に同じフィルターが適用されます。 フィルター文字列の形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> | 任意の文字を使用できます ( `"*"`例:)。  <br/> |
| `[ ]` <br/> |文字のセットを定義`"[0123456789]"`します (例:)。  <br/> |
| `-` <br/> |文字の範囲を示します (例: `"[a-z]"`)。  <br/> |
| `~` <br/> |これらの文字が許可されていないこと`"[~0-9]")`を示します (例:。 <br/>|   
| `\` <br/> |以前の記号のいずれかを引用するために使用`"[\-\\\[\]]"`されます\, (例:-、[、および] 文字が許可されます)。  <br/> |
   
**ulitemid**
  
> ダイアログボックスリソース内のコントロールを識別する値を指定します。 DTCT_PAGE 型のタブ付きページの場合、 **ulitemid**メンバーは、文字列リソースからページのコンポーネント名を読み込むためにオプションとして使用されます。 位置とラベルの情報は、ダイアログボックスリソースから読み取られます。 
    
**ctl**
  
> コントロールのデータを保持し、コントロールの**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) プロパティに対応する構造。 それぞれの種類のコントロールには、異なる構造があります。
    
## <a name="remarks"></a>解説

**DTCTL**構造体は、任意の型の1つのコントロールを表します。 このメンバーのほとんどは、コントロールのプロパティを設定するために使用されます。 
  
**ctl**メンバーは、特定の種類のコントロールに関連する構造の和集合です。 たとえば、 **DTCTL**構造体が編集コントロールを記述している場合、 **ctl**メンバーは[DTBLEDIT](dtbledit.md)構造を指します。 この構造体は、コントロールの**PR_CONTROL_STRUCTURE**プロパティに対応しています。 共用体の最初のメンバーは、 **DTCTL**構造体のコンパイル時の初期化を許可するために lpvoid 型の変数です。 
  
[builddisplaytable](builddisplaytable.md)関数は、 **DTCTL**構造を使用して、コントロールのリソースから表示テーブルを作成していますが、 **DTCTL**構造体は表示テーブル自体には表示されません。 この構造体は、 **builddisplaytable**に情報を提供するだけです。
  
**ulCtlFlags**メンバーでは、4つの flags DT_ACCEPT_DBCS、DT_EDITABLE、DT_MULTILINE_and DT_PASSWORD_EDIT が編集コントロールのみに影響します。 他の2つの DT_REQUIRED と DT_SET_IMMEDIATE は、編集可能なコントロールに影響します。 
  
ダイアログボックスで使用可能なコントロールには、ラベル、テキストボックス、インク認識のテキストボックス、リスト、ドロップダウンリスト、コンボボックス、チェックボックス、グループボックス、ボタン、ラジオボタン、およびタブページがあります。
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
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

