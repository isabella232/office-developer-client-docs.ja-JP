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
# <a name="dtpage"></a><span data-ttu-id="6b470-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="6b470-103">DTPAGE</span></span>

  
  
<span data-ttu-id="6b470-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b470-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b470-105">[builddisplaytable](builddisplaytable.md)関数によって表示テーブルから構築されたダイアログボックスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b470-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b470-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6b470-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b470-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b470-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="6b470-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="6b470-108">Members</span></span>

 <span data-ttu-id="6b470-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="6b470-109">**cctl**</span></span>
  
> <span data-ttu-id="6b470-110">**lpctl**メンバーが指すコントロールの数。</span><span class="sxs-lookup"><span data-stu-id="6b470-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="6b470-111">**lpszresourcename**</span><span class="sxs-lookup"><span data-stu-id="6b470-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="6b470-112">ダイアログボックスリソースの名前または整数識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b470-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="6b470-113">**lpszcomponent**</span><span class="sxs-lookup"><span data-stu-id="6b470-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="6b470-114">mapisvc.inf の **[Help File Mappings]** セクションに表示される文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b470-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="6b470-115">**lpszcomponent**は**ulitemid**メンバーとの和集合に含まれているため、これらのメンバーのうち1つだけが有効なデータを持っています。</span><span class="sxs-lookup"><span data-stu-id="6b470-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="6b470-116">**ulitemid**</span><span class="sxs-lookup"><span data-stu-id="6b470-116">**ulItemID**</span></span>
  
> <span data-ttu-id="6b470-117">ヘルプファイル名を読み取ることができる65535以下の値を持つ整数リソース識別子。</span><span class="sxs-lookup"><span data-stu-id="6b470-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="6b470-118">**ulitemid**は**lpszcomponent**メンバーと共用されているため、これらのメンバーのうち1つだけが有効なデータを持っています。</span><span class="sxs-lookup"><span data-stu-id="6b470-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="6b470-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="6b470-119">**lpctl**</span></span>
  
> <span data-ttu-id="6b470-120">[DTCTL](dtctl.md)構造体の配列へのポインター。ページ上の各コントロールに対して1つ。</span><span class="sxs-lookup"><span data-stu-id="6b470-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b470-121">注釈</span><span class="sxs-lookup"><span data-stu-id="6b470-121">Remarks</span></span>

<span data-ttu-id="6b470-122">タブページのヘルプファイルを識別するには、 **lpszcomponent**メンバーをハードコーディングされた文字列または**ulitemid**メンバーのいずれかを整数リソース識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="6b470-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="6b470-123">mapisvc.inf の **[Help File Mappings]** セクションの各エントリ。INF は、30文字以内のコンポーネント文字列から構成され、左側には右に、ヘルプファイルのパスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b470-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="6b470-124">**ulitemid**と**lpszresourcename**の両方が**builddisplaytable**の_hInstance_パラメーターにあります。</span><span class="sxs-lookup"><span data-stu-id="6b470-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="6b470-125">詳細については、「mapisvc.inf」を参照してください[。INF [Help File Mappings] セクション](mapisvc-inf-help-file-mappings-section.md)</span><span class="sxs-lookup"><span data-stu-id="6b470-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="6b470-126">**builddisplaytable**は、この構造を使用して、コントロールリソースから表示テーブルを作成しますが、 **dtpage**構造は表示テーブル自体には表示されません。</span><span class="sxs-lookup"><span data-stu-id="6b470-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="6b470-127">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b470-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="6b470-128">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b470-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b470-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b470-129">See also</span></span>



[<span data-ttu-id="6b470-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="6b470-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="6b470-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="6b470-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="6b470-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="6b470-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="6b470-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="6b470-133">MAPI Structures</span></span>](mapi-structures.md)

