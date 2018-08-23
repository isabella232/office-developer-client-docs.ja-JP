---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572565"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="76948-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="76948-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="76948-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76948-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76948-105">並べ替え順の指定した数値を含む名前付き[SSortOrderSet](ssortorderset.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="76948-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76948-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="76948-106">Header file:</span></span>  <br/> |<span data-ttu-id="76948-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76948-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="76948-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="76948-108">Related structure:</span></span>  <br/> |<span data-ttu-id="76948-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="76948-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="76948-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76948-110">Parameters</span></span>

<span data-ttu-id="76948-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="76948-111">__csort_</span></span>
  
> <span data-ttu-id="76948-112">新しい構造体に含まれる並べ替え順序の数です。</span><span class="sxs-lookup"><span data-stu-id="76948-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="76948-113">__名_</span><span class="sxs-lookup"><span data-stu-id="76948-113">__name_</span></span>
  
> <span data-ttu-id="76948-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="76948-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76948-115">注釈</span><span class="sxs-lookup"><span data-stu-id="76948-115">Remarks</span></span>

<span data-ttu-id="76948-116">明示的な境界を使用して設定の並べ替え順序を作成するのにには、 **SizedSSortOrderSet**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="76948-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="76948-117">**SSortOrderSet**構造体へのポインターとしての**SizedSSortOrderSet**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="76948-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="76948-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="76948-118">See also</span></span>

- [<span data-ttu-id="76948-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="76948-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="76948-120">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="76948-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

