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
# <a name="scommentrestriction"></a><span data-ttu-id="8808d-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="8808d-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="8808d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8808d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8808d-105">制限に注釈を付けるコメント制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="8808d-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8808d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8808d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8808d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8808d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="8808d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8808d-108">Members</span></span>

 <span data-ttu-id="8808d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8808d-109">**cValues**</span></span>
  
> <span data-ttu-id="8808d-110">**lpProp** メンバーが指す配列内のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="8808d-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="8808d-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="8808d-111">**lpRes**</span></span>
  
> <span data-ttu-id="8808d-112">[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8808d-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="8808d-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="8808d-113">**lpProp**</span></span>
  
> <span data-ttu-id="8808d-114">名前付きプロパティのプロパティ タグと値を含む [SPropValue](spropvalue.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8808d-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8808d-115">注釈</span><span class="sxs-lookup"><span data-stu-id="8808d-115">Remarks</span></span>

<span data-ttu-id="8808d-116">**SCommentRestriction 構造体は**、オブジェクトを名前付きプロパティのセットと関連付ける。</span><span class="sxs-lookup"><span data-stu-id="8808d-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="8808d-117">コメントの制限は、評価されないので、他の制限とは異なっています。</span><span class="sxs-lookup"><span data-stu-id="8808d-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="8808d-118">つまり [、IMAPITable::Restrict メソッドでは無視](imapitable-restrict.md) されます。</span><span class="sxs-lookup"><span data-stu-id="8808d-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="8808d-119">IMAPITable::Restrict 呼び出しが行われた後[、IMAPITable::QueryRows](imapitable-queryrows.md)メソッドによって返される行には影響しません。 </span><span class="sxs-lookup"><span data-stu-id="8808d-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="8808d-120">**SCommentRestriction 構造** を使用すると、アプリケーション固有の情報をディスクに保存するときに制限を付け続けることができます。</span><span class="sxs-lookup"><span data-stu-id="8808d-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="8808d-121">たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントは **、SCommentRestriction** 構造で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8808d-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="8808d-122">関連付けられた [SPropertyRestriction](spropertyrestriction.md) 構造体にはプロパティ タグしか保持されないので、プロパティの制限ではプロパティ名を保存できない。</span><span class="sxs-lookup"><span data-stu-id="8808d-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="8808d-123">**SCommentRestriction** 構造と制限全般の詳細については、「制限について」[を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="8808d-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8808d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="8808d-124">See also</span></span>



[<span data-ttu-id="8808d-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8808d-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8808d-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="8808d-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="8808d-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8808d-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="8808d-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8808d-128">MAPI Structures</span></span>](mapi-structures.md)

