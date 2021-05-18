---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412976"
---
# <a name="flaglist"></a><span data-ttu-id="469f5-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="469f5-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="469f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="469f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="469f5-105">名前解決プロセス中のアドレス エントリの状態を示すために使用されるフラグの一覧が含まれる。</span><span class="sxs-lookup"><span data-stu-id="469f5-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="469f5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="469f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="469f5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="469f5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="469f5-108">Members</span><span class="sxs-lookup"><span data-stu-id="469f5-108">Members</span></span>

 <span data-ttu-id="469f5-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="469f5-109">**cFlags**</span></span>
  
> <span data-ttu-id="469f5-110">リスト内の MAPI で定義されたフラグの数。</span><span class="sxs-lookup"><span data-stu-id="469f5-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="469f5-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="469f5-111">**ulFlags**</span></span>
  
> <span data-ttu-id="469f5-112">受信者の名前解決操作の状態を提供するフラグの配列。</span><span class="sxs-lookup"><span data-stu-id="469f5-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="469f5-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="469f5-113">The following flags can be set:</span></span>
    
<span data-ttu-id="469f5-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="469f5-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="469f5-115">受信者は解決されましたが、一意のエントリ識別子には解決されません。</span><span class="sxs-lookup"><span data-stu-id="469f5-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="469f5-116">他のアドレス帳コンテナーは、この受信者の解決を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="469f5-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="469f5-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="469f5-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="469f5-118">受信者が一意のエントリ識別子に解決されました。</span><span class="sxs-lookup"><span data-stu-id="469f5-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="469f5-119">他のアドレス帳コンテナーは、この受信者の解決を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="469f5-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="469f5-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="469f5-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="469f5-121">エントリが解決されていない。</span><span class="sxs-lookup"><span data-stu-id="469f5-121">The entry has not been resolved.</span></span> <span data-ttu-id="469f5-122">他のアドレス帳コンテナーは、この受信者の解決を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="469f5-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="469f5-123">注釈</span><span class="sxs-lookup"><span data-stu-id="469f5-123">Remarks</span></span>

<span data-ttu-id="469f5-124">**FLAGLIST 構造体** は [、IABContainer::ResolveNames のパラメーターとして使用されます](iabcontainer-resolvenames.md)。</span><span class="sxs-lookup"><span data-stu-id="469f5-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="469f5-125">解決する各受信者は [、ADRLIST 構造に含](adrlist.md) まれています。</span><span class="sxs-lookup"><span data-stu-id="469f5-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="469f5-126">アドレス帳コンテナーは、各受信者を解決しようとして **、FLAGLIST** 構造内の対応するエントリに適切なフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="469f5-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="469f5-127">**FLAGLIST** 構造体のすべてのエントリは **、ADRLIST** 構造体のエントリと同じ順序です。</span><span class="sxs-lookup"><span data-stu-id="469f5-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="469f5-128">これにより、フラグ設定を受信者に簡単に関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="469f5-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="469f5-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="469f5-129">See also</span></span>



[<span data-ttu-id="469f5-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="469f5-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="469f5-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="469f5-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="469f5-132">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="469f5-132">MAPI Structures</span></span>](mapi-structures.md)

