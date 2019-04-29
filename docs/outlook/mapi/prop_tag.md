---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425884"
---
# <a name="proptag"></a><span data-ttu-id="03e7d-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="03e7d-103">PROP_TAG</span></span>

<span data-ttu-id="03e7d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03e7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03e7d-105">指定したプロパティの種類と識別子を結合して作成されたプロパティタグを返します。</span><span class="sxs-lookup"><span data-stu-id="03e7d-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03e7d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="03e7d-106">Header file:</span></span>  <br/> |<span data-ttu-id="03e7d-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03e7d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="03e7d-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="03e7d-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="03e7d-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="03e7d-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="03e7d-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="03e7d-110">Parameters</span></span>

<span data-ttu-id="03e7d-111">_ulproptype_</span><span class="sxs-lookup"><span data-stu-id="03e7d-111">_ulPropType_</span></span>
  
> <span data-ttu-id="03e7d-112">新しいプロパティタグのプロパティの種類。</span><span class="sxs-lookup"><span data-stu-id="03e7d-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="03e7d-113">_ulpropid_</span><span class="sxs-lookup"><span data-stu-id="03e7d-113">_ulPropID_</span></span>
  
> <span data-ttu-id="03e7d-114">新しいプロパティタグのプロパティ識別子。</span><span class="sxs-lookup"><span data-stu-id="03e7d-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03e7d-115">注釈</span><span class="sxs-lookup"><span data-stu-id="03e7d-115">Remarks</span></span>

<span data-ttu-id="03e7d-116">**PROP\_タグ**マクロは、 _ulproptype_型のプロパティと_ulpropid_で指定された識別子のプロパティタグを作成します。</span><span class="sxs-lookup"><span data-stu-id="03e7d-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="03e7d-117">たとえば、エントリ識別子のプロパティタグは、次のように**PROP_TAG**マクロを使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="03e7d-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="03e7d-118">返される property タグの下位16ビットには、プロパティの型 PT_BINARY が含まれており、上位16ビットにはプロパティ識別子の0xffff が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03e7d-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="03e7d-119">プロパティタグの詳細については、「 [MAPI プロパティタグ](mapi-property-tags.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03e7d-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03e7d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="03e7d-120">See also</span></span>

- [<span data-ttu-id="03e7d-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="03e7d-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="03e7d-122">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="03e7d-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

