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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430883"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="430ca-103">PidTagControlFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="430ca-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="430ca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="430ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="430ca-105">表示テーブルから作成されたダイアログ ボックスで使用されるコントロールの動作を制御するフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="430ca-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="430ca-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="430ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="430ca-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="430ca-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="430ca-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="430ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="430ca-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="430ca-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="430ca-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="430ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="430ca-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="430ca-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="430ca-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="430ca-112">Area:</span></span>  <br/> |<span data-ttu-id="430ca-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="430ca-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="430ca-114">注釈</span><span class="sxs-lookup"><span data-stu-id="430ca-114">Remarks</span></span>

<span data-ttu-id="430ca-115">このプロパティには、次のフラグを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="430ca-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="430ca-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="430ca-117">コントロールには、Double-Byte文字セット (DBCS) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="430ca-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="430ca-118">このフラグは、編集コントロールと一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-118">This flag is used with edit controls.</span></span> <span data-ttu-id="430ca-119">複数バイトの文字セットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="430ca-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="430ca-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="430ca-121">コントロールは編集できます。コントロールに関連付けられている値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="430ca-122">このフラグが設定されていない場合、コントロールは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="430ca-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="430ca-123">ラベル、グループ ボックス、標準プッシュ ボタン、複数値のドロップダウン リスト ボックス、およびリスト ボックス コントロールでは、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="430ca-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="430ca-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="430ca-125">編集コントロールには複数の行を含めできます。</span><span class="sxs-lookup"><span data-stu-id="430ca-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="430ca-126">つまり、コントロール内に戻り文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="430ca-127">このフラグは、編集コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="430ca-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="430ca-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="430ca-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="430ca-129">編集コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-129">Applies to edit controls.</span></span> <span data-ttu-id="430ca-130">編集コントロールはパスワードのように扱います。</span><span class="sxs-lookup"><span data-stu-id="430ca-130">The edit control is treated like a password.</span></span> <span data-ttu-id="430ca-131">値は、入力された実際の文字をエコーするのではなく、アスタリスクを使用して表示されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="430ca-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="430ca-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="430ca-133">コントロールで変更を許可する場合 [(DT_EDITABLE)、IMAPIProp::SaveChanges](imapiprop-savechanges.md) が呼び出される前に値が必要です。</span><span class="sxs-lookup"><span data-stu-id="430ca-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="430ca-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="430ca-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="430ca-135">値の即時設定を有効にします。コントロールの値が変更されたとすぐに、MAPI は、そのコントロールに関連付けられているプロパティの **SetProps** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="430ca-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="430ca-136">このフラグを設定しない場合、ダイアログ ボックスが閉じらされた時点で値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="430ca-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="430ca-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="430ca-138">リスト ボックス内で選択が行われた場合、そのリスト ボックスのインデックス列はプロパティとして設定されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="430ca-139">常に、DT_SET_IMMEDIATE。</span><span class="sxs-lookup"><span data-stu-id="430ca-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="430ca-140">このプロパティは、コントロールの DTCTL 構造の ulCtlFlags [メンバーに格納](dtctl.md) されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="430ca-141">ほとんどのコントロール フラグは、ユーザー入力を許可するすべてのコントロールに適用されます。編集コントロールにのみ適用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="430ca-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="430ca-142">ボタンやラベルなどのユーザー入力を許可しないコントロールは、コントロール フラグに 0 を設定します。</span><span class="sxs-lookup"><span data-stu-id="430ca-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="430ca-143">フラグ値の多くは、自明です。</span><span class="sxs-lookup"><span data-stu-id="430ca-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="430ca-144">たとえば、コントロールDT_REQUIRED設定されている場合は、ダイアログ ボックスを閉じ込む前に値を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="430ca-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="430ca-145">サービス プロバイダーが **IMAPIProp** 実装を通じて値を指定するか、ユーザーが値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="430ca-146">DT_EDITABLEコントロールの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="430ca-147">DT_MULTILINE編集コントロールの値を複数行にまたがって指定できます。</span><span class="sxs-lookup"><span data-stu-id="430ca-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="430ca-148">一部のコントロール フラグは、その意味では明らかではありません。</span><span class="sxs-lookup"><span data-stu-id="430ca-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="430ca-149">コントロールが DT_SET_IMMEDIATEフラグを設定すると、その値に対する変更は、ユーザーが新しいコントロールに移動するとすぐに影響を受ける。</span><span class="sxs-lookup"><span data-stu-id="430ca-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="430ca-150">MAPI は、コントロールのプロパティのプロパティ インターフェイス [の IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを 1 回呼び出します。</span><span class="sxs-lookup"><span data-stu-id="430ca-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="430ca-151">これは既定の動作とは異なります。これは、ユーザーが **[OK]** ボタンを選択するか、ダイアログ ボックスを閉じるまで、コントロールの値に変更を加えるのを延期する方法です。</span><span class="sxs-lookup"><span data-stu-id="430ca-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="430ca-152">このDT_SET_IMMEDIATEは、多くの場合、表示テーブル通知と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="430ca-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="430ca-153">次の表に、コントロールの種類と、各種類に設定できるすべてのフラグ値を示します。</span><span class="sxs-lookup"><span data-stu-id="430ca-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="430ca-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="430ca-154">**Control**</span></span>|<span data-ttu-id="430ca-155">**このプロパティの有効な値**</span><span class="sxs-lookup"><span data-stu-id="430ca-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="430ca-156">ボタン</span><span class="sxs-lookup"><span data-stu-id="430ca-156">Button</span></span>  <br/> |<span data-ttu-id="430ca-157">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-158">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-158">Check box</span></span>  <br/> |<span data-ttu-id="430ca-159">DT_EDITABLE、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="430ca-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="430ca-160">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-160">Combo box</span></span>  <br/> |<span data-ttu-id="430ca-161">DT_EDITABLE、DT_REQUIRED、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="430ca-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="430ca-162">ドロップダウン リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="430ca-163">DT_EDITABLE、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="430ca-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="430ca-164">編集</span><span class="sxs-lookup"><span data-stu-id="430ca-164">Edit</span></span>  <br/> |<span data-ttu-id="430ca-165">DT_ACCEPT_DBCS、DT_MULTILINE、DT_EDITABLE、DT_PASSWORD_EDIT、DT_REQUIRED、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="430ca-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="430ca-166">グループ ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-166">Group box</span></span>  <br/> |<span data-ttu-id="430ca-167">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-168">ラベル</span><span class="sxs-lookup"><span data-stu-id="430ca-168">Label</span></span>  <br/> |<span data-ttu-id="430ca-169">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-170">リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-170">List box</span></span>  <br/> |<span data-ttu-id="430ca-171">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-172">[複数値] ドロップダウン リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="430ca-173">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-174">複数値リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="430ca-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="430ca-175">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-176">タブ付きページ</span><span class="sxs-lookup"><span data-stu-id="430ca-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="430ca-177">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="430ca-178">ラジオ ボタン</span><span class="sxs-lookup"><span data-stu-id="430ca-178">Radio button</span></span>  <br/> |<span data-ttu-id="430ca-179">0 である必要があります</span><span class="sxs-lookup"><span data-stu-id="430ca-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="430ca-180">関連リソース</span><span class="sxs-lookup"><span data-stu-id="430ca-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="430ca-181">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="430ca-181">Header files</span></span>

<span data-ttu-id="430ca-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="430ca-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="430ca-183">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="430ca-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="430ca-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="430ca-184">Mapitags.h</span></span>
  
> <span data-ttu-id="430ca-185">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="430ca-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="430ca-186">関連項目</span><span class="sxs-lookup"><span data-stu-id="430ca-186">See also</span></span>



[<span data-ttu-id="430ca-187">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="430ca-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="430ca-188">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="430ca-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="430ca-189">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="430ca-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="430ca-190">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="430ca-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

