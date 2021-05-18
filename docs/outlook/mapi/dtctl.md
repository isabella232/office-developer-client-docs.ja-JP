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
# <a name="dtctl"></a><span data-ttu-id="d5603-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="d5603-103">DTCTL</span></span>

<span data-ttu-id="d5603-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5603-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5603-105">表示テーブルから作成されたダイアログ ボックスで使用されるコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d5603-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5603-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d5603-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5603-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5603-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d5603-108">Members</span><span class="sxs-lookup"><span data-stu-id="d5603-108">Members</span></span>

<span data-ttu-id="d5603-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="d5603-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="d5603-110">**ctl** メンバーに含まれるコントロールの種類と、コントロールのプロパティ **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) PR_CONTROL_TYPEに対応します。</span><span class="sxs-lookup"><span data-stu-id="d5603-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="d5603-111">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5603-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="d5603-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="d5603-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="d5603-113">ラベル コントロール</span><span class="sxs-lookup"><span data-stu-id="d5603-113">Label control.</span></span>
    
<span data-ttu-id="d5603-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="d5603-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="d5603-115">コントロールの編集。</span><span class="sxs-lookup"><span data-stu-id="d5603-115">Edit control.</span></span>
    
<span data-ttu-id="d5603-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="d5603-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="d5603-117">リスト ボックス コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-117">List box control.</span></span>
    
<span data-ttu-id="d5603-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="d5603-119">コンボ ボックス コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-119">Combo box control.</span></span>
    
<span data-ttu-id="d5603-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="d5603-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="d5603-121">ドロップダウン リスト コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-121">Drop-down list control.</span></span>
    
<span data-ttu-id="d5603-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="d5603-123">チェック ボックス コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-123">Check box control.</span></span>
    
<span data-ttu-id="d5603-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="d5603-125">グループ ボックス コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-125">Group box control.</span></span>
    
<span data-ttu-id="d5603-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d5603-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="d5603-127">ボタン コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-127">Button control.</span></span>
    
<span data-ttu-id="d5603-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="d5603-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="d5603-129">タブ付きページ コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-129">Tabbed page control.</span></span>
    
<span data-ttu-id="d5603-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="d5603-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="d5603-131">ラジオ ボタン コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-131">Radio button control.</span></span>
    
<span data-ttu-id="d5603-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="d5603-133">複数値のリスト コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="d5603-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="d5603-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="d5603-135">複数値のドロップダウン リスト コントロール。</span><span class="sxs-lookup"><span data-stu-id="d5603-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="d5603-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="d5603-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="d5603-137">コントロールの機能を説明し、コントロールのプロパティ[(PidTagControlFlags)](pidtagcontrolflags-canonical-property.md)プロパティPR_CONTROL_FLAGS対応するフラグのビットマスク。 </span><span class="sxs-lookup"><span data-stu-id="d5603-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="d5603-138">これらのフラグは、チェック ボックス、コンボ ボックス、リスト ボックス、および編集コントロールにのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="d5603-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="d5603-139">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5603-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="d5603-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="d5603-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="d5603-141">ANSI 形式または DBCS 形式のどちらかが受け入れ可能です。</span><span class="sxs-lookup"><span data-stu-id="d5603-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="d5603-142">このフラグは、編集コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d5603-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="d5603-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="d5603-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="d5603-144">ユーザーは、コントロール内のテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d5603-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="d5603-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="d5603-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="d5603-146">コントロールには、複数のテキスト行を含めできます。</span><span class="sxs-lookup"><span data-stu-id="d5603-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="d5603-147">このフラグは、編集コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d5603-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="d5603-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="d5603-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="d5603-149">コントロールにはパスワードが含まれている。したがって、コントロールの内容をユーザーに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5603-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="d5603-150">このフラグは、編集コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d5603-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="d5603-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="d5603-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="d5603-152">ダイアログ ボックス コントロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="d5603-152">The dialog box control is required.</span></span> <span data-ttu-id="d5603-153">このフラグは、編集およびコンボ ボックス コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d5603-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="d5603-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="d5603-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="d5603-155">コントロールの変更時に値を即座に出力できます。</span><span class="sxs-lookup"><span data-stu-id="d5603-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="d5603-156">これにより、2 つのコントロール間で依存関係を確立できます。</span><span class="sxs-lookup"><span data-stu-id="d5603-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="d5603-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="d5603-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="d5603-158">サービス プロバイダーとコントロールの識別子を表す [GUID](guid.md) 構造で構成される構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5603-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="d5603-159">**lpbNotif** メンバーと **cbNotif** メンバーは、コントロールの **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティに対応し、コントロールを更新する必要があるときにユーザー インターフェイスに通知するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5603-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="d5603-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="d5603-160">**cbNotif**</span></span>
  
