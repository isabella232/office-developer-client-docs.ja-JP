---
title: CHANGE_PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CHANGE_PROP_TYPE
api_type:
- COM
ms.assetid: 95513b5a-fd3b-46f2-a6c0-094500ae4ca7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 26dfd40ed8b4cd2b2261abff4d2692de46acb6fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799786"
---
# <a name="changeproptype"></a><span data-ttu-id="849ff-103">CHANGE_PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="849ff-103">CHANGE_PROP_TYPE</span></span>

  
  
<span data-ttu-id="849ff-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="849ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="849ff-105">プロパティ タグのプロパティの型を指定した値に更新されます。</span><span class="sxs-lookup"><span data-stu-id="849ff-105">Updates the property type of a property tag to a specified value.</span></span> <span data-ttu-id="849ff-106">プロパティの識別子は変更はありません。</span><span class="sxs-lookup"><span data-stu-id="849ff-106">The property identifier is unchanged.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="849ff-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="849ff-107">Header file:</span></span>  <br/> |<span data-ttu-id="849ff-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="849ff-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="849ff-109">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="849ff-109">Related structure:</span></span>  <br/> |[<span data-ttu-id="849ff-110">SPropValue</span><span class="sxs-lookup"><span data-stu-id="849ff-110">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
CHANGE_PROP_TYPE (ulPropTag, ulPropType)
```

## <a name="parameters"></a><span data-ttu-id="849ff-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="849ff-111">Parameters</span></span>

 <span data-ttu-id="849ff-112">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="849ff-112">_ulPropTag_</span></span>
  
> <span data-ttu-id="849ff-113">変更するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="849ff-113">The property tag to be modified.</span></span>
    
 <span data-ttu-id="849ff-114">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="849ff-114">_ulPropType_</span></span>
  
> <span data-ttu-id="849ff-115">プロパティの型の新しい値。</span><span class="sxs-lookup"><span data-stu-id="849ff-115">The new value for the property type.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="849ff-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="849ff-116">See also</span></span>



[<span data-ttu-id="849ff-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="849ff-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="849ff-118">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="849ff-118">Macros Related to Structures</span></span>](macros-related-to-structures.md)

