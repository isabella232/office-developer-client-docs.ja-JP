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
# <a name="dtctl"></a><span data-ttu-id="16f52-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="16f52-103">DTCTL</span></span>

<span data-ttu-id="16f52-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16f52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16f52-105">表示テーブルから構築されたダイアログボックスで使用されるコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="16f52-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16f52-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="16f52-106">Header file:</span></span>  <br/> |<span data-ttu-id="16f52-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16f52-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="16f52-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="16f52-108">Members</span></span>

<span data-ttu-id="16f52-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="16f52-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="16f52-110">**ctl**メンバーに含まれているコントロールの種類で、コントロールの**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) プロパティに対応しています。</span><span class="sxs-lookup"><span data-stu-id="16f52-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="16f52-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="16f52-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="16f52-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="16f52-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="16f52-113">ラベル コントロール</span><span class="sxs-lookup"><span data-stu-id="16f52-113">Label control.</span></span>
    
<span data-ttu-id="16f52-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="16f52-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="16f52-115">編集コントロール</span><span class="sxs-lookup"><span data-stu-id="16f52-115">Edit control.</span></span>
    
<span data-ttu-id="16f52-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="16f52-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="16f52-117">リストボックスコントロール</span><span class="sxs-lookup"><span data-stu-id="16f52-117">List box control.</span></span>
    
<span data-ttu-id="16f52-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="16f52-119">コンボボックスコントロール</span><span class="sxs-lookup"><span data-stu-id="16f52-119">Combo box control.</span></span>
    
<span data-ttu-id="16f52-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="16f52-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="16f52-121">ドロップダウンリストコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-121">Drop-down list control.</span></span>
    
<span data-ttu-id="16f52-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="16f52-123">チェックボックスコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-123">Check box control.</span></span>
    
<span data-ttu-id="16f52-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="16f52-125">グループボックスコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-125">Group box control.</span></span>
    
<span data-ttu-id="16f52-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="16f52-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="16f52-127">[ボタン] コントロール</span><span class="sxs-lookup"><span data-stu-id="16f52-127">Button control.</span></span>
    
<span data-ttu-id="16f52-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="16f52-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="16f52-129">タブ付きページコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-129">Tabbed page control.</span></span>
    
<span data-ttu-id="16f52-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="16f52-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="16f52-131">ラジオボタンコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-131">Radio button control.</span></span>
    
<span data-ttu-id="16f52-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="16f52-133">複数値リストコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="16f52-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="16f52-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="16f52-135">複数値ドロップダウンリストコントロール。</span><span class="sxs-lookup"><span data-stu-id="16f52-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="16f52-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="16f52-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="16f52-137">コントロールの機能を説明し、コントロールの**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに対応するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="16f52-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="16f52-138">これらのフラグは、チェックボックス、コンボボックス、リストボックス、編集コントロールに対してのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="16f52-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="16f52-139">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="16f52-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="16f52-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="16f52-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="16f52-141">ANSI または DBCS 形式のいずれかが受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="16f52-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="16f52-142">このフラグは、編集コントロールに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="16f52-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="16f52-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="16f52-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="16f52-144">ユーザーは、コントロール内のテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="16f52-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="16f52-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="16f52-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="16f52-146">コントロールには複数のテキスト行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="16f52-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="16f52-147">このフラグは、編集コントロールに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="16f52-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="16f52-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="16f52-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="16f52-149">コントロールにはパスワードが含まれています。そのため、コントロールの内容をユーザーに表示しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="16f52-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="16f52-150">このフラグは、編集コントロールに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="16f52-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="16f52-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="16f52-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="16f52-152">ダイアログボックスコントロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="16f52-152">The dialog box control is required.</span></span> <span data-ttu-id="16f52-153">このフラグは、編集コントロールとコンボボックスコントロールに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="16f52-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="16f52-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="16f52-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="16f52-155">コントロールが変更されたときに、値の出力を即時に有効にします。</span><span class="sxs-lookup"><span data-stu-id="16f52-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="16f52-156">これにより、2つのコントロール間の依存関係を確立することができます。</span><span class="sxs-lookup"><span data-stu-id="16f52-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="16f52-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="16f52-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="16f52-158">サービスプロバイダおよびコントロールの識別子を表すための[GUID](guid.md)構造で構成される構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f52-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="16f52-159">**lpbNotif**および**cbNotif**メンバーは、コントロールの**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティに対応し、コントロールを更新する必要があるときに、ユーザーインターフェイスに通知するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="16f52-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="16f52-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="16f52-160">**cbNotif**</span></span>
  
