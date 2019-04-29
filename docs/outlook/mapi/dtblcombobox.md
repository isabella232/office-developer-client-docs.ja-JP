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
# <a name="dtblcombobox"></a><span data-ttu-id="01745-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="01745-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="01745-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01745-105">表示テーブルから構築されたダイアログボックスで使用されるコンボボックスコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="01745-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01745-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="01745-106">Header file:</span></span>  <br/> |<span data-ttu-id="01745-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01745-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="01745-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="01745-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="01745-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="01745-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="01745-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="01745-110">Members</span></span>

 <span data-ttu-id="01745-111">**ulblpszcharsallowed**</span><span class="sxs-lookup"><span data-stu-id="01745-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="01745-112">**dtblcombobox**構造体の先頭から、制限がある場合は、コンボボックスの編集コントロールに入力できる文字を表す文字列フィルターへのオフセットです。</span><span class="sxs-lookup"><span data-stu-id="01745-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="01745-113">フィルターは正規表現として解釈されず、入力されたすべての文字に同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="01745-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="01745-114">フィルターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="01745-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="01745-115">**文字**</span><span class="sxs-lookup"><span data-stu-id="01745-115">**Character**</span></span>|<span data-ttu-id="01745-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="01745-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="01745-117">任意の文字を使用できます ( `"*"`例:)。</span><span class="sxs-lookup"><span data-stu-id="01745-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="01745-118">文字のセットを定義します (例`"[0123456789]"`:)。</span><span class="sxs-lookup"><span data-stu-id="01745-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="01745-119">文字の範囲を示します (例: `"[a-z]"`)。</span><span class="sxs-lookup"><span data-stu-id="01745-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="01745-120">これらの文字が許可されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="01745-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="01745-121">(例: `"[~0-9]"`)。</span><span class="sxs-lookup"><span data-stu-id="01745-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="01745-122">以前の記号のいずれかを引用するために使用`"[\-\\\[\]]"`されます\, (例:-、[、および] 文字が許可されます)。</span><span class="sxs-lookup"><span data-stu-id="01745-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="01745-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="01745-123">**ulFlags**</span></span>
  
> <span data-ttu-id="01745-124">文字文字列フィルタの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="01745-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="01745-125">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="01745-125">The following flag can be set:</span></span>
    
<span data-ttu-id="01745-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="01745-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="01745-127">フィルターは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="01745-127">The filter is in Unicode format.</span></span> <span data-ttu-id="01745-128">MAPI_UNICODE フラグが設定されていない場合、フィルターは ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="01745-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="01745-129">**ulnumcharsallowed**</span><span class="sxs-lookup"><span data-stu-id="01745-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="01745-130">コンボボックスのテキストボックスに入力できる最大文字数。</span><span class="sxs-lookup"><span data-stu-id="01745-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="01745-131">**ulprpropertyname**</span><span class="sxs-lookup"><span data-stu-id="01745-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="01745-132">PT_TSTRING 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="01745-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="01745-133">**ulprtablename**</span><span class="sxs-lookup"><span data-stu-id="01745-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="01745-134">**openproperty**呼び出しを使用して**IMAPITable**インターフェイスを開くことができる、PT_OBJECT 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="01745-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="01745-135">このテーブルには、 **ulprpropertyname**メンバーによって識別されるプロパティと同じ型のプロパティを持つ1つの列が必要です。</span><span class="sxs-lookup"><span data-stu-id="01745-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="01745-136">表の行は、リストを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="01745-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="01745-137">注釈</span><span class="sxs-lookup"><span data-stu-id="01745-137">Remarks</span></span>

<span data-ttu-id="01745-138">**dtblcombobox**構造体は、リストと選択フィールドで構成されるコントロールをコンボボックスに記述します。</span><span class="sxs-lookup"><span data-stu-id="01745-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="01745-139">一覧には、ユーザーが選択できる情報が表示され、選択フィールドに現在の選択範囲が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01745-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="01745-140">選択フィールドは、リストにまだ含まれていないテキストの入力にも使用できる編集コントロールです。</span><span class="sxs-lookup"><span data-stu-id="01745-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="01745-141">2つのプロパティタグのメンバーは連携して、リストの表示と編集コントロールを調整します。</span><span class="sxs-lookup"><span data-stu-id="01745-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="01745-142">最初に、MAPI がコンボボックスを表示するときには、表示テーブルに関連付けられている**imapiprop**実装の**openproperty**メソッドを呼び出して、 **ulprtablename**メンバーで表されるテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="01745-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="01745-143">このテーブルには、 **ulprpropertyname**メンバーによって表されるプロパティの値を含む1つの列があります。</span><span class="sxs-lookup"><span data-stu-id="01745-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="01745-144">したがって、この列は**ulprpropertyname**プロパティと同じ型である必要があり、両方の列は文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="01745-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="01745-145">列の値は、コンボボックスの [リスト] セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="01745-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="01745-146">そのため、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は**ulprpropertyname**の有効なプロパティタグではありません。</span><span class="sxs-lookup"><span data-stu-id="01745-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="01745-147">ユーザーがいずれかの行を選択するか、またはテキストボックスに新しいデータを入力すると、 **ulprpropertyname**プロパティが、選択または入力した値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="01745-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="01745-148">編集コントロールの初期値を表示するために、MAPI は[imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して、表示テーブルのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="01745-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="01745-149">取得したプロパティのいずれかが**ulprpropertyname**メンバーによって表されるプロパティと一致する場合、その値は初期値となります。</span><span class="sxs-lookup"><span data-stu-id="01745-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="01745-150">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01745-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="01745-151">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01745-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01745-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="01745-152">See also</span></span>



[<span data-ttu-id="01745-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="01745-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="01745-154">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="01745-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="01745-155">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="01745-155">MAPI Structures</span></span>](mapi-structures.md)

