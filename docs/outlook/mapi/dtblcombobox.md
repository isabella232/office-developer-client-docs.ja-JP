---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406977"
---
# <a name="dtblcombobox"></a><span data-ttu-id="edb00-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="edb00-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="edb00-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edb00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edb00-105">表示テーブルから作成されたダイアログ ボックスで使用されるコンボ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="edb00-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edb00-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="edb00-106">Header file:</span></span>  <br/> |<span data-ttu-id="edb00-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edb00-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="edb00-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="edb00-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="edb00-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="edb00-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a><span data-ttu-id="edb00-110">Members</span><span class="sxs-lookup"><span data-stu-id="edb00-110">Members</span></span>

 <span data-ttu-id="edb00-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="edb00-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="edb00-112">**DTBLCOMBOBOX** 構造体の開始から、制限がある場合は、コンボ ボックスの編集コントロールに入力できる文字を表す文字列フィルターへのオフセット。</span><span class="sxs-lookup"><span data-stu-id="edb00-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="edb00-113">フィルターは正規表現として解釈されるのではなく、入力された文字ごとに同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="edb00-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="edb00-114">フィルターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="edb00-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="edb00-115">**文字**</span><span class="sxs-lookup"><span data-stu-id="edb00-115">**Character**</span></span>|<span data-ttu-id="edb00-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="edb00-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="edb00-117">任意の文字を使用できます (たとえば  `"*"` )。</span><span class="sxs-lookup"><span data-stu-id="edb00-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="edb00-118">文字のセットを定義します (たとえば  `"[0123456789]"` )。</span><span class="sxs-lookup"><span data-stu-id="edb00-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="edb00-119">文字の範囲を示します (たとえば  `"[a-z]"` )。</span><span class="sxs-lookup"><span data-stu-id="edb00-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="edb00-120">これらの文字は使用できません。</span><span class="sxs-lookup"><span data-stu-id="edb00-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="edb00-121">(たとえば  `"[~0-9]"` )。</span><span class="sxs-lookup"><span data-stu-id="edb00-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="edb00-122">前の記号を引用符で囲む場合に使用します (たとえば  `"[\-\\\[\]]"` \, 、-、[、] 文字を使用できます)。</span><span class="sxs-lookup"><span data-stu-id="edb00-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="edb00-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="edb00-123">**ulFlags**</span></span>
  
> <span data-ttu-id="edb00-124">文字列フィルターの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="edb00-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="edb00-125">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="edb00-125">The following flag can be set:</span></span>
    
<span data-ttu-id="edb00-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="edb00-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="edb00-127">フィルターは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="edb00-127">The filter is in Unicode format.</span></span> <span data-ttu-id="edb00-128">このフラグMAPI_UNICODE設定されていない場合、フィルターは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="edb00-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="edb00-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="edb00-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="edb00-130">コンボ ボックスのテキスト ボックスに入力できる最大文字数。</span><span class="sxs-lookup"><span data-stu-id="edb00-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="edb00-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="edb00-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="edb00-132">型のプロパティのプロパティ タグPT_TSTRING。</span><span class="sxs-lookup"><span data-stu-id="edb00-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="edb00-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="edb00-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="edb00-134">**OpenProperty** 呼び出しをPT_OBJECT **IMAPITable** インターフェイスを開くことができる型のプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="edb00-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="edb00-135">表には **、ulPRPropertyName** メンバーで識別されるプロパティと同じ型のプロパティを持つ列が 1 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="edb00-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="edb00-136">テーブルの行を使用して、リストに値を設定します。</span><span class="sxs-lookup"><span data-stu-id="edb00-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="edb00-137">注釈</span><span class="sxs-lookup"><span data-stu-id="edb00-137">Remarks</span></span>

<span data-ttu-id="edb00-138">**DTBLCOMBOBOX** 構造体は、リストと選択フィールドで構成されるコントロールをコンボ ボックスで表します。</span><span class="sxs-lookup"><span data-stu-id="edb00-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="edb00-139">リストには、ユーザーが選択できる情報が表示され、選択フィールドに現在の選択範囲が表示されます。</span><span class="sxs-lookup"><span data-stu-id="edb00-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="edb00-140">選択フィールドは編集コントロールで、リストにテキストを入力していない場合にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="edb00-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="edb00-141">2 つのプロパティ タグ メンバーが連携して、リスト表示を編集コントロールと調整します。</span><span class="sxs-lookup"><span data-stu-id="edb00-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="edb00-142">MAPI が最初にコンボ ボックスを表示すると、表示テーブルに関連付けられた **IMAPIProp** 実装の **OpenProperty** メソッドを呼び出して **、ulPRTableName** メンバーで表されるテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="edb00-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="edb00-143">このテーブルには **、ulPRPropertyName** メンバーで表されるプロパティの値を含む列が 1 つ含まれます。</span><span class="sxs-lookup"><span data-stu-id="edb00-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="edb00-144">したがって、この列は **ulPRPropertyName** プロパティと同じ型である必要があります。両方の列は文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="edb00-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="edb00-145">列の値は、コンボ ボックスのリスト セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="edb00-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="edb00-146">したがって **、PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は **ulPRPropertyName** の有効なプロパティ タグではありません。</span><span class="sxs-lookup"><span data-stu-id="edb00-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="edb00-147">ユーザーがいずれかの行を選択するか、テキスト ボックスに新しいデータを入力すると **、ulPRPropertyName** プロパティは選択または入力された値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="edb00-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="edb00-148">編集コントロールの初期値を表示するには、MAPI は [IMAPIProp::GetProps](imapiprop-getprops.md) を呼び出して、表示テーブルのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="edb00-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="edb00-149">取得されたプロパティの 1 つが **ulPRPropertyName** メンバーで表されるプロパティと一致する場合、その値は初期値になります。</span><span class="sxs-lookup"><span data-stu-id="edb00-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="edb00-150">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="edb00-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="edb00-151">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="edb00-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edb00-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="edb00-152">See also</span></span>



[<span data-ttu-id="edb00-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="edb00-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="edb00-154">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="edb00-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="edb00-155">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="edb00-155">MAPI Structures</span></span>](mapi-structures.md)

