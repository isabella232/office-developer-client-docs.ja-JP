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
# <a name="dtbledit"></a><span data-ttu-id="f8232-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="f8232-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="f8232-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8232-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8232-105">表示テーブルから構築されたダイアログボックスで使用される編集コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="f8232-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8232-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f8232-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8232-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8232-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f8232-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="f8232-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f8232-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="f8232-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="f8232-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="f8232-110">Members</span></span>

 <span data-ttu-id="f8232-111">**ulblpszcharsallowed**</span><span class="sxs-lookup"><span data-stu-id="f8232-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="f8232-112">編集コントロールに入力できる文字に制限がある場合は、 **DTBLEDIT**構造の先頭から、制限を表す文字列フィルターまでのオフセット。</span><span class="sxs-lookup"><span data-stu-id="f8232-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="f8232-113">フィルターは正規表現として解釈されず、入力されたすべての文字に同じフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f8232-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="f8232-114">フィルターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f8232-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="f8232-115">**文字**</span><span class="sxs-lookup"><span data-stu-id="f8232-115">**Character**</span></span>|<span data-ttu-id="f8232-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8232-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="f8232-117">任意の文字を使用できます ( `"*"`例:)。</span><span class="sxs-lookup"><span data-stu-id="f8232-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="f8232-118">文字のセットを定義します`"[0123456789]".`(例:)。</span><span class="sxs-lookup"><span data-stu-id="f8232-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="f8232-119">文字の範囲を示します (例: `"[a-z]"`)。</span><span class="sxs-lookup"><span data-stu-id="f8232-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="f8232-120">これらの文字が許可されていないこと`"[~0-9]"`を示します (例:)。</span><span class="sxs-lookup"><span data-stu-id="f8232-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="f8232-121">以前の記号のいずれかを引用するために使用`"[\-\\\[\]]"`されます\, (例:-、[、および] 文字が許可されます)。</span><span class="sxs-lookup"><span data-stu-id="f8232-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="f8232-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f8232-122">**ulFlags**</span></span>
  
> <span data-ttu-id="f8232-123">文字フィルターの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f8232-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="f8232-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f8232-124">The following flag can be set:</span></span>
    
<span data-ttu-id="f8232-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8232-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f8232-126">フィルターは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="f8232-126">The filter is in Unicode format.</span></span> <span data-ttu-id="f8232-127">MAPI_UNICODE フラグが設定されていない場合、フィルターは ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="f8232-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="f8232-128">**ulnumcharsallowed**</span><span class="sxs-lookup"><span data-stu-id="f8232-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="f8232-129">ユーザーがテキストボックスに入力できる最大文字数。</span><span class="sxs-lookup"><span data-stu-id="f8232-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="f8232-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="f8232-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="f8232-131">PT_TSTRING 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="f8232-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="f8232-132">**ulPropTag**メンバーは、編集コントロールでデータを表示および編集するための文字列プロパティを識別します。</span><span class="sxs-lookup"><span data-stu-id="f8232-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f8232-133">注釈</span><span class="sxs-lookup"><span data-stu-id="f8232-133">Remarks</span></span>

<span data-ttu-id="f8232-134">**DTBLEDIT**構造体には、英数字情報を含むダイアログボックスの領域の編集コントロールが記述されています。</span><span class="sxs-lookup"><span data-stu-id="f8232-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="f8232-135">ほとんどすべてのダイアログボックスには、少なくとも1つの編集コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="f8232-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="f8232-136">編集コントロールは、ユーザーまたは読み取り専用で変更できます。</span><span class="sxs-lookup"><span data-stu-id="f8232-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="f8232-137">編集コントロールは、単一行または複数行にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f8232-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="f8232-138">通常、複数行の編集コントロールには、スクロールバーが関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="f8232-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="f8232-139">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8232-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f8232-140">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8232-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8232-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8232-141">See also</span></span>



[<span data-ttu-id="f8232-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f8232-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="f8232-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f8232-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f8232-144">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8232-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="f8232-145">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f8232-145">MAPI Structures</span></span>](mapi-structures.md)

