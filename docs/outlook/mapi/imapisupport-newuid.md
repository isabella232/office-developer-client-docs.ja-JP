---
title: imapisupportnewuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330199"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="72ec4-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="72ec4-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="72ec4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72ec4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72ec4-105">一意の識別子として使用する新しい[MAPIUID](mapiuid.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="72ec4-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="72ec4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="72ec4-106">Parameters</span></span>

 <span data-ttu-id="72ec4-107">_lpmuid_</span><span class="sxs-lookup"><span data-stu-id="72ec4-107">_lpMuid_</span></span>
  
> <span data-ttu-id="72ec4-108">新しい**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="72ec4-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="72ec4-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="72ec4-109">Return value</span></span>

<span data-ttu-id="72ec4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="72ec4-110">S_OK</span></span> 
  
> <span data-ttu-id="72ec4-111">新しい**MAPIUID**構造が作成されました。</span><span class="sxs-lookup"><span data-stu-id="72ec4-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="72ec4-112">解説</span><span class="sxs-lookup"><span data-stu-id="72ec4-112">Remarks</span></span>

<span data-ttu-id="72ec4-113">**imapisupport:: newuid**メソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="72ec4-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="72ec4-114">サービスプロバイダーとメッセージサービスは、長期の一意の識別子を生成する必要があるときに、 **newuid**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="72ec4-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="72ec4-115">たとえば、メッセージストアプロバイダーは**newuid**を呼び出して、新しく作成されたメッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティに入れる**MAPIUID**を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="72ec4-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="72ec4-116">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="72ec4-116">Notes to callers</span></span>

<span data-ttu-id="72ec4-117">ログオン時に登録した**MAPIUID**構造を、 **newuid**メソッドが作成する**MAPIUID**構造体と混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="72ec4-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="72ec4-118">[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出すときに登録する**MAPIUID**構造は、アドレス帳またはメッセージストアプロバイダーを MAPI に対して表し、さまざまなプロバイダーが作成するエントリ識別子を区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="72ec4-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="72ec4-119">この**MAPIUID**構造体は、ハードコーディングされている必要があり、 **newuid**への呼び出しによって取得されることはありません。</span><span class="sxs-lookup"><span data-stu-id="72ec4-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72ec4-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="72ec4-120">See also</span></span>



[<span data-ttu-id="72ec4-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="72ec4-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="72ec4-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="72ec4-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

