---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563871"
---
# <a name="sizedentryid"></a><span data-ttu-id="26e42-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="26e42-103">SizedENTRYID</span></span>

<span data-ttu-id="26e42-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26e42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26e42-105">指定したサイズの**ab**のメンバーを含む名前付き[エントリ ID](entryid.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="26e42-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26e42-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="26e42-106">Header file:</span></span>  <br/> |<span data-ttu-id="26e42-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26e42-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="26e42-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="26e42-108">Related structure:</span></span>  <br/> |<span data-ttu-id="26e42-109">**エントリ ID**</span><span class="sxs-lookup"><span data-stu-id="26e42-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="26e42-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26e42-110">Parameters</span></span>

<span data-ttu-id="26e42-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="26e42-111">__cb_</span></span>
  
> <span data-ttu-id="26e42-112">**Ab**の新しい構造体のメンバーのバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="26e42-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="26e42-113">__名_</span><span class="sxs-lookup"><span data-stu-id="26e42-113">__name_</span></span>
  
> <span data-ttu-id="26e42-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="26e42-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26e42-115">注釈</span><span class="sxs-lookup"><span data-stu-id="26e42-115">Remarks</span></span>

<span data-ttu-id="26e42-116">**SizedENTRYID**マクロを使用して、配列の長さの要件を認識した後に、エントリの識別子を定義できます。</span><span class="sxs-lookup"><span data-stu-id="26e42-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="26e42-117">明示的な境界を持つエントリ識別子を作成するのにには、このマクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="26e42-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="26e42-118">**エントリ ID**の構造体へのポインターとしての**SizedENTRYID**マクロから得られる新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="26e42-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="26e42-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="26e42-119">See also</span></span>

- [<span data-ttu-id="26e42-120">エントリ ID</span><span class="sxs-lookup"><span data-stu-id="26e42-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="26e42-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="26e42-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

