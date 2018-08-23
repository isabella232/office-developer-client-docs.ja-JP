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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803920"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="d4eb9-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="d4eb9-103">SizedDtblEdit</span></span>

<span data-ttu-id="d4eb9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4eb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4eb9-105">エディット コントロールと、コントロールに入力できる文字の最大数を記述するための[DTBLEDIT](dtbledit.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4eb9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d4eb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="d4eb9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4eb9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d4eb9-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d4eb9-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="d4eb9-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="d4eb9-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d4eb9-110">Parameters</span></span>

<span data-ttu-id="d4eb9-111">_n_</span><span class="sxs-lookup"><span data-stu-id="d4eb9-111">_n_</span></span>
  
> <span data-ttu-id="d4eb9-112">エディット コントロールに入力できる文字の最大数。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="d4eb9-113">_u_</span><span class="sxs-lookup"><span data-stu-id="d4eb9-113">_u_</span></span>
  
> <span data-ttu-id="d4eb9-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4eb9-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d4eb9-115">Remarks</span></span>

<span data-ttu-id="d4eb9-116">**SizedDtblEdit**マクロを使用して、有効な文字の数がわかっている場合は、エディット コントロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="d4eb9-117">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="d4eb9-118">**DTBLEDIT**構造体のポインターとして、 **SizedDtblEdit**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="d4eb9-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="d4eb9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4eb9-119">See also</span></span>

- [<span data-ttu-id="d4eb9-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="d4eb9-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="d4eb9-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="d4eb9-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

