---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803972"
---
# <a name="smapiverbarray"></a><span data-ttu-id="7f5be-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="7f5be-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="7f5be-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f5be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f5be-105">MAPI の動詞を記述する[SMAPIVerb](smapiverb.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f5be-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f5be-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7f5be-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f5be-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7f5be-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7f5be-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="7f5be-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7f5be-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="7f5be-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="7f5be-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="7f5be-110">Members</span></span>

 <span data-ttu-id="7f5be-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="7f5be-111">**cForms**</span></span>
  
> <span data-ttu-id="7f5be-112">配列内の動詞の数です。</span><span class="sxs-lookup"><span data-stu-id="7f5be-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="7f5be-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="7f5be-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="7f5be-114">MAPI の動詞の配列です。</span><span class="sxs-lookup"><span data-stu-id="7f5be-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f5be-115">備考</span><span class="sxs-lookup"><span data-stu-id="7f5be-115">Remarks</span></span>

<span data-ttu-id="7f5be-116">**SMAPIVerbArray**構造体は、 [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="7f5be-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f5be-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f5be-117">See also</span></span>



[<span data-ttu-id="7f5be-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="7f5be-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="7f5be-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7f5be-119">MAPI Structures</span></span>](mapi-structures.md)

