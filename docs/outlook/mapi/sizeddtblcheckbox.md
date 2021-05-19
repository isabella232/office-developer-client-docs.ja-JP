---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420809"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="4cd9b-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="4cd9b-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="4cd9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cd9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cd9b-105">チェック ボックス コントロールと指定した長さのラベルを記述するための [DTBLCHECKBOX](dtblcheckbox.md) 構造体を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cd9b-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cd9b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4cd9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="4cd9b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cd9b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4cd9b-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="4cd9b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4cd9b-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="4cd9b-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="4cd9b-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4cd9b-110">Parameters</span></span>

<span data-ttu-id="4cd9b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="4cd9b-111">_n_</span></span>
  
> <span data-ttu-id="4cd9b-112">新しい構造に含めるラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="4cd9b-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="4cd9b-113">_u_</span><span class="sxs-lookup"><span data-stu-id="4cd9b-113">_u_</span></span>
  
> <span data-ttu-id="4cd9b-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="4cd9b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4cd9b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="4cd9b-115">Remarks</span></span>

<span data-ttu-id="4cd9b-116">**SizedDtblCheckBox** マクロを使用すると、ラベル文字の数が分かっている場合にチェック ボックスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="4cd9b-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="4cd9b-117">新しい構造は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="4cd9b-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="4cd9b-118">**SizedDtblCheckBox** マクロから生成される構造体へのポインターを **DTBLCHECKBOX** 構造ポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="4cd9b-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="4cd9b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cd9b-119">See also</span></span>

- [<span data-ttu-id="4cd9b-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="4cd9b-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="4cd9b-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="4cd9b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

