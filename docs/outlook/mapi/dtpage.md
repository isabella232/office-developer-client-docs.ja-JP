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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408223"
---
# <a name="dtpage"></a><span data-ttu-id="fc2d2-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="fc2d2-103">DTPAGE</span></span>

  
  
<span data-ttu-id="fc2d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc2d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc2d2-105">[BuildDisplayTable](builddisplaytable.md)関数によって表示テーブルから作成されるダイアログ ボックスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc2d2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fc2d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc2d2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc2d2-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="fc2d2-108">Members</span><span class="sxs-lookup"><span data-stu-id="fc2d2-108">Members</span></span>

 <span data-ttu-id="fc2d2-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="fc2d2-109">**cctl**</span></span>
  
> <span data-ttu-id="fc2d2-110">lpctl メンバーが指す **コントロールの** 数。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="fc2d2-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="fc2d2-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="fc2d2-112">ダイアログ ボックス リソースの名前または整数識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="fc2d2-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="fc2d2-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="fc2d2-114">MAPISVC.INF の [ヘルプ ファイル マッピング **]** セクションに表示される文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="fc2d2-115">**lpszComponent** は **ulItemID** メンバーとの共用体にあるため、有効なデータを持つメンバーは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="fc2d2-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="fc2d2-116">**ulItemID**</span></span>
  
> <span data-ttu-id="fc2d2-117">ヘルプ ファイル名を読み取る 65535 以下の値を持つ整数リソース識別子。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="fc2d2-118">**ulItemID は** **lpszComponent** メンバーとの共用体にあるため、有効なデータを持つメンバーは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="fc2d2-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="fc2d2-119">**lpctl**</span></span>
  
> <span data-ttu-id="fc2d2-120">ページ上のコントロールごとに [1 つ、DTCTL](dtctl.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fc2d2-121">注釈</span><span class="sxs-lookup"><span data-stu-id="fc2d2-121">Remarks</span></span>

<span data-ttu-id="fc2d2-122">タブ付きページのヘルプ ファイルを識別するには **、lpszComponent** メンバーをハードコードされた文字列に設定するか **、ulItemID** メンバーを整数リソース識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="fc2d2-123">MAPISVC の **[ヘルプ ファイル マッピング] セクション** の各エントリ。INF は、左側の 30 文字以内のコンポーネント文字列と、右側のヘルプ ファイル パスで構成されます。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="fc2d2-124">**ulItemID と** **lpszResourceName** の両方が **、BuildDisplayTable**_の hInstance_ パラメーターに含されています。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="fc2d2-125">詳細については [、「MAPISVC」を参照してください。INF [ヘルプ ファイル マッピング] セクション](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="fc2d2-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="fc2d2-126">**BuildDisplayTable は**、この構造を使用してコントロール リソースから表示テーブルを構築しますが **、DTPAGE** 構造は表示テーブル自体には表示されません。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="fc2d2-127">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="fc2d2-128">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="fc2d2-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc2d2-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc2d2-129">See also</span></span>



[<span data-ttu-id="fc2d2-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="fc2d2-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="fc2d2-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="fc2d2-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="fc2d2-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="fc2d2-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="fc2d2-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fc2d2-133">MAPI Structures</span></span>](mapi-structures.md)

