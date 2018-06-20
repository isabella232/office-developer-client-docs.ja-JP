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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 86cd30b15402f35e8396dedf6b685050ee4fb45e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800002"
---
# <a name="dtblpage"></a><span data-ttu-id="5d64f-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5d64f-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="5d64f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d64f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d64f-105">ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するタブ付きのページを説明します。</span><span class="sxs-lookup"><span data-stu-id="5d64f-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d64f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5d64f-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d64f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d64f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5d64f-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="5d64f-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="5d64f-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="5d64f-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="5d64f-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="5d64f-110">Members</span></span>

 <span data-ttu-id="5d64f-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="5d64f-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="5d64f-112">ページ タブの文字の文字列のラベルのメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="5d64f-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="5d64f-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5d64f-113">**ulFlags**</span></span>
  
> <span data-ttu-id="5d64f-114">**UlbLpszLabelName**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5d64f-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="5d64f-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5d64f-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="5d64f-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5d64f-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5d64f-117">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="5d64f-117">The label is in Unicode format.</span></span> <span data-ttu-id="5d64f-118">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="5d64f-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="5d64f-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="5d64f-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="5d64f-120">**[ヘルプ ファイルのマッピング]** セクションで、MAPISVC を識別する文字列のメモリ内の位置。INF ファイルを構成、または 0。</span><span class="sxs-lookup"><span data-stu-id="5d64f-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="5d64f-121">MAPISVC に表示されるファイル名です。INF セクション] ダイアログ ボックスの [**ヘルプ**] ボタンをクリックすると、タブ付きページの拡張ヘルプにアクセスするユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d64f-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="5d64f-122">MAPISVC 内のエントリに関する詳細については。INF、[形式の MAPISVC にファイルを参照してください。INF](file-format-of-mapisvc-inf.md)。</span><span class="sxs-lookup"><span data-stu-id="5d64f-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="5d64f-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="5d64f-123">**ulContext**</span></span>
  
> <span data-ttu-id="5d64f-124">**UlbLpszComponent**のメンバーによって定義されている文字列のタブ付きページの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="5d64f-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="5d64f-125">**UlbLpszComponent**メンバーと**ulContext**のメンバーの両方を操作するのには [**ヘルプ**] ボタンを 0 以外の値にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d64f-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="5d64f-126">この識別子は 0 をし、コンポーネントの文字列が NULL の場合、ページに関連付けられているヘルプはありません。</span><span class="sxs-lookup"><span data-stu-id="5d64f-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5d64f-127">備考</span><span class="sxs-lookup"><span data-stu-id="5d64f-127">Remarks</span></span>

<span data-ttu-id="5d64f-128">**DTBLPAGE**構造体では、タブ付きページの関連するダイアログ ボックスがいくつかの区切りに使用するコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5d64f-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="5d64f-129">通常、これらのダイアログ ボックスは、構成、メッセージ、または受信者のオプションを表示するためのプロパティ シートです。</span><span class="sxs-lookup"><span data-stu-id="5d64f-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="5d64f-130">タブをクリックすると、ユーザーは別に 1 つのシートからに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="5d64f-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="5d64f-131">コンポーネントと文字列のコンテキストの識別子では、詳しいヘルプは、タブ付きページで使用できるかどうかに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d64f-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="5d64f-132">拡張ヘルプが利用可能な場合は、コンポーネントの文字列とコンテキストの識別子はへのアクセス方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d64f-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="5d64f-133">コンポーネントの文字列は、ヘルプ ファイルにマップします。初期のヘルプ トピックのコンテキストの識別子にマップします。</span><span class="sxs-lookup"><span data-stu-id="5d64f-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="5d64f-134">コンテキスト id は、0 され、コンポーネントの文字列が NULL の場合、拡張ヘルプは使用できません。</span><span class="sxs-lookup"><span data-stu-id="5d64f-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="5d64f-135">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d64f-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="5d64f-136">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d64f-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5d64f-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d64f-137">See also</span></span>



[<span data-ttu-id="5d64f-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="5d64f-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="5d64f-139">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="5d64f-139">MAPI Structures</span></span>](mapi-structures.md)

