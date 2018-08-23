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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803972"
---
# <a name="smapiverbarray"></a><span data-ttu-id="0755f-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="0755f-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="0755f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0755f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0755f-105">MAPI の動詞を記述する[SMAPIVerb](smapiverb.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0755f-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0755f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0755f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0755f-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="0755f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="0755f-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0755f-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="0755f-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="0755f-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="0755f-110">Members</span><span class="sxs-lookup"><span data-stu-id="0755f-110">Members</span></span>

 <span data-ttu-id="0755f-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="0755f-111">**cForms**</span></span>
  
> <span data-ttu-id="0755f-112">配列内の動詞の数です。</span><span class="sxs-lookup"><span data-stu-id="0755f-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="0755f-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="0755f-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="0755f-114">MAPI の動詞の配列です。</span><span class="sxs-lookup"><span data-stu-id="0755f-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0755f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="0755f-115">Remarks</span></span>

<span data-ttu-id="0755f-116">**SMAPIVerbArray**構造体は、 [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="0755f-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0755f-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="0755f-117">See also</span></span>



[<span data-ttu-id="0755f-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="0755f-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="0755f-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0755f-119">MAPI Structures</span></span>](mapi-structures.md)

