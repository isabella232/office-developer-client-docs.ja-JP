---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336415"
---
# <a name="ssubrestriction"></a><span data-ttu-id="c2d45-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="c2d45-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="c2d45-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2d45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2d45-105">メッセージの添付ファイルまたは受信者テーブルの行をフィルター処理するために使用されるサブオブジェクト制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2d45-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2d45-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c2d45-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2d45-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2d45-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="c2d45-108">Members</span><span class="sxs-lookup"><span data-stu-id="c2d45-108">Members</span></span>

 <span data-ttu-id="c2d45-109">**ulsubobject の**</span><span class="sxs-lookup"><span data-stu-id="c2d45-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="c2d45-110">制限のターゲットとして機能するサブオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="c2d45-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="c2d45-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c2d45-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="c2d45-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="c2d45-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="c2d45-113">メッセージの受信者テーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="c2d45-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="c2d45-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="c2d45-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="c2d45-115">メッセージの添付ファイルテーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="c2d45-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="c2d45-116">**lpres**</span><span class="sxs-lookup"><span data-stu-id="c2d45-116">**lpRes**</span></span>
  
> <span data-ttu-id="c2d45-117">[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c2d45-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c2d45-118">解説</span><span class="sxs-lookup"><span data-stu-id="c2d45-118">Remarks</span></span>

<span data-ttu-id="c2d45-119">サブオブジェクトの制限は、すべてのテーブルでサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c2d45-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="c2d45-120">通常、フォルダーの内容のテーブルと検索結果のフォルダーのみがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c2d45-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="c2d45-121">たとえば、サブオブジェクトの制限を使用して、特定の種類の添付ファイルまたは受信者を持つメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="c2d45-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="c2d45-122">実装がサブオブジェクトの制限をサポートしていない場合は、 [IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)メソッドから MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="c2d45-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="c2d45-123">制限のしくみについての一般的な説明については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2d45-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2d45-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2d45-124">See also</span></span>



[<span data-ttu-id="c2d45-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c2d45-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="c2d45-126">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="c2d45-126">MAPI Structures</span></span>](mapi-structures.md)

