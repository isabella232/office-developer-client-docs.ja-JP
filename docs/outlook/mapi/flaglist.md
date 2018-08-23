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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800074"
---
# <a name="flaglist"></a><span data-ttu-id="1ea8e-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="1ea8e-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="1ea8e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ea8e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ea8e-105">名前解決の処理中にアドレス エントリのステータスを示すために使用されるフラグの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ea8e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1ea8e-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ea8e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ea8e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="1ea8e-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ea8e-108">Members</span></span>

 <span data-ttu-id="1ea8e-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="1ea8e-109">**cFlags**</span></span>
  
> <span data-ttu-id="1ea8e-110">MAPI 定義のフラグを一覧の数です。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="1ea8e-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1ea8e-111">**ulFlags**</span></span>
  
> <span data-ttu-id="1ea8e-112">受信者の名前解決操作のステータスを提供するフラグの配列。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="1ea8e-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-113">The following flags can be set:</span></span>
    
<span data-ttu-id="1ea8e-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="1ea8e-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="1ea8e-115">受信者が解決されていませんが、エントリの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="1ea8e-116">他のアドレス帳コンテナーは、この受信者を解決するのにはいけません。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="1ea8e-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="1ea8e-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="1ea8e-118">受信者は、エントリの一意の識別子に解決されました。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="1ea8e-119">他のアドレス帳コンテナーは、この受信者を解決するのにはいけません。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="1ea8e-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="1ea8e-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="1ea8e-121">エントリは解決されていません。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-121">The entry has not been resolved.</span></span> <span data-ttu-id="1ea8e-122">他のアドレス帳コンテナーは、この受信者を解決するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ea8e-123">注釈</span><span class="sxs-lookup"><span data-stu-id="1ea8e-123">Remarks</span></span>

<span data-ttu-id="1ea8e-124">**FLAGLIST**構造体は、 [IABContainer::ResolveNames](iabcontainer-resolvenames.md)のパラメーターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="1ea8e-125">各受信者を解決するのには、 [ADRLIST](adrlist.md)構造体に含まれます。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="1ea8e-126">アドレス帳コンテナーは、各受信者を解決しようとすると、 **FLAGLIST**構造体に対応するエントリに適切なフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="1ea8e-127">**ADRLIST**構造体のエントリと同じ順序では、 **FLAGLIST**構造体のエントリのすべてです。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="1ea8e-128">これにより、フラグの設定を受信者に関連付けるには簡単です。</span><span class="sxs-lookup"><span data-stu-id="1ea8e-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ea8e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ea8e-129">See also</span></span>



[<span data-ttu-id="1ea8e-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="1ea8e-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="1ea8e-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="1ea8e-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="1ea8e-132">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1ea8e-132">MAPI Structures</span></span>](mapi-structures.md)

