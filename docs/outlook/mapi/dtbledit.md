---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404681"
---
# <a name="dtbledit"></a><span data-ttu-id="bcaa9-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="bcaa9-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="bcaa9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcaa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcaa9-105">表示テーブルから作成されたダイアログ ボックスで使用される編集コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcaa9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bcaa9-106">Header file:</span></span>  <br/> |<span data-ttu-id="bcaa9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcaa9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bcaa9-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="bcaa9-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="bcaa9-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="bcaa9-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="bcaa9-110">Members</span><span class="sxs-lookup"><span data-stu-id="bcaa9-110">Members</span></span>

 <span data-ttu-id="bcaa9-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="bcaa9-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="bcaa9-112">**DTBLEDIT** 構造体の開始から、制限がある場合は、編集コントロールに入力できる文字を表す文字列フィルターへのオフセット。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="bcaa9-113">フィルターは正規表現として解釈されるのではなく、入力された文字ごとに同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="bcaa9-114">フィルターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="bcaa9-115">**文字**</span><span class="sxs-lookup"><span data-stu-id="bcaa9-115">**Character**</span></span>|<span data-ttu-id="bcaa9-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="bcaa9-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="bcaa9-117">任意の文字を使用できます (たとえば  `"*"` )。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="bcaa9-118">文字のセットを定義します (たとえば  `"[0123456789]".` 、 )</span><span class="sxs-lookup"><span data-stu-id="bcaa9-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="bcaa9-119">文字の範囲を示します (たとえば  `"[a-z]"` )。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="bcaa9-120">これらの文字は使用できません (たとえば  `"[~0-9]"` )。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="bcaa9-121">前の記号を引用符で囲む場合に使用します (たとえば  `"[\-\\\[\]]"` \, 、-、[、] 文字を使用できます)。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="bcaa9-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="bcaa9-122">**ulFlags**</span></span>
  
> <span data-ttu-id="bcaa9-123">文字フィルターの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="bcaa9-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-124">The following flag can be set:</span></span>
    
<span data-ttu-id="bcaa9-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bcaa9-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="bcaa9-126">フィルターは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-126">The filter is in Unicode format.</span></span> <span data-ttu-id="bcaa9-127">このフラグMAPI_UNICODE設定されていない場合、フィルターは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="bcaa9-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="bcaa9-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="bcaa9-129">ユーザーがテキスト ボックスに入力できる最大文字数。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="bcaa9-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="bcaa9-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="bcaa9-131">型のプロパティのプロパティ タグPT_TSTRING。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="bcaa9-132">**ulPropTag メンバーは**、編集コントロールでデータが表示および編集される文字列プロパティを識別します。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bcaa9-133">注釈</span><span class="sxs-lookup"><span data-stu-id="bcaa9-133">Remarks</span></span>

<span data-ttu-id="bcaa9-134">**DTBLEDIT 構造体は**、英数字の情報を含むダイアログ ボックスの領域を編集コントロールに記述します。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="bcaa9-135">ほとんどすべてのダイアログ ボックスには、少なくとも 1 つの編集コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="bcaa9-136">編集コントロールは、ユーザーが変更したり、読み取り専用にしたりできます。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="bcaa9-137">編集コントロールには、単一行または複数行を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="bcaa9-138">複数行の編集コントロールには、通常、スクロール バーが関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="bcaa9-139">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="bcaa9-140">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="bcaa9-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bcaa9-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcaa9-141">See also</span></span>



[<span data-ttu-id="bcaa9-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="bcaa9-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="bcaa9-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="bcaa9-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="bcaa9-144">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcaa9-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="bcaa9-145">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="bcaa9-145">MAPI Structures</span></span>](mapi-structures.md)

