---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339278"
---
# <a name="sexistrestriction"></a><span data-ttu-id="ccb2c-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="ccb2c-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="ccb2c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccb2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccb2c-105">特定のプロパティがテーブル内の列として存在するかどうかをテストするために使用される存在制限を記述します。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccb2c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ccb2c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ccb2c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ccb2c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="ccb2c-108">Members</span><span class="sxs-lookup"><span data-stu-id="ccb2c-108">Members</span></span>

 <span data-ttu-id="ccb2c-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="ccb2c-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="ccb2c-110">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="ccb2c-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="ccb2c-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="ccb2c-112">各行に存在するかどうかをテストする列を識別するプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="ccb2c-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="ccb2c-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="ccb2c-114">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccb2c-115">解説</span><span class="sxs-lookup"><span data-stu-id="ccb2c-115">Remarks</span></span>

<span data-ttu-id="ccb2c-116">存在する制限は、プロパティやコンテンツの制限など、プロパティに関連する他の種類の制限について有意義な結果を保証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="ccb2c-117">プロパティを含む制限が[IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)に渡され、プロパティが存在しない場合、制限の結果は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="ccb2c-118">プロパティ制限に参加する**と**制限が存在し、制限が存在することにより、発信者が正確な結果を保証できます。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="ccb2c-119">存在する制限は、PT_OBJECT 型のサブオブジェクトのプロパティでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="ccb2c-120">**sexistrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccb2c-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ccb2c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="ccb2c-121">See also</span></span>



[<span data-ttu-id="ccb2c-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="ccb2c-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="ccb2c-123">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ccb2c-123">MAPI Structures</span></span>](mapi-structures.md)

