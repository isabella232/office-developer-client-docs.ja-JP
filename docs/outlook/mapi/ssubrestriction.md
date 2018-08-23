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
ms.openlocfilehash: 152f3032876d6473f1716afa46507196cd5ecc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804001"
---
# <a name="ssubrestriction"></a><span data-ttu-id="eb459-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="eb459-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="eb459-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb459-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb459-105">メッセージの添付ファイルや受信者テーブルの行をフィルター処理に使用されるサブ オブジェクトの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="eb459-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb459-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="eb459-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb459-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb459-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="eb459-108">Members</span><span class="sxs-lookup"><span data-stu-id="eb459-108">Members</span></span>

 <span data-ttu-id="eb459-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="eb459-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="eb459-110">制限の対象となる下位のオブジェクトの種類です。</span><span class="sxs-lookup"><span data-stu-id="eb459-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="eb459-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="eb459-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="eb459-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="eb459-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="eb459-113">メッセージの受信者テーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="eb459-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="eb459-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="eb459-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="eb459-115">メッセージの添付ファイル テーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="eb459-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="eb459-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="eb459-116">**lpRes**</span></span>
  
> <span data-ttu-id="eb459-117">[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb459-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eb459-118">注釈</span><span class="sxs-lookup"><span data-stu-id="eb459-118">Remarks</span></span>

<span data-ttu-id="eb459-119">サブ オブジェクトの制限事項は、すべてのテーブルではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="eb459-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="eb459-120">通常、だけフォルダーの内容をテーブルと、検索結果のフォルダーでは、それらをサポートします。</span><span class="sxs-lookup"><span data-stu-id="eb459-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="eb459-121">などの特定の種類の添付ファイル、または受信者がメッセージを検索するのには下位のオブジェクトの制限が使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb459-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="eb459-122">実装が下位のオブジェクトの制限をサポートしていない場合、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドまたは[IMAPITable::FindRow](imapitable-findrow.md)メソッドから MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="eb459-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="eb459-123">制限のしくみの概要については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb459-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb459-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb459-124">See also</span></span>



[<span data-ttu-id="eb459-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="eb459-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="eb459-126">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="eb459-126">MAPI Structures</span></span>](mapi-structures.md)

