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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567532"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="28be8-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="28be8-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="28be8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28be8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28be8-105">チェック ボックス コントロールと指定した長さのラベルを記述するための[DTBLCHECKBOX](dtblcheckbox.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="28be8-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28be8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="28be8-106">Header file:</span></span>  <br/> |<span data-ttu-id="28be8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28be8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="28be8-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="28be8-108">Related structure:</span></span>  <br/> |<span data-ttu-id="28be8-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="28be8-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="28be8-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28be8-110">Parameters</span></span>

<span data-ttu-id="28be8-111">_n_</span><span class="sxs-lookup"><span data-stu-id="28be8-111">_n_</span></span>
  
> <span data-ttu-id="28be8-112">新しい構造体に含まれるラベルの長さです。</span><span class="sxs-lookup"><span data-stu-id="28be8-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="28be8-113">_u_</span><span class="sxs-lookup"><span data-stu-id="28be8-113">_u_</span></span>
  
> <span data-ttu-id="28be8-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="28be8-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28be8-115">注釈</span><span class="sxs-lookup"><span data-stu-id="28be8-115">Remarks</span></span>

<span data-ttu-id="28be8-116">**SizedDtblCheckBox**マクロを使用して、ラベルの文字数がわかっている場合は、チェック ボックスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="28be8-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="28be8-117">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="28be8-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="28be8-118">**DTBLCHECKBOX**構造体のポインターとして、 **SizedDtblCheckBox**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="28be8-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="28be8-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="28be8-119">See also</span></span>

- [<span data-ttu-id="28be8-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="28be8-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="28be8-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="28be8-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

