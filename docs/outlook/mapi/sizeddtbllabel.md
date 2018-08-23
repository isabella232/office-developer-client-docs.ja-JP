---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803937"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="32650-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="32650-103">SizedDtblLabel</span></span>

<span data-ttu-id="32650-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="32650-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="32650-105">Label コントロールと関連付けられている指定された長さのラベルを記述するための[DTBLLABEL](dtbllabel.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="32650-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32650-106">ヘッダー ファイルに指定します。</span><span class="sxs-lookup"><span data-stu-id="32650-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="32650-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32650-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="32650-108">関連の構造</span><span class="sxs-lookup"><span data-stu-id="32650-108">Related structure</span></span>  <br/> |<span data-ttu-id="32650-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="32650-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="32650-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32650-110">Parameters</span></span>

<span data-ttu-id="32650-111">_n_</span><span class="sxs-lookup"><span data-stu-id="32650-111">_n_</span></span>
  
> <span data-ttu-id="32650-112">ラベルの長さです。</span><span class="sxs-lookup"><span data-stu-id="32650-112">Length of the label.</span></span> <span data-ttu-id="32650-113">これには、終了の NULL 文字が含まれます。</span><span class="sxs-lookup"><span data-stu-id="32650-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="32650-114">_u_</span><span class="sxs-lookup"><span data-stu-id="32650-114">_u_</span></span>
  
> <span data-ttu-id="32650-115">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="32650-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32650-116">注釈</span><span class="sxs-lookup"><span data-stu-id="32650-116">Remarks</span></span>

<span data-ttu-id="32650-117">**SizedDtblLabel**マクロを使用して、ラベルの文字数がわかっている場合、表示テーブルのラベルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="32650-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="32650-118">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="32650-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="32650-119">**DTBLLABEL**構造体のポインターとして、 **SizedDtblLabel**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="32650-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="32650-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="32650-120">See also</span></span>

- [<span data-ttu-id="32650-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="32650-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="32650-122">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="32650-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

