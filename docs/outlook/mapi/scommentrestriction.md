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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589183"
---
# <a name="scommentrestriction"></a><span data-ttu-id="cf83f-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="cf83f-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="cf83f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf83f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf83f-105">制限の注釈を付けるためには、コメントの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf83f-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf83f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cf83f-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf83f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf83f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="cf83f-108">Members</span><span class="sxs-lookup"><span data-stu-id="cf83f-108">Members</span></span>

 <span data-ttu-id="cf83f-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="cf83f-109">**cValues**</span></span>
  
> <span data-ttu-id="cf83f-110">**LpProp**メンバーが指す配列内のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="cf83f-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="cf83f-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="cf83f-111">**lpRes**</span></span>
  
> <span data-ttu-id="cf83f-112">[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf83f-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="cf83f-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="cf83f-113">**lpProp**</span></span>
  
> <span data-ttu-id="cf83f-114">プロパティ タグと名前付きプロパティの値をそれぞれ含む[SPropValue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf83f-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf83f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="cf83f-115">Remarks</span></span>

<span data-ttu-id="cf83f-116">**SCommentRestriction**構造体は、一連の名前付きプロパティとオブジェクトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cf83f-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="cf83f-117">コメントの制限は他の制限とは異なりは評価されません。</span><span class="sxs-lookup"><span data-stu-id="cf83f-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="cf83f-118">[IMAPITable::Restrict](imapitable-restrict.md)メソッドによって、それらは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cf83f-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="cf83f-119">**IMAPITable::Restrict**の呼び出しが行われた後に、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドによって返された行には影響はありません。</span><span class="sxs-lookup"><span data-stu-id="cf83f-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="cf83f-120">ディスクに保存するときに、制限のあるアプリケーション固有の情報を保持する**SCommentRestriction**構造体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf83f-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="cf83f-121">たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントことができますでこれを**SCommentRestriction**構造体。</span><span class="sxs-lookup"><span data-stu-id="cf83f-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="cf83f-122">プロパティ タグのみが関連する[SPropertyRestriction](spropertyrestriction.md)構造体に格納されているために、プロパティの名前を保存するプロパティの制限のことはできません。</span><span class="sxs-lookup"><span data-stu-id="cf83f-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="cf83f-123">**SCommentRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf83f-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf83f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf83f-124">See also</span></span>



[<span data-ttu-id="cf83f-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cf83f-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="cf83f-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="cf83f-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="cf83f-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cf83f-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="cf83f-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="cf83f-128">MAPI Structures</span></span>](mapi-structures.md)

