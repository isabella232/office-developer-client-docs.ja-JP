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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799969"
---
# <a name="dtblcombobox"></a><span data-ttu-id="354fc-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="354fc-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="354fc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="354fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="354fc-105">ダイアログ ボックスが表示テーブルの構築に使用するコンボ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="354fc-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="354fc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="354fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="354fc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="354fc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="354fc-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="354fc-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="354fc-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="354fc-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="354fc-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="354fc-110">Members</span></span>

 <span data-ttu-id="354fc-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="354fc-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="354fc-112">場合、エディット コントロールのいずれかのコンボ ボックスに入力できる文字の制限を記述する文字の文字列のフィルターに**DTBLCOMBOBOX**構造体の先頭からオフセットします。</span><span class="sxs-lookup"><span data-stu-id="354fc-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="354fc-113">フィルターは正規表現として解釈されないと、入力されたすべての文字に同じフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="354fc-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="354fc-114">フィルターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="354fc-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="354fc-115">**文字**</span><span class="sxs-lookup"><span data-stu-id="354fc-115">**Character**</span></span>|<span data-ttu-id="354fc-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="354fc-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="354fc-117">任意の文字が許可される (たとえば、 `"*"`)。</span><span class="sxs-lookup"><span data-stu-id="354fc-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="354fc-118">文字のセットを定義 (たとえば、 `"[0123456789]"`)。</span><span class="sxs-lookup"><span data-stu-id="354fc-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="354fc-119">文字の範囲を示します (たとえば、 `"[a-z]"`)。</span><span class="sxs-lookup"><span data-stu-id="354fc-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="354fc-120">これらの文字が許可されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="354fc-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="354fc-121">(たとえば、 `"[~0-9]"`)。</span><span class="sxs-lookup"><span data-stu-id="354fc-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="354fc-122">従来の記号のいずれかを引用するために使用 (たとえば、`"[\-\\\[\]]"`意味の\,[と] 文字は使用)。</span><span class="sxs-lookup"><span data-stu-id="354fc-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="354fc-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="354fc-123">**ulFlags**</span></span>
  
> <span data-ttu-id="354fc-124">文字の文字列のフィルターの形式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="354fc-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="354fc-125">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="354fc-125">The following flag can be set:</span></span>
    
<span data-ttu-id="354fc-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="354fc-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="354fc-127">フィルターは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="354fc-127">The filter is in Unicode format.</span></span> <span data-ttu-id="354fc-128">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフィルターです。</span><span class="sxs-lookup"><span data-stu-id="354fc-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="354fc-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="354fc-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="354fc-130">コンボ ボックスのテキスト ボックスに入力できる文字の最大数。</span><span class="sxs-lookup"><span data-stu-id="354fc-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="354fc-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="354fc-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="354fc-132">型 PT_TSTRING のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="354fc-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="354fc-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="354fc-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="354fc-134">**IMAPITable**インターフェイスを**OpenProperty**呼び出しを使用して開くことができる型 PT_OBJECT のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="354fc-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="354fc-135">テーブルには、1 つの列プロパティは、 **ulPRPropertyName**のメンバーによって識別されるプロパティと同じ型を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="354fc-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="354fc-136">リストを作成するテーブルの行を使用します。</span><span class="sxs-lookup"><span data-stu-id="354fc-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="354fc-137">備考</span><span class="sxs-lookup"><span data-stu-id="354fc-137">Remarks</span></span>

<span data-ttu-id="354fc-138">**DTBLCOMBOBOX**構造体では、コンボ ボックスの一覧と、[選択] フィールドで構成されるコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="354fc-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="354fc-139">一覧には、情報をユーザーが選択できる、選択フィールドには、現在の選択範囲が表示されますが表示されます。</span><span class="sxs-lookup"><span data-stu-id="354fc-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="354fc-140">選択フィールドは、エディット コントロールにテキストを入力されていないリストも使用できます。</span><span class="sxs-lookup"><span data-stu-id="354fc-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="354fc-141">エディット コントロールにリストの表示を調整するため 2 つのプロパティ タグのメンバーが連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="354fc-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="354fc-142">MAPI には、まず、コンボ ボックスが表示されたら、 **ulPRTableName**のメンバーによって表されるテーブルを取得するために表示された表に関連付けられている**IMAPIProp**実装の**OpenProperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="354fc-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="354fc-143">このテーブルは、 **ulPRPropertyName**のメンバーによって表されるプロパティの値を含む列を 1 つの列にあります。</span><span class="sxs-lookup"><span data-stu-id="354fc-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="354fc-144">したがって、 **ulPRPropertyName**プロパティと同じ型のこの列がある必要があり、両方の列は文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="354fc-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="354fc-145">列の値は、コンボ ボックスのリスト] セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="354fc-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="354fc-146">したがって、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は、 **ulPRPropertyName**のプロパティの有効なタグではありません。</span><span class="sxs-lookup"><span data-stu-id="354fc-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="354fc-147">ユーザーは、行のいずれかを選択するか、テキスト ボックスに新しいデータを入力、すると、 **ulPRPropertyName**プロパティは、選択または入力した値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="354fc-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="354fc-148">エディット コントロールの初期値を表示するには、MAPI は、表示された表のプロパティ値を取得するために[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="354fc-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="354fc-149">取得したプロパティのいずれかには、 **ulPRPropertyName**のメンバーによって表されるプロパティが一致すると、その値が初期値になります。</span><span class="sxs-lookup"><span data-stu-id="354fc-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="354fc-150">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="354fc-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="354fc-151">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="354fc-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="354fc-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="354fc-152">See also</span></span>



[<span data-ttu-id="354fc-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="354fc-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="354fc-154">PidTagControlType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="354fc-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="354fc-155">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="354fc-155">MAPI Structures</span></span>](mapi-structures.md)

