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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eefd0c62314a35c4c6c956b8d4a4d92d5746d1c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590464"
---
# <a name="dtbledit"></a><span data-ttu-id="65954-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="65954-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="65954-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65954-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65954-105">ディスプレイ テーブルから作成されたダイアログ ボックスで使用するエディット コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="65954-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65954-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="65954-106">Header file:</span></span>  <br/> |<span data-ttu-id="65954-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65954-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="65954-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="65954-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="65954-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="65954-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="65954-110">Members</span><span class="sxs-lookup"><span data-stu-id="65954-110">Members</span></span>

 <span data-ttu-id="65954-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="65954-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="65954-112">該当する場合、エディット コントロールに入力できる文字の制限を記述する文字の文字列のフィルターに**DTBLEDIT**構造体の先頭からオフセットします。</span><span class="sxs-lookup"><span data-stu-id="65954-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="65954-113">フィルターは正規表現として解釈されないと、入力されたすべての文字に同じフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="65954-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="65954-114">フィルターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="65954-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="65954-115">**文字**</span><span class="sxs-lookup"><span data-stu-id="65954-115">**Character**</span></span>|<span data-ttu-id="65954-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="65954-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="65954-117">任意の文字が許可される (たとえば、 `"*"`)。</span><span class="sxs-lookup"><span data-stu-id="65954-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="65954-118">文字のセットを定義 (たとえば、 `"[0123456789]".`)</span><span class="sxs-lookup"><span data-stu-id="65954-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="65954-119">文字の範囲を示します (たとえば、 `"[a-z]"`)。</span><span class="sxs-lookup"><span data-stu-id="65954-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="65954-120">これらの文字が許可されていないことを示します (たとえば、 `"[~0-9]"`)。</span><span class="sxs-lookup"><span data-stu-id="65954-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="65954-121">従来の記号のいずれかを引用するために使用 (たとえば、`"[\-\\\[\]]"`意味の\,[と] 文字は使用)。</span><span class="sxs-lookup"><span data-stu-id="65954-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="65954-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="65954-122">**ulFlags**</span></span>
  
> <span data-ttu-id="65954-123">文字フィルターの形式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="65954-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="65954-124">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="65954-124">The following flag can be set:</span></span>
    
<span data-ttu-id="65954-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="65954-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="65954-126">フィルターは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="65954-126">The filter is in Unicode format.</span></span> <span data-ttu-id="65954-127">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフィルターです。</span><span class="sxs-lookup"><span data-stu-id="65954-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="65954-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="65954-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="65954-129">ユーザーがテキスト ボックスに入力できる文字の最大数。</span><span class="sxs-lookup"><span data-stu-id="65954-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="65954-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="65954-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="65954-131">型 PT_TSTRING のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="65954-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="65954-132">**UlPropTag**メンバーは、文字列のプロパティがデータを表示および編集コントロールでは編集を識別します。</span><span class="sxs-lookup"><span data-stu-id="65954-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65954-133">注釈</span><span class="sxs-lookup"><span data-stu-id="65954-133">Remarks</span></span>

<span data-ttu-id="65954-134">**DTBLEDIT**構造体は、エディット コントロールに英数字の情報を含むダイアログ ボックス上の領域を説明します。</span><span class="sxs-lookup"><span data-stu-id="65954-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="65954-135">ほぼすべてのダイアログ ボックスには、少なくとも 1 つのエディット コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="65954-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="65954-136">エディット コントロールは、ユーザーが変更可能または読み取り専用にできます。</span><span class="sxs-lookup"><span data-stu-id="65954-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="65954-137">エディット コントロールを 1 つにすることもできます行または複数行の文字列です。</span><span class="sxs-lookup"><span data-stu-id="65954-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="65954-138">複数行エディット コントロールには、通常、それらに関連付けられているスクロール バーがあります。</span><span class="sxs-lookup"><span data-stu-id="65954-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="65954-139">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65954-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="65954-140">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65954-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65954-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="65954-141">See also</span></span>



[<span data-ttu-id="65954-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="65954-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="65954-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="65954-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="65954-144">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="65954-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="65954-145">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="65954-145">MAPI Structures</span></span>](mapi-structures.md)

