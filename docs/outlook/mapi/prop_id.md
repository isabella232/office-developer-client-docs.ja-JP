---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ad4b9d3f7c2ca1766ecca4fe9467fc49098f2212
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803695"
---
# <a name="propid"></a><span data-ttu-id="a0c2d-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="a0c2d-103">PROP_ID</span></span>

  
  
<span data-ttu-id="a0c2d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0c2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0c2d-105">指定されたプロパティ タグのプロパティの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0c2d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a0c2d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0c2d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0c2d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a0c2d-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="a0c2d-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a0c2d-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="a0c2d-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0c2d-110">Parameters</span></span>

 <span data-ttu-id="a0c2d-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="a0c2d-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="a0c2d-112">返される識別子を格納するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0c2d-113">備考</span><span class="sxs-lookup"><span data-stu-id="a0c2d-113">Remarks</span></span>

<span data-ttu-id="a0c2d-114">プロパティのすべてのタグには、下位ワード (ビット 0 ~ 15) のプロパティの型と、上位ワード (16 ~ 31 のビット) のプロパティの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="a0c2d-115">**PROP_ID**マクロは、プロパティの識別子を抽出し返される整数の 15 からビット 0 に入れます。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="a0c2d-116">戻り値の残りのビットは、0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="a0c2d-117">たとえば、 **PROP_ID**マクロは、 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)に渡すための識別子を取得する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="a0c2d-118">**GetNamesFromIDs**は、名前付きプロパティの識別子に関連付けられているプロパティ名を取得します。</span><span class="sxs-lookup"><span data-stu-id="a0c2d-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0c2d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0c2d-119">See also</span></span>



[<span data-ttu-id="a0c2d-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a0c2d-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a0c2d-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="a0c2d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

