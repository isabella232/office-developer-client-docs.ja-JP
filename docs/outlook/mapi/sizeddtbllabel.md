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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408615"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="d2190-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="d2190-103">SizedDtblLabel</span></span>

<span data-ttu-id="d2190-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2190-105">ラベルコントロールと、指定した長さの関連付けられたラベルを記述するための[dtbllabel](dtbllabel.md)構造を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="d2190-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2190-106">ヘッダーファイルで指定します。</span><span class="sxs-lookup"><span data-stu-id="d2190-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="d2190-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2190-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d2190-108">関連する構造</span><span class="sxs-lookup"><span data-stu-id="d2190-108">Related structure</span></span>  <br/> |<span data-ttu-id="d2190-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="d2190-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="d2190-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2190-110">Parameters</span></span>

<span data-ttu-id="d2190-111">_n_</span><span class="sxs-lookup"><span data-stu-id="d2190-111">_n_</span></span>
  
> <span data-ttu-id="d2190-112">ラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="d2190-112">Length of the label.</span></span> <span data-ttu-id="d2190-113">これには、末尾の NULL 文字が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d2190-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="d2190-114">_u_</span><span class="sxs-lookup"><span data-stu-id="d2190-114">_u_</span></span>
  
> <span data-ttu-id="d2190-115">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2190-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2190-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d2190-116">Remarks</span></span>

<span data-ttu-id="d2190-117">**sizeddtbllabel**マクロを使用すると、ラベル内の文字数が既知の場合に、表示テーブルのラベルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d2190-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="d2190-118">次のメンバーで新しい構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d2190-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="d2190-119">結果の構造体へのポインターを、 **sizeddtbllabel**マクロから**dtbllabel**構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="d2190-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="d2190-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2190-120">See also</span></span>

- [<span data-ttu-id="d2190-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="d2190-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="d2190-122">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="d2190-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

