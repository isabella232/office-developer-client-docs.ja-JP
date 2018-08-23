---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583940"
---
# <a name="sizedsrowset"></a><span data-ttu-id="3fe7b-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="3fe7b-103">SizedSRowSet</span></span>

<span data-ttu-id="3fe7b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fe7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fe7b-105">指定された行数を格納する名前付き[SRowSet](srowset.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="3fe7b-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fe7b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3fe7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3fe7b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3fe7b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3fe7b-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="3fe7b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="3fe7b-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="3fe7b-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="3fe7b-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3fe7b-110">Parameters</span></span>

<span data-ttu-id="3fe7b-111">__クロウズ_</span><span class="sxs-lookup"><span data-stu-id="3fe7b-111">__crow_</span></span>
  
> <span data-ttu-id="3fe7b-112">新しい構造体に含まれる行の数のカウントです。</span><span class="sxs-lookup"><span data-stu-id="3fe7b-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="3fe7b-113">__名_</span><span class="sxs-lookup"><span data-stu-id="3fe7b-113">__name_</span></span>
  
> <span data-ttu-id="3fe7b-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="3fe7b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fe7b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="3fe7b-115">Remarks</span></span>

<span data-ttu-id="3fe7b-116">**SRowSet**構造体へのポインターとしての**SizedSRowSet**マクロから得られる新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3fe7b-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="3fe7b-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="3fe7b-117">See also</span></span>

- [<span data-ttu-id="3fe7b-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="3fe7b-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="3fe7b-119">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="3fe7b-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

