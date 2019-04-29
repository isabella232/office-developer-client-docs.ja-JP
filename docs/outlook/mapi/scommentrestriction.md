---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430610"
---
# <a name="scommentrestriction"></a><span data-ttu-id="fa9c4-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="fa9c4-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="fa9c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa9c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa9c4-105">制限に注釈を付けるために使用されるコメント制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa9c4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fa9c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa9c4-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa9c4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="fa9c4-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="fa9c4-108">Members</span></span>

 <span data-ttu-id="fa9c4-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="fa9c4-109">**cValues**</span></span>
  
> <span data-ttu-id="fa9c4-110">**lpprop**メンバーによって参照されている配列内のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="fa9c4-111">**lpres**</span><span class="sxs-lookup"><span data-stu-id="fa9c4-111">**lpRes**</span></span>
  
> <span data-ttu-id="fa9c4-112">[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="fa9c4-113">**lpprop**</span><span class="sxs-lookup"><span data-stu-id="fa9c4-113">**lpProp**</span></span>
  
> <span data-ttu-id="fa9c4-114">[spropvalue](spropvalue.md)構造体の配列へのポインター。それぞれには、プロパティタグと、名前付きプロパティの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa9c4-115">注釈</span><span class="sxs-lookup"><span data-stu-id="fa9c4-115">Remarks</span></span>

<span data-ttu-id="fa9c4-116">**sコメント制限**構造は、オブジェクトを一連の名前付きプロパティに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="fa9c4-117">コメント制限は、評価されないため、他の制限とは異なります。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="fa9c4-118">つまり、 [IMAPITable:: Restrict](imapitable-restrict.md)メソッドでは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="fa9c4-119">**imapitable:: Restrict**呼び出しが行われた後、 [imapitable:: QueryRows](imapitable-queryrows.md)メソッドによって返される行には影響はありません。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="fa9c4-120">**sコメント制限**構造を使用すると、アプリケーション固有の情報をディスクに保存するときに制限を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="fa9c4-121">たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントは、 **sコメント制限**構造でそのようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="fa9c4-122">プロパティの制限でプロパティ名を保存することはできません。これは、関連付けられた[spropertyrestriction](spropertyrestriction.md)構造体には property タグのみが含まれるためです。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="fa9c4-123">詳細については\*\*\*\* 、「制限[につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa9c4-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa9c4-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa9c4-124">See also</span></span>



[<span data-ttu-id="fa9c4-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fa9c4-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="fa9c4-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fa9c4-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="fa9c4-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="fa9c4-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="fa9c4-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fa9c4-128">MAPI Structures</span></span>](mapi-structures.md)

