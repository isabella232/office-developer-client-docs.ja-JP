---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803928"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="eaab4-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="eaab4-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="eaab4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eaab4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eaab4-105">グループ ボックス コントロールと指定した長さのラベルを記述するための[DTBLGROUPBOX](dtblgroupbox.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eaab4-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eaab4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="eaab4-106">Header file:</span></span>  <br/> |<span data-ttu-id="eaab4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eaab4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eaab4-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="eaab4-108">Related structure:</span></span>  <br/> |<span data-ttu-id="eaab4-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="eaab4-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="eaab4-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="eaab4-110">Parameters</span></span>

<span data-ttu-id="eaab4-111">_n_</span><span class="sxs-lookup"><span data-stu-id="eaab4-111">_n_</span></span>
  
> <span data-ttu-id="eaab4-112">グループ ボックスのラベルの長さです。</span><span class="sxs-lookup"><span data-stu-id="eaab4-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="eaab4-113">_u_</span><span class="sxs-lookup"><span data-stu-id="eaab4-113">_u_</span></span>
  
> <span data-ttu-id="eaab4-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="eaab4-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaab4-115">備考</span><span class="sxs-lookup"><span data-stu-id="eaab4-115">Remarks</span></span>

<span data-ttu-id="eaab4-116">**SizedDtblGroupBox**マクロを使用して、ラベルの長さがわかっている場合、グループ ボックス コントロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="eaab4-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="eaab4-117">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="eaab4-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="eaab4-118">**DTBLGROUPBOX**構造体のポインターとして、 **SizedDtblGroupBox**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="eaab4-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="eaab4-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="eaab4-119">See also</span></span>

- [<span data-ttu-id="eaab4-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="eaab4-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="eaab4-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="eaab4-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

