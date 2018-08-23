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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803682"
---
# <a name="proptag"></a><span data-ttu-id="d7a6e-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="d7a6e-103">PROP_TAG</span></span>

<span data-ttu-id="d7a6e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7a6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7a6e-105">指定したプロパティの型と識別子を組み合わせることによって作成されたプロパティ タグを返します。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7a6e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d7a6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7a6e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7a6e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d7a6e-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="d7a6e-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d7a6e-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="d7a6e-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d7a6e-110">Parameters</span></span>

<span data-ttu-id="d7a6e-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="d7a6e-111">_ulPropType_</span></span>
  
> <span data-ttu-id="d7a6e-112">新しいプロパティ タグのプロパティの型。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="d7a6e-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="d7a6e-113">_ulPropID_</span></span>
  
> <span data-ttu-id="d7a6e-114">新しいプロパティ タグのプロパティの識別子です。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7a6e-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d7a6e-115">Remarks</span></span>

<span data-ttu-id="d7a6e-116">**プロペラ\_タグ**マクロは型の_ulPropType_と_ulPropID_で指定されている識別子のプロパティのプロパティ タグを作成します。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="d7a6e-117">たとえば、次のように、 **PROP_TAG**マクロを使用してエントリ識別子のプロパティ タグを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="d7a6e-118">PT_BINARY で、プロパティの型が返されるプロパティ タグの下位 16 ビットに含まれているし、上位 16 ビットが 0 xffff のプロパティ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="d7a6e-119">プロパティ タグの詳細については、 [MAPI プロパティ タグ](mapi-property-tags.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7a6e-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7a6e-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7a6e-120">See also</span></span>

- [<span data-ttu-id="d7a6e-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d7a6e-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d7a6e-122">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="d7a6e-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

