---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424001"
---
# <a name="dtblpage"></a><span data-ttu-id="e8241-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="e8241-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="e8241-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8241-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8241-105">表示テーブルから作成されたダイアログ ボックスで使用されるタブ付きページについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e8241-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8241-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e8241-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8241-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8241-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e8241-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="e8241-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e8241-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="e8241-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="e8241-110">Members</span><span class="sxs-lookup"><span data-stu-id="e8241-110">Members</span></span>

 <span data-ttu-id="e8241-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="e8241-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="e8241-112">ページ タブの文字列ラベルのメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="e8241-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="e8241-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e8241-113">**ulFlags**</span></span>
  
> <span data-ttu-id="e8241-114">**ulbLpszLabelName** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e8241-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="e8241-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e8241-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="e8241-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8241-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e8241-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="e8241-117">The label is in Unicode format.</span></span> <span data-ttu-id="e8241-118">このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="e8241-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="e8241-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="e8241-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="e8241-120">MAPISVC の [ヘルプ ファイル マッピング **]** セクションを識別する文字列のメモリ内の位置。INF 構成ファイルまたは 0。</span><span class="sxs-lookup"><span data-stu-id="e8241-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="e8241-121">MAPISVC に表示されるファイル名。INF セクションを使用すると、ダイアログ ボックスの [ヘルプ] ボタンをクリックして、タブ付きページの拡張ヘルプにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e8241-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="e8241-122">MAPISVC のエントリの詳細については、次の情報を参照してください。[INF、「MAPISVC のファイル形式」を参照してください。INF .](file-format-of-mapisvc-inf.md)</span><span class="sxs-lookup"><span data-stu-id="e8241-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="e8241-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="e8241-123">**ulContext**</span></span>
  
> <span data-ttu-id="e8241-124">**ulbLpszComponent** メンバーによって定義された文字列内のタブ付きページの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="e8241-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="e8241-125">ヘルプ **ボタンが機能するには、ulbLpszComponent** メンバーと **ulContext** メンバーの両方が **0** 以外である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8241-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="e8241-126">この識別子が 0 で、コンポーネント文字列が NULL の場合、ページに関連付けられたヘルプはありません。</span><span class="sxs-lookup"><span data-stu-id="e8241-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e8241-127">注釈</span><span class="sxs-lookup"><span data-stu-id="e8241-127">Remarks</span></span>

<span data-ttu-id="e8241-128">**DTBLPAGE 構造は**、複数の関連するダイアログ ボックスを分離するために使用されるタブ付きページを表します。</span><span class="sxs-lookup"><span data-stu-id="e8241-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="e8241-129">通常、これらのダイアログ ボックスは、構成、メッセージ、または受信者のオプションを表示するためのプロパティ シートです。</span><span class="sxs-lookup"><span data-stu-id="e8241-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="e8241-130">タブをクリックすると、ユーザーはシート間で切り替えます。</span><span class="sxs-lookup"><span data-stu-id="e8241-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="e8241-131">コンポーネントの文字列とコンテキスト識別子は、タブ付きページで拡張ヘルプを使用できるかどうかに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e8241-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="e8241-132">拡張ヘルプが使用可能な場合、コンポーネント文字列とコンテキスト識別子は、そのヘルプにアクセスする方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e8241-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="e8241-133">コンポーネント文字列はヘルプ ファイルにマップされます。コンテキスト識別子は、最初のヘルプ トピックにマップされます。</span><span class="sxs-lookup"><span data-stu-id="e8241-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="e8241-134">コンテキスト識別子が 0 で、コンポーネント文字列が NULL の場合、拡張ヘルプは使用できません。</span><span class="sxs-lookup"><span data-stu-id="e8241-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="e8241-135">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="e8241-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e8241-136">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="e8241-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8241-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8241-137">See also</span></span>



[<span data-ttu-id="e8241-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e8241-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e8241-139">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e8241-139">MAPI Structures</span></span>](mapi-structures.md)

