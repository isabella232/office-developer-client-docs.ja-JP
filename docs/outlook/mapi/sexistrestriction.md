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
ms.openlocfilehash: 62b5a42a540a4fb96761c45cd51c510f12225e9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803901"
---
# <a name="sexistrestriction"></a><span data-ttu-id="28035-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="28035-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="28035-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28035-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28035-105">テーブル内の列として、特定のプロパティが存在するかどうかをテストするために既存の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="28035-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28035-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="28035-106">Header file:</span></span>  <br/> |<span data-ttu-id="28035-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28035-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="28035-108">Members</span><span class="sxs-lookup"><span data-stu-id="28035-108">Members</span></span>

 <span data-ttu-id="28035-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="28035-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="28035-110">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28035-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="28035-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="28035-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="28035-112">プロパティ タグが各行の存在をテストするのには、列を識別します。</span><span class="sxs-lookup"><span data-stu-id="28035-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="28035-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="28035-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="28035-114">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28035-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28035-115">注釈</span><span class="sxs-lookup"><span data-stu-id="28035-115">Remarks</span></span>

<span data-ttu-id="28035-116">既存の制限は、他の種類のプロパティとコンテンツの制限などのプロパティに関連する制限の意味のある結果を保証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="28035-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="28035-117">プロパティが含まれている制限が[IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)に渡され、プロパティが存在しない、制限の結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="28035-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="28035-118">既存の制限のプロパティの制限を結合して**** 制限を作成すると、呼び出し元を正確な結果保証することができます。</span><span class="sxs-lookup"><span data-stu-id="28035-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="28035-119">存在タイプ PT_OBJECT サブオブジェクトのプロパティを使用して制限を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="28035-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="28035-120">**SExistRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28035-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="28035-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="28035-121">See also</span></span>



[<span data-ttu-id="28035-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="28035-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="28035-123">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="28035-123">MAPI Structures</span></span>](mapi-structures.md)

