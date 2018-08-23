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
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800012"
---
# <a name="dtctl"></a><span data-ttu-id="49e66-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="49e66-103">DTCTL</span></span>

<span data-ttu-id="49e66-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49e66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49e66-105">ディスプレイ テーブルから作成されたダイアログ ボックスで使用するコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="49e66-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49e66-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="49e66-106">Header file:</span></span>  <br/> |<span data-ttu-id="49e66-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49e66-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="49e66-108">Members</span><span class="sxs-lookup"><span data-stu-id="49e66-108">Members</span></span>

<span data-ttu-id="49e66-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="49e66-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="49e66-110">**Ctl**のメンバーに含まれているし、コントロールの**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) のプロパティに対応するコントロールの種類です。</span><span class="sxs-lookup"><span data-stu-id="49e66-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="49e66-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="49e66-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="49e66-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="49e66-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="49e66-113">ラベル コントロール</span><span class="sxs-lookup"><span data-stu-id="49e66-113">Label control.</span></span>
    
<span data-ttu-id="49e66-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="49e66-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="49e66-115">コントロールを編集します。</span><span class="sxs-lookup"><span data-stu-id="49e66-115">Edit control.</span></span>
    
<span data-ttu-id="49e66-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="49e66-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="49e66-117">リスト ボックス コントロールです。</span><span class="sxs-lookup"><span data-stu-id="49e66-117">List box control.</span></span>
    
<span data-ttu-id="49e66-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="49e66-119">コンボ ボックス コントロールです。</span><span class="sxs-lookup"><span data-stu-id="49e66-119">Combo box control.</span></span>
    
<span data-ttu-id="49e66-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="49e66-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="49e66-121">ドロップダウン リスト コントロール。</span><span class="sxs-lookup"><span data-stu-id="49e66-121">Drop-down list control.</span></span>
    
<span data-ttu-id="49e66-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="49e66-123">チェック ボックスをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="49e66-123">Check box control.</span></span>
    
<span data-ttu-id="49e66-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="49e66-125">ボックス コントロールをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="49e66-125">Group box control.</span></span>
    
<span data-ttu-id="49e66-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="49e66-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="49e66-127">コントロールのボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e66-127">Button control.</span></span>
    
<span data-ttu-id="49e66-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="49e66-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="49e66-129">タブ付きページのコントロールです。</span><span class="sxs-lookup"><span data-stu-id="49e66-129">Tabbed page control.</span></span>
    
<span data-ttu-id="49e66-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="49e66-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="49e66-131">オプション ボタン コントロールです。</span><span class="sxs-lookup"><span data-stu-id="49e66-131">Radio button control.</span></span>
    
<span data-ttu-id="49e66-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="49e66-133">複数値を持つリスト コントロール。</span><span class="sxs-lookup"><span data-stu-id="49e66-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="49e66-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="49e66-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="49e66-135">複数値ドロップダウン リスト コントロール。</span><span class="sxs-lookup"><span data-stu-id="49e66-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="49e66-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="49e66-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="49e66-137">コントロールの機能について説明し、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) のプロパティに対応するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="49e66-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="49e66-138">これらのフラグは、チェック ボックス、コンボ ボックス、リスト ボックスに設定できるし、コントロールのみを編集します。</span><span class="sxs-lookup"><span data-stu-id="49e66-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="49e66-139">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="49e66-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="49e66-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="49e66-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="49e66-141">ANSI または DBCS のいずれかの形式が用意されています。</span><span class="sxs-lookup"><span data-stu-id="49e66-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="49e66-142">このフラグは、エディット コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="49e66-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="49e66-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="49e66-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="49e66-144">ユーザーは、コントロール内のテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="49e66-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="49e66-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="49e66-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="49e66-146">コントロールは、複数のテキスト行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="49e66-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="49e66-147">このフラグは、エディット コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="49e66-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="49e66-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="49e66-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="49e66-149">コントロールには、パスワードが含まれています。したがって、コントロールの内容がユーザーに表示されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="49e66-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="49e66-150">このフラグは、エディット コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="49e66-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="49e66-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="49e66-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="49e66-152">ダイアログ ボックスのコントロールは、必要があります。</span><span class="sxs-lookup"><span data-stu-id="49e66-152">The dialog box control is required.</span></span> <span data-ttu-id="49e66-153">このフラグは、編集し、コンボ ボックス コントロールに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="49e66-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="49e66-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="49e66-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="49e66-155">コントロールの変更時に値の直接の出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="49e66-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="49e66-156">こうと、依存関係を 2 つのコントロール間で確立することができます。</span><span class="sxs-lookup"><span data-stu-id="49e66-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="49e66-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="49e66-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="49e66-158">サービス プロバイダーと、コントロールの識別子を表す[GUID](guid.md)構造体で構成される構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49e66-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="49e66-159">**LpbNotif**と**cbNotif**のメンバーでは、 **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) のプロパティに対応しているし、コントロールを更新するときに、ユーザー ・ インタ フェースを通知するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="49e66-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="49e66-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="49e66-160">**cbNotif**</span></span>
  
