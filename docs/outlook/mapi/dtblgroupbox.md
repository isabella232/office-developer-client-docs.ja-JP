---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438394"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="70739-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="70739-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="70739-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70739-105">表示テーブルから作成されたダイアログ ボックスで使用されるグループ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="70739-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70739-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="70739-106">Header file:</span></span>  <br/> |<span data-ttu-id="70739-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70739-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="70739-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="70739-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="70739-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="70739-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="70739-110">Members</span><span class="sxs-lookup"><span data-stu-id="70739-110">Members</span></span>

 <span data-ttu-id="70739-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="70739-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="70739-112">グループ ボックスに付く文字列のメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="70739-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="70739-113">表示されている場合は、ボックスの左上にラベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="70739-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="70739-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="70739-114">**ulFlags**</span></span>
  
> <span data-ttu-id="70739-115">**ulbLpszLabel** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="70739-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="70739-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="70739-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="70739-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70739-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70739-118">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="70739-118">The label is in Unicode format.</span></span> <span data-ttu-id="70739-119">このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="70739-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70739-120">注釈</span><span class="sxs-lookup"><span data-stu-id="70739-120">Remarks</span></span>

<span data-ttu-id="70739-121">**DTBLGROUPBOX** 構造は、ダイアログ ボックス内の他のコントロールを視覚的に関連付けるグループ ボックス コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="70739-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="70739-122">強調表示の手法では、他のコントロールをボックスで囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="70739-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="70739-123">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="70739-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="70739-124">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="70739-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="70739-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="70739-125">See also</span></span>



[<span data-ttu-id="70739-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="70739-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="70739-127">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="70739-127">MAPI Structures</span></span>](mapi-structures.md)

