---
title: PidTagControlFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331865"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="efd6a-103">PidTagControlFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="efd6a-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="efd6a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efd6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efd6a-105">表示テーブルから構築されたダイアログボックスで使用されるコントロールの動作を制御するフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efd6a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="efd6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efd6a-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="efd6a-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="efd6a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="efd6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efd6a-109">0x3f00</span><span class="sxs-lookup"><span data-stu-id="efd6a-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="efd6a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="efd6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="efd6a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="efd6a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="efd6a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="efd6a-112">Area:</span></span>  <br/> |<span data-ttu-id="efd6a-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="efd6a-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efd6a-114">解説</span><span class="sxs-lookup"><span data-stu-id="efd6a-114">Remarks</span></span>

<span data-ttu-id="efd6a-115">このプロパティには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="efd6a-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="efd6a-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="efd6a-117">コントロールは、2バイト文字セット (DBCS) 文字を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="efd6a-118">このフラグは、編集コントロールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-118">This flag is used with edit controls.</span></span> <span data-ttu-id="efd6a-119">複数バイト文字セットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="efd6a-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="efd6a-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="efd6a-121">コントロールを編集できます。コントロールに関連付けられている値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="efd6a-122">このフラグが設定されていない場合、コントロールは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="efd6a-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="efd6a-123">この値は、ラベル、グループボックス、標準プッシュボタン、複数値ドロップダウンリストボックス、およびリストボックスコントロールでは無視されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="efd6a-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="efd6a-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="efd6a-125">編集コントロールには複数の行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="efd6a-126">これは、コントロール内に戻り文字を入力できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="efd6a-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="efd6a-127">このフラグは、編集コントロールに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="efd6a-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="efd6a-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="efd6a-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="efd6a-129">編集コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-129">Applies to edit controls.</span></span> <span data-ttu-id="efd6a-130">編集コントロールは、パスワードと同じように扱われます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-130">The edit control is treated like a password.</span></span> <span data-ttu-id="efd6a-131">値は、入力した実際の文字をエコーするのではなく、アスタリスクを使用して表示されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="efd6a-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="efd6a-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="efd6a-133">コントロールで変更が許可されている (DT_EDITABLE) 場合は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出される前に値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="efd6a-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="efd6a-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="efd6a-135">値の即時設定を有効にします。コントロールの値が変更されるとすぐに、MAPI は、そのコントロールに関連付けられているプロパティの**setprops**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="efd6a-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="efd6a-136">このフラグが設定されていない場合は、ダイアログボックスを閉じるときに値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="efd6a-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="efd6a-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="efd6a-138">リストボックス内で選択が行われると、そのリストボックスのインデックス列がプロパティとして設定されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="efd6a-139">DT_SET_IMMEDIATE で常に使用されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="efd6a-140">このプロパティは、コントロールの[DTCTL](dtctl.md)構造の ulCtlFlags メンバに格納されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="efd6a-141">コントロールフラグのほとんどは、ユーザー入力を許可するすべてのコントロールに適用されます。編集コントロールにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="efd6a-142">ユーザー入力を許可しないコントロール (ボタン、ラベルなど) は、コントロールフラグに0を設定します。</span><span class="sxs-lookup"><span data-stu-id="efd6a-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="efd6a-143">フラグの値の多くは、わかりやすいものになっています。</span><span class="sxs-lookup"><span data-stu-id="efd6a-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="efd6a-144">たとえば、コントロールに DT_REQUIRED が設定されている場合は、ダイアログボックスを閉じる前に値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="efd6a-145">サービスプロバイダーは、 **imapiprop**の実装によって値を指定するか、またはユーザーが1つの値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="efd6a-146">DT_EDITABLE は、コントロールの値を変更できることを示します。</span><span class="sxs-lookup"><span data-stu-id="efd6a-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="efd6a-147">DT_MULTILINE では、編集コントロールの値が複数行にわたることができます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="efd6a-148">コントロールフラグによっては、意味がわかりません。</span><span class="sxs-lookup"><span data-stu-id="efd6a-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="efd6a-149">コントロールが DT_SET_IMMEDIATE フラグを設定すると、その値に加えられた変更は、ユーザーが新しいコントロールに移動した直後に影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="efd6a-150">MAPI は、プロパティインターフェイスの[imapiprop:: setprops](imapiprop-setprops.md)メソッドに対して、コントロールのプロパティに対して1回の呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="efd6a-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="efd6a-151">これは既定の動作とは異なります。これは、ユーザーが **[OK** ] ボタンを選択するか、ダイアログボックスを閉じるまで、コントロールの値への変更を有効にするまでの時間を延期することです。</span><span class="sxs-lookup"><span data-stu-id="efd6a-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="efd6a-152">DT_SET_IMMEDIATE フラグは、多くの場合、表示テーブル通知と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="efd6a-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="efd6a-153">次の表に、コントロールの種類と、各種類に対して設定できるフラグの値を示します。</span><span class="sxs-lookup"><span data-stu-id="efd6a-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="efd6a-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="efd6a-154">**Control**</span></span>|<span data-ttu-id="efd6a-155">**このプロパティの有効な値**</span><span class="sxs-lookup"><span data-stu-id="efd6a-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efd6a-156">ボタン</span><span class="sxs-lookup"><span data-stu-id="efd6a-156">Button</span></span>  <br/> |<span data-ttu-id="efd6a-157">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-158">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-158">Check box</span></span>  <br/> |<span data-ttu-id="efd6a-159">DT_EDITABLE、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="efd6a-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="efd6a-160">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-160">Combo box</span></span>  <br/> |<span data-ttu-id="efd6a-161">DT_EDITABLE、DT_REQUIRED、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="efd6a-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="efd6a-162">ドロップダウンリストボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="efd6a-163">DT_EDITABLE、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="efd6a-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="efd6a-164">編集</span><span class="sxs-lookup"><span data-stu-id="efd6a-164">Edit</span></span>  <br/> |<span data-ttu-id="efd6a-165">DT_ACCEPT_DBCS、DT_MULTILINE、DT_EDITABLE、DT_PASSWORD_EDIT、DT_REQUIRED、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="efd6a-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="efd6a-166">グループ ボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-166">Group box</span></span>  <br/> |<span data-ttu-id="efd6a-167">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-168">Label</span><span class="sxs-lookup"><span data-stu-id="efd6a-168">Label</span></span>  <br/> |<span data-ttu-id="efd6a-169">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-170">リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-170">List box</span></span>  <br/> |<span data-ttu-id="efd6a-171">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-172">[複数値] ドロップダウンリストボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="efd6a-173">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-174">複数値リストボックス</span><span class="sxs-lookup"><span data-stu-id="efd6a-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="efd6a-175">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-176">タブ付きページ</span><span class="sxs-lookup"><span data-stu-id="efd6a-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="efd6a-177">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="efd6a-178">ラジオボタン</span><span class="sxs-lookup"><span data-stu-id="efd6a-178">Radio button</span></span>  <br/> |<span data-ttu-id="efd6a-179">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="efd6a-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="efd6a-180">関連リソース</span><span class="sxs-lookup"><span data-stu-id="efd6a-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="efd6a-181">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="efd6a-181">Header files</span></span>

<span data-ttu-id="efd6a-182">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efd6a-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="efd6a-183">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="efd6a-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="efd6a-184">Mapitags</span><span class="sxs-lookup"><span data-stu-id="efd6a-184">Mapitags.h</span></span>
  
> <span data-ttu-id="efd6a-185">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="efd6a-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efd6a-186">関連項目</span><span class="sxs-lookup"><span data-stu-id="efd6a-186">See also</span></span>



[<span data-ttu-id="efd6a-187">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="efd6a-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efd6a-188">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="efd6a-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efd6a-189">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="efd6a-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efd6a-190">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="efd6a-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

