---
title: PidTagControlFlags の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802638"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="1789b-103">PidTagControlFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1789b-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1789b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1789b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1789b-105">ディスプレイ テーブルから作成されたダイアログ ボックスで使用するコントロールの動作を制御するフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="1789b-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1789b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1789b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1789b-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1789b-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1789b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1789b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1789b-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="1789b-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="1789b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1789b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1789b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1789b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1789b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1789b-112">Area:</span></span>  <br/> |<span data-ttu-id="1789b-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="1789b-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1789b-114">備考</span><span class="sxs-lookup"><span data-stu-id="1789b-114">Remarks</span></span>

<span data-ttu-id="1789b-115">次のフラグの 1 つ以上は、このプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1789b-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="1789b-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="1789b-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="1789b-117">コントロールは、これで 2 バイト文字セット (DBCS) 文字を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="1789b-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="1789b-118">このフラグは、エディット コントロールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-118">This flag is used with edit controls.</span></span> <span data-ttu-id="1789b-119">複数バイト文字セットは、できます。</span><span class="sxs-lookup"><span data-stu-id="1789b-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="1789b-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="1789b-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="1789b-121">コントロールを編集することができます。コントロールに関連付けられている値を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1789b-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="1789b-122">このフラグが設定されていない場合、コントロールが読み取り専用にします。</span><span class="sxs-lookup"><span data-stu-id="1789b-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="1789b-123">複数値ドロップダウン リスト ボックスとリスト ボックス コントロール、ラベル、グループ ボックス、標準のプッシュ ボタンには、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="1789b-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="1789b-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="1789b-125">エディット コントロールは、複数の行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1789b-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="1789b-126">これは、コントロール内で戻り値の文字を入力できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="1789b-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="1789b-127">このフラグは、エディット コントロールでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="1789b-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="1789b-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="1789b-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="1789b-129">エディット コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-129">Applies to edit controls.</span></span> <span data-ttu-id="1789b-130">エディット コントロールは、パスワードのように扱われます。</span><span class="sxs-lookup"><span data-stu-id="1789b-130">The edit control is treated like a password.</span></span> <span data-ttu-id="1789b-131">実際に入力した文字をエコーするのではなくアスタリスクを使用して値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="1789b-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="1789b-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="1789b-133">コントロールは、(DT_EDITABLE) の変更を許可している場合[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に値が必要です。</span><span class="sxs-lookup"><span data-stu-id="1789b-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="1789b-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="1789b-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="1789b-135">により即時の設定値のコントロールの値を変更するとすぐに、MAPI は、そのコントロールに関連付けられているプロパティの**SetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1789b-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="1789b-136">このフラグが設定されていない場合、ダイアログ ボックスを閉じるときに値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="1789b-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="1789b-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="1789b-138">リスト ボックス内で選択が行われると、そのリスト ボックスのインデックス列がプロパティとして設定されています。</span><span class="sxs-lookup"><span data-stu-id="1789b-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="1789b-139">常に DT_SET_IMMEDIATE を使用します。</span><span class="sxs-lookup"><span data-stu-id="1789b-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="1789b-140">このプロパティは、コントロールの[DTCTL](dtctl.md)構造体の ulCtlFlags メンバーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="1789b-141">コントロール フラグのほとんどすべてのユーザーの入力を許可するコントロールに適用します。いくつかは、エディット コントロールにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="1789b-142">ボタンやラベルなどのユーザー入力を許可しないコントロールは、コントロール フラグを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="1789b-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="1789b-143">フラグの値の多くは、説明されています。</span><span class="sxs-lookup"><span data-stu-id="1789b-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="1789b-144">たとえば、DT_REQUIRED 設定すると、コントロールのダイアログ ボックスが閉じられるまで許可される前に値でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1789b-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="1789b-145">サービス プロバイダーは、 **IMAPIProp**実装を通じて値を指定できますか、ユーザーがいずれかを入力します。</span><span class="sxs-lookup"><span data-stu-id="1789b-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="1789b-146">DT_EDITABLE は、コントロールの値を変更できることを示します。</span><span class="sxs-lookup"><span data-stu-id="1789b-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="1789b-147">DT_MULTILINE は、複数行にまたがって記述するエディット コントロールの値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1789b-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="1789b-148">制御フラグがいくつかは、その意味で原因は定かではありません。</span><span class="sxs-lookup"><span data-stu-id="1789b-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="1789b-149">コントロールは、DT_SET_IMMEDIATE フラグを設定、ときにユーザーが新しいコントロールに移動するとすぐにその値を変更が影響します。</span><span class="sxs-lookup"><span data-stu-id="1789b-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="1789b-150">MAPI は、コントロールのプロパティの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドをプロパティのインターフェイスの 1 つの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="1789b-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="1789b-151">これは、ユーザーが **[ok]** ボタンを選択するか、ダイアログ ボックスを閉じるまで有効にするコントロールの値に変更することを延期するのには、既定の動作と異なります。</span><span class="sxs-lookup"><span data-stu-id="1789b-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="1789b-152">DT_SET_IMMEDIATE フラグ表示のテーブルの通知と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="1789b-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="1789b-153">次の表は、コントロールの種類とそのすべての種類ごとに設定できるフラグの値の一覧です。</span><span class="sxs-lookup"><span data-stu-id="1789b-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="1789b-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="1789b-154">**Control**</span></span>|<span data-ttu-id="1789b-155">**このプロパティの有効な値**</span><span class="sxs-lookup"><span data-stu-id="1789b-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1789b-156">ボタン</span><span class="sxs-lookup"><span data-stu-id="1789b-156">Button</span></span>  <br/> |<span data-ttu-id="1789b-157">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-158">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-158">Check box</span></span>  <br/> |<span data-ttu-id="1789b-159">DT_EDITABLE、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="1789b-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="1789b-160">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-160">Combo box</span></span>  <br/> |<span data-ttu-id="1789b-161">DT_EDITABLE、DT_REQUIRED、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="1789b-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="1789b-162">ドロップダウン リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="1789b-163">DT_EDITABLE、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="1789b-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="1789b-164">編集</span><span class="sxs-lookup"><span data-stu-id="1789b-164">Edit</span></span>  <br/> |<span data-ttu-id="1789b-165">DT_ACCEPT_DBCS、DT_MULTILINE、DT_EDITABLE、DT_PASSWORD_EDIT、DT_REQUIRED、DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="1789b-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="1789b-166">グループ ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-166">Group box</span></span>  <br/> |<span data-ttu-id="1789b-167">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-168">ラベル</span><span class="sxs-lookup"><span data-stu-id="1789b-168">Label</span></span>  <br/> |<span data-ttu-id="1789b-169">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-170">リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-170">List box</span></span>  <br/> |<span data-ttu-id="1789b-171">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-172">複数値ドロップダウン リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="1789b-173">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-174">複数値リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="1789b-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="1789b-175">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-176">タブ付きページ</span><span class="sxs-lookup"><span data-stu-id="1789b-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="1789b-177">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="1789b-178">ラジオ ボタン</span><span class="sxs-lookup"><span data-stu-id="1789b-178">Radio button</span></span>  <br/> |<span data-ttu-id="1789b-179">0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1789b-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1789b-180">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1789b-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1789b-181">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1789b-181">Header files</span></span>

<span data-ttu-id="1789b-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1789b-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="1789b-183">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1789b-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="1789b-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1789b-184">Mapitags.h</span></span>
  
> <span data-ttu-id="1789b-185">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1789b-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1789b-186">関連項目</span><span class="sxs-lookup"><span data-stu-id="1789b-186">See also</span></span>



[<span data-ttu-id="1789b-187">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1789b-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1789b-188">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1789b-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1789b-189">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1789b-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1789b-190">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1789b-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