> <span data-ttu-id="49e66-161">**LpbNotif**メンバーが指す構造体のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="49e66-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="49e66-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="49e66-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="49e66-163">文字を記述する文字列へのポインターは、エディット コントロールまたはコンボ ボックス コントロールに入力できます。</span><span class="sxs-lookup"><span data-stu-id="49e66-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="49e66-164">その他の種類のコントロールでは、NULL **lpszFilter**メンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="49e66-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="49e66-165">編集コントロールとコンボ ボックス コントロールには、一度に 1 つの文字に適用する正規表現をしてください。</span><span class="sxs-lookup"><span data-stu-id="49e66-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="49e66-166">コントロール内のすべての文字には、同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="49e66-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="49e66-167">フィルター文字列の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="49e66-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="49e66-168">**文字**</span><span class="sxs-lookup"><span data-stu-id="49e66-168">**Character**</span></span>|<span data-ttu-id="49e66-169">**説明**</span><span class="sxs-lookup"><span data-stu-id="49e66-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="49e66-170">任意の文字が許可される (たとえば、 `"*"`)。</span><span class="sxs-lookup"><span data-stu-id="49e66-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="49e66-171">文字のセットを定義 (たとえば、 `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="49e66-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="49e66-172">文字の範囲を示します (たとえば、 `"[a-z]"`)。</span><span class="sxs-lookup"><span data-stu-id="49e66-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="49e66-173">これらの文字が許可されていないことを示します (たとえば、 `"[~0-9]")`。</span><span class="sxs-lookup"><span data-stu-id="49e66-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="49e66-174">従来の記号のいずれかを引用するために使用 (たとえば、`"[\-\\\[\]]"`意味の\,[と] 文字は使用)。</span><span class="sxs-lookup"><span data-stu-id="49e66-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="49e66-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="49e66-175">**ulItemID**</span></span>
  
> <span data-ttu-id="49e66-176">ダイアログ ボックスのリソース内のコントロールを識別する値です。</span><span class="sxs-lookup"><span data-stu-id="49e66-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="49e66-177">DTCT_PAGE **ulItemID**の種類のタブ付きページのコントロールに、必要に応じてページのコンポーネントの名前を文字列リソースからロードするにメンバーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="49e66-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="49e66-178">位置およびラベル情報は、ダイアログ ボックスのリソースから読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="49e66-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="49e66-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="49e66-179">**ctl**</span></span>
  
> <span data-ttu-id="49e66-180">コントロールのデータを保持し、 **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) のプロパティに対応する構造体です。</span><span class="sxs-lookup"><span data-stu-id="49e66-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="49e66-181">コントロールの種類ごとには、さまざまな構造体があります。</span><span class="sxs-lookup"><span data-stu-id="49e66-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49e66-182">注釈</span><span class="sxs-lookup"><span data-stu-id="49e66-182">Remarks</span></span>

<span data-ttu-id="49e66-183">**DTCTL**構造体では、任意の型の 1 つのコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="49e66-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="49e66-184">ほとんどのメンバーを使用して、コントロールのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49e66-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="49e66-185">**Ctl**のメンバーは、特定の種類のコントロールに関連する構造体の共用体です。</span><span class="sxs-lookup"><span data-stu-id="49e66-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="49e66-186">**DTCTL**構造体は、エディット コントロールを記述するが場合、は、 [DTBLEDIT](dtbledit.md)構造体に、 **ctl**メンバーがポイントします。</span><span class="sxs-lookup"><span data-stu-id="49e66-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="49e66-187">この構造体は、コントロールの**PR_CONTROL_STRUCTURE**プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="49e66-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="49e66-188">**DTCTL**構造体のコンパイル時の初期化を許可するマーシャルの型の変数、その最初のメンバーとして、共用体があります。</span><span class="sxs-lookup"><span data-stu-id="49e66-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="49e66-189">[BuildDisplayTable](builddisplaytable.md)関数では、 **DTCTL**構造体を使用して、コントロールのリソースから表示された表を作成するため、表示された表自体のことはありません**DTCTL**構造体が表示されます。</span><span class="sxs-lookup"><span data-stu-id="49e66-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="49e66-190">この構造体は、単に**BuildDisplayTable**の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="49e66-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="49e66-191">**UlCtlFlags**メンバーでは、DT_ACCEPT_DBCS、DT_EDITABLE、DT_MULTILINE_and DT_PASSWORD_EDIT に影響を与える 4 つのフラグは、コントロールを編集します。</span><span class="sxs-lookup"><span data-stu-id="49e66-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="49e66-192">編集可能な任意のコントロールに影響を与える他の 2 つ DT_REQUIRED と DT_SET_IMMEDIATE。</span><span class="sxs-lookup"><span data-stu-id="49e66-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="49e66-193">ダイアログ ボックスで使用できるコントロールは、ラベル、テキスト ボックス、インク対応テキスト ボックス、リスト、」ドロップ ダウン リスト、コンボ ボックス、チェック ボックスをオン、グループ ボックス、ボタン、ラジオ ボタン、およびタブ付きページです。</span><span class="sxs-lookup"><span data-stu-id="49e66-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="49e66-194">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49e66-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="49e66-195">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49e66-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49e66-196">関連項目</span><span class="sxs-lookup"><span data-stu-id="49e66-196">See also</span></span>

- [<span data-ttu-id="49e66-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="49e66-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="49e66-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="49e66-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="49e66-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="49e66-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="49e66-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="49e66-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="49e66-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="49e66-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="49e66-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="49e66-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="49e66-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="49e66-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="49e66-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="49e66-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="49e66-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="49e66-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="49e66-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="49e66-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="49e66-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="49e66-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="49e66-210">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="49e66-210">MAPI Structures</span></span>](mapi-structures.md)