> <span data-ttu-id="16f52-161">**lpbNotif**メンバーが指す構造体のバイト数。</span><span class="sxs-lookup"><span data-stu-id="16f52-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="16f52-162">**lpszfilter**</span><span class="sxs-lookup"><span data-stu-id="16f52-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="16f52-163">編集コントロールまたはコンボボックスコントロールに入力できる文字を示す文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f52-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="16f52-164">その他の種類のコントロールについては、 **lpszfilter**メンバーを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="16f52-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="16f52-165">エディットコントロールおよびコンボボックスコントロールの場合、一度に1文字に適用される正規表現である必要があります。</span><span class="sxs-lookup"><span data-stu-id="16f52-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="16f52-166">コントロール内のすべての文字に同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="16f52-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="16f52-167">フィルター文字列の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="16f52-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="16f52-168">**文字**</span><span class="sxs-lookup"><span data-stu-id="16f52-168">**Character**</span></span>|<span data-ttu-id="16f52-169">**説明**</span><span class="sxs-lookup"><span data-stu-id="16f52-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="16f52-170">任意の文字を使用できます ( `"*"`例:)。</span><span class="sxs-lookup"><span data-stu-id="16f52-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="16f52-171">文字のセットを定義`"[0123456789]"`します (例:)。</span><span class="sxs-lookup"><span data-stu-id="16f52-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="16f52-172">文字の範囲を示します (例: `"[a-z]"`)。</span><span class="sxs-lookup"><span data-stu-id="16f52-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="16f52-173">これらの文字が許可されていないこと`"[~0-9]")`を示します (例:。</span><span class="sxs-lookup"><span data-stu-id="16f52-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="16f52-174">以前の記号のいずれかを引用するために使用`"[\-\\\[\]]"`されます\, (例:-、[、および] 文字が許可されます)。</span><span class="sxs-lookup"><span data-stu-id="16f52-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="16f52-175">**ulitemid**</span><span class="sxs-lookup"><span data-stu-id="16f52-175">**ulItemID**</span></span>
  
> <span data-ttu-id="16f52-176">ダイアログボックスリソース内のコントロールを識別する値を指定します。</span><span class="sxs-lookup"><span data-stu-id="16f52-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="16f52-177">DTCT_PAGE 型のタブ付きページの場合、 **ulitemid**メンバーは、文字列リソースからページのコンポーネント名を読み込むためにオプションとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="16f52-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="16f52-178">位置とラベルの情報は、ダイアログボックスリソースから読み取られます。</span><span class="sxs-lookup"><span data-stu-id="16f52-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="16f52-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="16f52-179">**ctl**</span></span>
  
> <span data-ttu-id="16f52-180">コントロールのデータを保持し、コントロールの**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) プロパティに対応する構造。</span><span class="sxs-lookup"><span data-stu-id="16f52-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="16f52-181">それぞれの種類のコントロールには、異なる構造があります。</span><span class="sxs-lookup"><span data-stu-id="16f52-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16f52-182">注釈</span><span class="sxs-lookup"><span data-stu-id="16f52-182">Remarks</span></span>

<span data-ttu-id="16f52-183">**DTCTL**構造体は、任意の型の1つのコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="16f52-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="16f52-184">このメンバーのほとんどは、コントロールのプロパティを設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="16f52-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="16f52-185">**ctl**メンバーは、特定の種類のコントロールに関連する構造の和集合です。</span><span class="sxs-lookup"><span data-stu-id="16f52-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="16f52-186">たとえば、 **DTCTL**構造体が編集コントロールを記述している場合、 **ctl**メンバーは[DTBLEDIT](dtbledit.md)構造を指します。</span><span class="sxs-lookup"><span data-stu-id="16f52-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="16f52-187">この構造体は、コントロールの**PR_CONTROL_STRUCTURE**プロパティに対応しています。</span><span class="sxs-lookup"><span data-stu-id="16f52-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="16f52-188">共用体の最初のメンバーは、 **DTCTL**構造体のコンパイル時の初期化を許可するために lpvoid 型の変数です。</span><span class="sxs-lookup"><span data-stu-id="16f52-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="16f52-189">[builddisplaytable](builddisplaytable.md)関数は、 **DTCTL**構造を使用して、コントロールのリソースから表示テーブルを作成していますが、 **DTCTL**構造体は表示テーブル自体には表示されません。</span><span class="sxs-lookup"><span data-stu-id="16f52-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="16f52-190">この構造体は、 **builddisplaytable**に情報を提供するだけです。</span><span class="sxs-lookup"><span data-stu-id="16f52-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="16f52-191">**ulCtlFlags**メンバーでは、4つの flags DT_ACCEPT_DBCS、DT_EDITABLE、DT_MULTILINE_and DT_PASSWORD_EDIT が編集コントロールのみに影響します。</span><span class="sxs-lookup"><span data-stu-id="16f52-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="16f52-192">他の2つの DT_REQUIRED と DT_SET_IMMEDIATE は、編集可能なコントロールに影響します。</span><span class="sxs-lookup"><span data-stu-id="16f52-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="16f52-193">ダイアログボックスで使用可能なコントロールには、ラベル、テキストボックス、インク認識のテキストボックス、リスト、ドロップダウンリスト、コンボボックス、チェックボックス、グループボックス、ボタン、ラジオボタン、およびタブページがあります。</span><span class="sxs-lookup"><span data-stu-id="16f52-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="16f52-194">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16f52-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="16f52-195">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16f52-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16f52-196">関連項目</span><span class="sxs-lookup"><span data-stu-id="16f52-196">See also</span></span>

- [<span data-ttu-id="16f52-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="16f52-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="16f52-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="16f52-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="16f52-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="16f52-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="16f52-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="16f52-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="16f52-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="16f52-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="16f52-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="16f52-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="16f52-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="16f52-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="16f52-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="16f52-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="16f52-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="16f52-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="16f52-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="16f52-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="16f52-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="16f52-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="16f52-210">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="16f52-210">MAPI Structures</span></span>](mapi-structures.md)

