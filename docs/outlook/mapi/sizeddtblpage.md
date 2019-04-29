---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407446"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="f2e30-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="f2e30-103">SizedDtblPage</span></span>

<span data-ttu-id="f2e30-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2e30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2e30-105">タブ付きページコントロールを記述するための[dtblpage](dtblpage.md)構造体、指定された長さのラベル、および指定された長さのヘルプファイルのエントリを含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="f2e30-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2e30-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f2e30-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2e30-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2e30-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f2e30-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="f2e30-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f2e30-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="f2e30-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="f2e30-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2e30-110">Parameters</span></span>

<span data-ttu-id="f2e30-111">_n_</span><span class="sxs-lookup"><span data-stu-id="f2e30-111">_n_</span></span>
  
> <span data-ttu-id="f2e30-112">[ページ] タブのラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="f2e30-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="f2e30-113">_n1_</span><span class="sxs-lookup"><span data-stu-id="f2e30-113">_n1_</span></span>
  
> <span data-ttu-id="f2e30-114">タブ付きページコントロールで使用するヘルプファイルを識別する、mapisvc.inf ファイルに表示されるエントリの長さ。</span><span class="sxs-lookup"><span data-stu-id="f2e30-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="f2e30-115">_u_</span><span class="sxs-lookup"><span data-stu-id="f2e30-115">_u_</span></span>
  
> <span data-ttu-id="f2e30-116">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2e30-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2e30-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f2e30-117">Remarks</span></span>

<span data-ttu-id="f2e30-118">**sizeddtblpage**マクロを使用すると、関連付けられたラベルの文字数とヘルプファイルのエントリがわかっている場合に、タブ付きページコントロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="f2e30-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="f2e30-119">次のメンバーで新しい構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f2e30-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="f2e30-120">**sizeddtblpage**マクロの結果として得られる構造体へのポインターを**dtblpage**構造ポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="f2e30-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="f2e30-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2e30-121">See also</span></span>

- [<span data-ttu-id="f2e30-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="f2e30-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="f2e30-123">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="f2e30-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

