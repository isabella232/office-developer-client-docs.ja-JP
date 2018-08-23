---
title: サービス プロバイダー一意識別子の登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bde7ff73f58c8809d2dd6467daea28461e7c6ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586271"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="69fee-103">サービス プロバイダー一意識別子の登録</span><span class="sxs-lookup"><span data-stu-id="69fee-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="69fee-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69fee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69fee-105">アドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、さまざまな種類のサービス オブジェクトを登録するのには、 [MAPIUID](mapiuid.md)と呼ばれる一意の識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="69fee-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="69fee-106">の**MAPIUID**は、GUID を格納する 16 バイトの識別子です。</span><span class="sxs-lookup"><span data-stu-id="69fee-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="69fee-107">次の手順を使用して、 **MAPIUID**を作成します。</span><span class="sxs-lookup"><span data-stu-id="69fee-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="69fee-108">定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="69fee-108">Define a constant.</span></span>
    
2. <span data-ttu-id="69fee-109">Visual Studio の *[GUID の作成*を呼び出す \* ツールです。</span><span class="sxs-lookup"><span data-stu-id="69fee-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="69fee-110">たとえば、アドレス帳プロバイダーとの**MAPIUID**を定義するヘッダー ファイルに次の定数場合があります。</span><span class="sxs-lookup"><span data-stu-id="69fee-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="69fee-111">**プロバイダーがアドレス帳またはメッセージ ストア プロバイダーの場合、MAPIUID を登録するのには**</span><span class="sxs-lookup"><span data-stu-id="69fee-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="69fee-112">[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="69fee-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="69fee-113">各ログオン用の**MAPIUID**を登録するオブジェクトのインスタンスを作成して、 **ab**のメンバーを作成するすべてのエントリの識別子の最初の 16 バイトにこの**MAPIUID**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="69fee-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="69fee-114">MAPI は、サービス プロバイダーとオブジェクトを関連付けるには、 **MAPIUID**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="69fee-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="69fee-115">開くには、MAPI オブジェクトの[IMAPISession::OpenEntry](imapisession-openentry.md)メソッドは、 **MAPIUID**の部分のエントリ id を調べ、クライアント呼び出しに対して、登録されている**MAPIUID**、ログオン オブジェクトを決定することと一致する必要がありますが表示される、開く要求します。</span><span class="sxs-lookup"><span data-stu-id="69fee-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="69fee-116">プロバイダーが、トランスポートの場合は、MAPI は、 **IXPLogon::AddressTypes**メソッドを呼び出すと、1 つまたは複数の**MAPIUID**構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="69fee-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="69fee-117">MAPI は、メッセージ配信のための責任を割り当てるには、トランスポート プロバイダーが登録されている**MAPIUID**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="69fee-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="69fee-118">サービス プロバイダーは、通常、1 つの**MAPIUID**を登録するが、複数の**MAPIUID**構造体を登録できます。</span><span class="sxs-lookup"><span data-stu-id="69fee-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="69fee-119">場合は、アドレス帳やメッセージ ストア プロバイダーをサポートしています複数のログオン オブジェクトでは、おそらく、プロファイルには、プロバイダーの複数のインスタンスを追加するユーザーを許可して、ログオン オブジェクトごとに別の**MAPIUID**を実装する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="69fee-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="69fee-120">複数の**MAPIUID**をサポートするその他の理由はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="69fee-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="69fee-121">プロバイダーの複数のバージョンをサポートする必要があり、エントリ id は適切なバージョンを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="69fee-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="69fee-122">バージョンごとに別の**MAPIUID**を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="69fee-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="69fee-123">サポートするオブジェクトの種類を区別するには。</span><span class="sxs-lookup"><span data-stu-id="69fee-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="69fee-124">たとえば、アドレス帳プロバイダーは 1 つの**MAPIUID**でのメッセージングのユーザー オブジェクトのエントリ id を使用して配布リストを使用する別の**MAPIUID**を登録する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="69fee-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="69fee-125">同時にアクティブになっている複数のログオン オブジェクトが存在する場合、合理的ごとに一意の**MAPIUID**構造体を持つ。</span><span class="sxs-lookup"><span data-stu-id="69fee-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="69fee-126">MAPI サービス プロバイダーへのエントリの識別子と一致していくつかの作業を保存する精度が向上します。</span><span class="sxs-lookup"><span data-stu-id="69fee-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="69fee-127">すべてログオン オブジェクトでは、独自の一意の識別子を持っていると、MAPI ことを保証できるいずれかの要求をログオン オブジェクトへのルートは、そのオブジェクトで処理できます。</span><span class="sxs-lookup"><span data-stu-id="69fee-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="69fee-128">ログオン オブジェクトでは、 **MAPIUID**構造体を共有している場合、MAPI は**MAPIUID**によって識別される最初のログオン オブジェクトに要求をルーティングします。</span><span class="sxs-lookup"><span data-stu-id="69fee-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="69fee-129">ログオン オブジェクトの 1 つは、エントリの識別子を処理しないために処理できない要求を受信する場合は、エラーを返す前に、次のログオン オブジェクトに要求を渡します。</span><span class="sxs-lookup"><span data-stu-id="69fee-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69fee-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="69fee-130">See also</span></span>



[<span data-ttu-id="69fee-131">サービス プロバイダー ログオンの実装</span><span class="sxs-lookup"><span data-stu-id="69fee-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