> <span data-ttu-id="d5603-161">lpbNotif メンバーが指す構造体 **内のバイト数** 。</span><span class="sxs-lookup"><span data-stu-id="d5603-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="d5603-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="d5603-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="d5603-163">編集またはコンボ ボックス コントロールに入力できる文字を表す文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5603-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="d5603-164">他の種類のコントロールでは **、lpszFilter** メンバーを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="d5603-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="d5603-165">編集およびコンボ ボックス コントロールの場合、一度に 1 文字に適用される正規表現である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5603-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="d5603-166">コントロール内のすべての文字に同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="d5603-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="d5603-167">フィルター文字列の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5603-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="d5603-168">**文字**</span><span class="sxs-lookup"><span data-stu-id="d5603-168">**Character**</span></span>|<span data-ttu-id="d5603-169">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5603-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="d5603-170">任意の文字を使用できます (たとえば `"*"` )。</span><span class="sxs-lookup"><span data-stu-id="d5603-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="d5603-171">文字のセットを定義します (たとえば `"[0123456789]"` 、.)</span><span class="sxs-lookup"><span data-stu-id="d5603-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="d5603-172">文字の範囲を示します (たとえば `"[a-z]"` )。</span><span class="sxs-lookup"><span data-stu-id="d5603-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="d5603-173">これらの文字は使用できません (たとえば `"[~0-9]")` 、 .</span><span class="sxs-lookup"><span data-stu-id="d5603-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="d5603-174">前の記号を引用符で囲む場合に使用します (たとえば `"[\-\\\[\]]"` \, 、-、[、] 文字を使用できます)。</span><span class="sxs-lookup"><span data-stu-id="d5603-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="d5603-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="d5603-175">**ulItemID**</span></span>
  
> <span data-ttu-id="d5603-176">ダイアログ ボックス リソース内のコントロールを識別する値。</span><span class="sxs-lookup"><span data-stu-id="d5603-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="d5603-177">タブ付きページ コントロールの場合 **、ulItemID** DTCT_PAGEを使用して、文字列リソースからページのコンポーネント名を読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5603-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="d5603-178">位置とラベルの情報は、ダイアログ ボックス のリソースから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d5603-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="d5603-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="d5603-179">**ctl**</span></span>
  
> <span data-ttu-id="d5603-180">コントロールのデータを保持し、コントロールのプロパティ ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md) **)** プロパティPR_CONTROL_STRUCTURE対応する構造体。</span><span class="sxs-lookup"><span data-stu-id="d5603-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="d5603-181">コントロールの種類ごとに構造が異なります。</span><span class="sxs-lookup"><span data-stu-id="d5603-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5603-182">注釈</span><span class="sxs-lookup"><span data-stu-id="d5603-182">Remarks</span></span>

<span data-ttu-id="d5603-183">**DTCTL 構造体は**、任意の種類の 1 つのコントロールを記述します。</span><span class="sxs-lookup"><span data-stu-id="d5603-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="d5603-184">ほとんどのメンバーは、コントロールのプロパティを設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5603-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="d5603-185">**ctl メンバー** は、特定の種類のコントロールに関連する構造体の共用体です。</span><span class="sxs-lookup"><span data-stu-id="d5603-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="d5603-186">**たとえば、DTCTL** 構造体が編集コントロールを記述している場合 **、ctl** メンバーは [DTBLEDIT 構造体を指](dtbledit.md)します。</span><span class="sxs-lookup"><span data-stu-id="d5603-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="d5603-187">この構造体は、コントロールのプロパティに **PR_CONTROL_STRUCTURE** します。</span><span class="sxs-lookup"><span data-stu-id="d5603-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="d5603-188">共用体は、DTCTL 構造体のコンパイル時の初期化を可能にするための LPVOID 型の変数を最初の **メンバーとして持** っています。</span><span class="sxs-lookup"><span data-stu-id="d5603-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="d5603-189">[BuildDisplayTable](builddisplaytable.md)関数は、コントロール リソースから表示テーブルを構築するために **DTCTL** 構造を使用しますが **、DTCTL** 構造は表示テーブル自体には表示されません。</span><span class="sxs-lookup"><span data-stu-id="d5603-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="d5603-190">この構造体は **、BuildDisplayTable に情報を提供します**。</span><span class="sxs-lookup"><span data-stu-id="d5603-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="d5603-191">**ulCtlFlags** メンバーでは、4 つのフラグDT_ACCEPT_DBCS、DT_EDITABLE、DT_MULTILINE_and DT_PASSWORD_EDITコントロールにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="d5603-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="d5603-192">他の 2 DT_REQUIREDおよびDT_SET_IMMEDIATE編集可能なコントロールに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="d5603-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="d5603-193">ダイアログ ボックスで使用できるコントロールは、ラベル、テキスト ボックス、インク対応テキスト ボックス、リスト、ドロップダウン リスト、コンボ ボックス、チェック ボックス、グループ ボックス、ボタン、ラジオ ボタン、タブ付きページです。</span><span class="sxs-lookup"><span data-stu-id="d5603-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="d5603-194">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="d5603-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="d5603-195">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="d5603-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5603-196">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5603-196">See also</span></span>

- [<span data-ttu-id="d5603-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="d5603-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="d5603-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="d5603-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="d5603-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="d5603-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="d5603-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="d5603-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="d5603-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="d5603-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="d5603-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="d5603-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="d5603-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="d5603-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="d5603-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="d5603-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="d5603-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="d5603-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="d5603-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="d5603-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="d5603-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="d5603-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="d5603-210">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d5603-210">MAPI Structures</span></span>](mapi-structures.md)

