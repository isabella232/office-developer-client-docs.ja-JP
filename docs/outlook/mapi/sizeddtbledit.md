---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437645"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="ecc3d-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="ecc3d-103">SizedDtblEdit</span></span>

<span data-ttu-id="ecc3d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecc3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecc3d-105">編集コントロールを記述するための [DTBLEDIT](dtbledit.md) 構造と、コントロールに入力できる最大文字数を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="ecc3d-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecc3d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ecc3d-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecc3d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecc3d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ecc3d-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="ecc3d-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ecc3d-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="ecc3d-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="ecc3d-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ecc3d-110">Parameters</span></span>

<span data-ttu-id="ecc3d-111">_n_</span><span class="sxs-lookup"><span data-stu-id="ecc3d-111">_n_</span></span>
  
> <span data-ttu-id="ecc3d-112">編集コントロールに入力できる最大文字数。</span><span class="sxs-lookup"><span data-stu-id="ecc3d-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="ecc3d-113">_u_</span><span class="sxs-lookup"><span data-stu-id="ecc3d-113">_u_</span></span>
  
> <span data-ttu-id="ecc3d-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="ecc3d-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecc3d-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ecc3d-115">Remarks</span></span>

<span data-ttu-id="ecc3d-116">**SizedDtblEdit マクロ** を使用すると、有効な文字の数が分かっているときに編集コントロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="ecc3d-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="ecc3d-117">新しい構造は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="ecc3d-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="ecc3d-118">**SizedDtblEdit** マクロから生成される構造へのポインターを **DTBLEDIT** 構造ポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="ecc3d-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="ecc3d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecc3d-119">See also</span></span>

- [<span data-ttu-id="ecc3d-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="ecc3d-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="ecc3d-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="ecc3d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

