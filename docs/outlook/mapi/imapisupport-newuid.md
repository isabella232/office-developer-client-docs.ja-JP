---
title: IMAPISupportNewUID
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800763"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="fdb0f-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="fdb0f-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="fdb0f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fdb0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fdb0f-105">一意の識別子として使用する新しい[MAPIUID](mapiuid.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="fdb0f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fdb0f-106">Parameters</span></span>

 <span data-ttu-id="fdb0f-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="fdb0f-107">_lpMuid_</span></span>
  
> <span data-ttu-id="fdb0f-108">新しい**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fdb0f-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fdb0f-109">Return value</span></span>

<span data-ttu-id="fdb0f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fdb0f-110">S_OK</span></span> 
  
> <span data-ttu-id="fdb0f-111">新しい**MAPIUID**構造体が作成されました。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fdb0f-112">備考</span><span class="sxs-lookup"><span data-stu-id="fdb0f-112">Remarks</span></span>

<span data-ttu-id="fdb0f-113">サポートのすべてのオブジェクトの**IMAPISupport::NewUID**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="fdb0f-114">サービス プロバイダーおよびメッセージ サービスは、長期的な一意の識別子を生成する必要があるたびに**NewUID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="fdb0f-115">メッセージは、たとえば、プロバイダーを格納、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティに新しく作成したメッセージを配置するには**MAPIUID**を取得する**NewUID**を呼び出すことがあります。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="fdb0f-116">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="fdb0f-116">Notes to callers</span></span>

<span data-ttu-id="fdb0f-117">**NewUID**メソッドを作成する**MAPIUID**構造体でのログオン時に登録する**MAPIUID**構造体を混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="fdb0f-118">メッセージが MAPI プロバイダーを格納し、別のプロバイダーを作成するエントリの識別子を区別するために使用または[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出すときに登録する**MAPIUID**構造体は、アドレス帳を表します。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="fdb0f-119">この**MAPIUID**の構造体は、ハード コーディングされ、 **NewUID**を呼び出すことによって取得されませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdb0f-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fdb0f-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="fdb0f-120">See also</span></span>



[<span data-ttu-id="fdb0f-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fdb0f-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="fdb0f-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fdb0f-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

