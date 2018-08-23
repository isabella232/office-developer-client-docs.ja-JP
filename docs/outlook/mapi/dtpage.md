---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 769ae984e4b6e8610ca7909ea2ac714d9d04d698
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589673"
---
# <a name="dtpage"></a><span data-ttu-id="e2328-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="e2328-103">DTPAGE</span></span>

  
  
<span data-ttu-id="e2328-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2328-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2328-105">[BuildDisplayTable](builddisplaytable.md)関数によって、表示された表から組み込まれているダイアログ ボックスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e2328-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2328-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e2328-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2328-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2328-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a><span data-ttu-id="e2328-108">Members</span><span class="sxs-lookup"><span data-stu-id="e2328-108">Members</span></span>

 <span data-ttu-id="e2328-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="e2328-109">**cctl**</span></span>
  
> <span data-ttu-id="e2328-110">**Lpctl**メンバーで指定されたコントロールの数。</span><span class="sxs-lookup"><span data-stu-id="e2328-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="e2328-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="e2328-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="e2328-112">ダイアログ ボックスのリソースの名前または整数の識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2328-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="e2328-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="e2328-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="e2328-114">MAPISVC.INF の **[ヘルプ ファイルのマッピング]** セクションに表示される文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2328-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="e2328-115">**LpszComponent**が**ulItemID**のメンバーを含む共用体であるため、これらのメンバーの 1 つだけが有効なデータです。</span><span class="sxs-lookup"><span data-stu-id="e2328-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="e2328-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="e2328-116">**ulItemID**</span></span>
  
> <span data-ttu-id="e2328-117">ヘルプ ファイル名を読み取ることができますから 65535 以下の値を持つ整数リソース識別子。</span><span class="sxs-lookup"><span data-stu-id="e2328-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="e2328-118">**UlItemID**が**lpszComponent**のメンバーを含む共用体であるため、これらのメンバーの 1 つだけが有効なデータです。</span><span class="sxs-lookup"><span data-stu-id="e2328-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="e2328-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="e2328-119">**lpctl**</span></span>
  
> <span data-ttu-id="e2328-120">ページ上の各コントロールのいずれかの[DTCTL](dtctl.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2328-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2328-121">注釈</span><span class="sxs-lookup"><span data-stu-id="e2328-121">Remarks</span></span>

<span data-ttu-id="e2328-122">タブ付きページのヘルプ ファイルを特定するには、整数リソース識別子にハード コーディングされた文字列への**lpszComponent**のメンバーまたは**ulItemID**のメンバーのいずれかを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2328-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="e2328-123">**[ヘルプ ファイルのマッピング]** セクションには、MAPISVC 内の各エントリで、です。INF は、コンポーネント、文字列の左側と右側のヘルプ ファイルのパスに、30 文字以内で構成されています。</span><span class="sxs-lookup"><span data-stu-id="e2328-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="e2328-124">_HInstance_のパラメーター **BuildDisplayTable**は、 **ulItemID**と**lpszResourceName**の両方を参照ください。</span><span class="sxs-lookup"><span data-stu-id="e2328-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="e2328-125">詳細については、 [MAPISVC を参照してください。INF の [ヘルプ ファイルのマッピング] セクションで](mapisvc-inf-help-file-mappings-section.md)。</span><span class="sxs-lookup"><span data-stu-id="e2328-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="e2328-126">**BuildDisplayTable**では、この構造体を使用して、テーブルを作成、表示コントロールのリソースから表示テーブル自体に**DTPAGE**構造は表示されません。</span><span class="sxs-lookup"><span data-stu-id="e2328-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="e2328-127">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2328-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e2328-128">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2328-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2328-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2328-129">See also</span></span>



[<span data-ttu-id="e2328-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="e2328-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="e2328-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="e2328-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="e2328-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e2328-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e2328-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e2328-133">MAPI Structures</span></span>](mapi-structures.md)

