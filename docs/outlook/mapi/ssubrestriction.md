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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406326"
---
# <a name="ssubrestriction"></a><span data-ttu-id="dda5e-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="dda5e-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="dda5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dda5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dda5e-105">メッセージの添付ファイルまたは受信者テーブルの行をフィルター処理するために使用されるサブオブジェクト制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="dda5e-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dda5e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dda5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="dda5e-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dda5e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="dda5e-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="dda5e-108">Members</span></span>

 <span data-ttu-id="dda5e-109">**ulsubobject の**</span><span class="sxs-lookup"><span data-stu-id="dda5e-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="dda5e-110">制限のターゲットとして機能するサブオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="dda5e-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="dda5e-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dda5e-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="dda5e-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="dda5e-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="dda5e-113">メッセージの受信者テーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="dda5e-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="dda5e-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="dda5e-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="dda5e-115">メッセージの添付ファイルテーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="dda5e-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="dda5e-116">**lpres**</span><span class="sxs-lookup"><span data-stu-id="dda5e-116">**lpRes**</span></span>
  
> <span data-ttu-id="dda5e-117">[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dda5e-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dda5e-118">注釈</span><span class="sxs-lookup"><span data-stu-id="dda5e-118">Remarks</span></span>

<span data-ttu-id="dda5e-119">サブオブジェクトの制限は、すべてのテーブルでサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="dda5e-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="dda5e-120">通常、フォルダーの内容のテーブルと検索結果のフォルダーのみがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="dda5e-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="dda5e-121">たとえば、サブオブジェクトの制限を使用して、特定の種類の添付ファイルまたは受信者を持つメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="dda5e-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="dda5e-122">実装がサブオブジェクトの制限をサポートしていない場合は、 [IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)メソッドから MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="dda5e-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="dda5e-123">制限のしくみについての一般的な説明については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dda5e-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dda5e-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="dda5e-124">See also</span></span>



[<span data-ttu-id="dda5e-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="dda5e-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="dda5e-126">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="dda5e-126">MAPI Structures</span></span>](mapi-structures.md)

