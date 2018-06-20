---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803913"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="c8711-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="c8711-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="c8711-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8711-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8711-105">ボタンと指定された長さのラベルを記述するための[DTBLBUTTON](dtblbutton.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="c8711-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8711-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c8711-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8711-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8711-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c8711-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="c8711-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c8711-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="c8711-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="c8711-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="c8711-110">Parameters</span></span>

 <span data-ttu-id="c8711-111">_n_</span><span class="sxs-lookup"><span data-stu-id="c8711-111">_n_</span></span>
  
> <span data-ttu-id="c8711-112">新しい構造体に含まれるラベルの長さです。</span><span class="sxs-lookup"><span data-stu-id="c8711-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="c8711-113">_u_</span><span class="sxs-lookup"><span data-stu-id="c8711-113">_u_</span></span>
  
> <span data-ttu-id="c8711-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="c8711-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8711-115">備考</span><span class="sxs-lookup"><span data-stu-id="c8711-115">Remarks</span></span>

<span data-ttu-id="c8711-116">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="c8711-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="c8711-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8711-117">See also</span></span>



[<span data-ttu-id="c8711-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="c8711-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="c8711-119">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="c8711-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

