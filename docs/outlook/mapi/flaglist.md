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
# <a name="flaglist"></a><span data-ttu-id="3f1d6-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="3f1d6-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="3f1d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f1d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f1d6-105">名前解決プロセス中にアドレスエントリの状態を示すために使用されるフラグの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f1d6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3f1d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f1d6-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f1d6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="3f1d6-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="3f1d6-108">Members</span></span>

 <span data-ttu-id="3f1d6-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="3f1d6-109">**cFlags**</span></span>
  
> <span data-ttu-id="3f1d6-110">リスト内の MAPI 定義フラグの数。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="3f1d6-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3f1d6-111">**ulFlags**</span></span>
  
> <span data-ttu-id="3f1d6-112">受信者の名前解決操作の状態を提供するフラグの配列。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="3f1d6-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-113">The following flags can be set:</span></span>
    
<span data-ttu-id="3f1d6-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="3f1d6-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="3f1d6-115">受信者は解決されましたが、一意のエントリ識別子には対応していません。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="3f1d6-116">他のアドレス帳コンテナーは、この受信者の解決を試みてはなりません。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="3f1d6-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="3f1d6-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="3f1d6-118">受信者が一意のエントリ識別子に解決されました。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="3f1d6-119">他のアドレス帳コンテナーは、この受信者の解決を試みてはなりません。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="3f1d6-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="3f1d6-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="3f1d6-121">エントリは解決されていません。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-121">The entry has not been resolved.</span></span> <span data-ttu-id="3f1d6-122">他のアドレス帳コンテナーは、この受信者の解決を試みます。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f1d6-123">注釈</span><span class="sxs-lookup"><span data-stu-id="3f1d6-123">Remarks</span></span>

<span data-ttu-id="3f1d6-124">**flaglist**構造体は、 [IABContainer:: ResolveNames](iabcontainer-resolvenames.md)のパラメーターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="3f1d6-125">解決される各受信者は、 [adrlist](adrlist.md)構造に含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="3f1d6-126">アドレス帳コンテナーは各受信者の解決を試みたときに、 **flaglist**構造の対応するエントリに適切なフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="3f1d6-127">**flaglist**構造体のすべてのエントリは、 **adrlist**構造内のエントリと同じ順序になっています。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="3f1d6-128">これにより、フラグ設定を受信者に簡単に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="3f1d6-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f1d6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f1d6-129">See also</span></span>



[<span data-ttu-id="3f1d6-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="3f1d6-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="3f1d6-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="3f1d6-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="3f1d6-132">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="3f1d6-132">MAPI Structures</span></span>](mapi-structures.md)

