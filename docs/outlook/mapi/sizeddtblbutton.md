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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282762"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="b33fa-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="b33fa-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="b33fa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b33fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b33fa-105">ボタンと指定された長さのラベルを記述するための[dtblbutton](dtblbutton.md)構造を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="b33fa-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b33fa-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b33fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="b33fa-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b33fa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b33fa-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="b33fa-108">Related structure:</span></span>  <br/> |<span data-ttu-id="b33fa-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="b33fa-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="b33fa-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b33fa-110">Parameters</span></span>

 <span data-ttu-id="b33fa-111">_n_</span><span class="sxs-lookup"><span data-stu-id="b33fa-111">_n_</span></span>
  
> <span data-ttu-id="b33fa-112">新しい構造に含めるラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="b33fa-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="b33fa-113">_u_</span><span class="sxs-lookup"><span data-stu-id="b33fa-113">_u_</span></span>
  
> <span data-ttu-id="b33fa-114">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b33fa-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b33fa-115">解説</span><span class="sxs-lookup"><span data-stu-id="b33fa-115">Remarks</span></span>

<span data-ttu-id="b33fa-116">次のメンバーで新しい構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b33fa-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="b33fa-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="b33fa-117">See also</span></span>



[<span data-ttu-id="b33fa-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="b33fa-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="b33fa-119">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="b33fa-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

