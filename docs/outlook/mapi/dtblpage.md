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
# <a name="dtblpage"></a><span data-ttu-id="2b271-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="2b271-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="2b271-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b271-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b271-105">表示テーブルから構築されたダイアログボックスで使用されるタブページについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2b271-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b271-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2b271-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b271-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b271-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2b271-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="2b271-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="2b271-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="2b271-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="2b271-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="2b271-110">Members</span></span>

 <span data-ttu-id="2b271-111">**ulblpszlabel**</span><span class="sxs-lookup"><span data-stu-id="2b271-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="2b271-112">[ページ] タブの文字文字列ラベルのメモリ内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b271-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="2b271-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2b271-113">**ulFlags**</span></span>
  
> <span data-ttu-id="2b271-114">**ulblpszlabelname**メンバーによって示されるラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2b271-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="2b271-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2b271-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="2b271-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b271-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2b271-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2b271-117">The label is in Unicode format.</span></span> <span data-ttu-id="2b271-118">MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2b271-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="2b271-119">**ulblpszcomponent**</span><span class="sxs-lookup"><span data-stu-id="2b271-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="2b271-120">mapisvc.inf の **[Help File Mappings]** セクションを識別する文字列のメモリ内での位置を指定します。INF 構成ファイルまたは0。</span><span class="sxs-lookup"><span data-stu-id="2b271-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="2b271-121">mapisvc.inf に表示されるファイル名。INF セクションは、ユーザーがダイアログボックスの [**ヘルプ**] ボタンをクリックして、タブページの拡張ヘルプにアクセスするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b271-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="2b271-122">mapisvc.inf のエントリの詳細については、を参照してください。INF については、「 [File Format of mapisvc.inf」を参照してください。INF](file-format-of-mapisvc-inf.md)。</span><span class="sxs-lookup"><span data-stu-id="2b271-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="2b271-123">**ulcontext**</span><span class="sxs-lookup"><span data-stu-id="2b271-123">**ulContext**</span></span>
  
> <span data-ttu-id="2b271-124">**ulblpszcomponent**メンバーによって定義された文字列内のタブページの一意識別子。</span><span class="sxs-lookup"><span data-stu-id="2b271-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="2b271-125">[**ヘルプ**] ボタンが機能するためには、 **ulblpszcomponent**メンバーと**ulcontext**メンバーの両方が0以外である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b271-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="2b271-126">この識別子が0で、コンポーネントの文字列が NULL の場合、ページに関連付けられたヘルプはありません。</span><span class="sxs-lookup"><span data-stu-id="2b271-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2b271-127">注釈</span><span class="sxs-lookup"><span data-stu-id="2b271-127">Remarks</span></span>

<span data-ttu-id="2b271-128">**dtblpage**構造体は、複数の関連するダイアログボックスを区切るために使用されるコントロールをタブページとして記述します。</span><span class="sxs-lookup"><span data-stu-id="2b271-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="2b271-129">通常、これらのダイアログボックスは、構成、メッセージ、または受信者のオプションを表示するためのプロパティシートです。</span><span class="sxs-lookup"><span data-stu-id="2b271-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="2b271-130">タブをクリックすると、ユーザーは1つのシートから別のシートに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="2b271-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="2b271-131">コンポーネントの文字列とコンテキストの識別子は、タブ付きページで拡張ヘルプを使用できるかどうかに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b271-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="2b271-132">拡張ヘルプが利用可能な場合は、コンポーネントの文字列とコンテキストの識別子によって、そのアクセス方法に関する情報が得られます。</span><span class="sxs-lookup"><span data-stu-id="2b271-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="2b271-133">コンポーネントの文字列は、ヘルプファイルにマップされます。コンテキスト識別子は、最初のヘルプトピックにマップされます。</span><span class="sxs-lookup"><span data-stu-id="2b271-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="2b271-134">コンテキスト識別子が0で、コンポーネント文字列が NULL の場合、拡張ヘルプは使用できません。</span><span class="sxs-lookup"><span data-stu-id="2b271-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="2b271-135">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b271-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2b271-136">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b271-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b271-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b271-137">See also</span></span>



[<span data-ttu-id="2b271-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2b271-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="2b271-139">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2b271-139">MAPI Structures</span></span>](mapi-structures.md)

