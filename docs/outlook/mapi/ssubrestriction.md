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
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581959"
---
# <a name="ssubrestriction"></a><span data-ttu-id="d92e3-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="d92e3-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="d92e3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d92e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d92e3-105">メッセージの添付ファイルや受信者テーブルの行をフィルター処理に使用されるサブ オブジェクトの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="d92e3-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d92e3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d92e3-106">Header file:</span></span>  <br/> |<span data-ttu-id="d92e3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d92e3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="d92e3-108">Members</span><span class="sxs-lookup"><span data-stu-id="d92e3-108">Members</span></span>

 <span data-ttu-id="d92e3-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="d92e3-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="d92e3-110">制限の対象となる下位のオブジェクトの種類です。</span><span class="sxs-lookup"><span data-stu-id="d92e3-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="d92e3-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d92e3-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="d92e3-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="d92e3-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="d92e3-113">メッセージの受信者テーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="d92e3-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="d92e3-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="d92e3-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="d92e3-115">メッセージの添付ファイル テーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="d92e3-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="d92e3-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="d92e3-116">**lpRes**</span></span>
  
> <span data-ttu-id="d92e3-117">[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d92e3-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d92e3-118">注釈</span><span class="sxs-lookup"><span data-stu-id="d92e3-118">Remarks</span></span>

<span data-ttu-id="d92e3-119">サブ オブジェクトの制限事項は、すべてのテーブルではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d92e3-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="d92e3-120">通常、だけフォルダーの内容をテーブルと、検索結果のフォルダーでは、それらをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d92e3-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="d92e3-121">などの特定の種類の添付ファイル、または受信者がメッセージを検索するのには下位のオブジェクトの制限が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d92e3-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="d92e3-122">実装が下位のオブジェクトの制限をサポートしていない場合、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドまたは[IMAPITable::FindRow](imapitable-findrow.md)メソッドから MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="d92e3-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="d92e3-123">制限のしくみの概要については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d92e3-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d92e3-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="d92e3-124">See also</span></span>



[<span data-ttu-id="d92e3-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d92e3-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="d92e3-126">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d92e3-126">MAPI Structures</span></span>](mapi-structures.md)

