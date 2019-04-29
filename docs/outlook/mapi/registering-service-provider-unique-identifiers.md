---
title: サービスプロバイダーの一意識別子の登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410176"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="cf3c9-103">サービスプロバイダーの一意識別子の登録</span><span class="sxs-lookup"><span data-stu-id="cf3c9-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="cf3c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf3c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf3c9-105">アドレス帳、メッセージストア、およびトランスポートプロバイダーは、 [MAPIUID](mapiuid.md)と呼ばれる一意の識別子を使用して、さまざまな種類のサービスオブジェクトに登録します。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="cf3c9-106">**MAPIUID**は、GUID を含む16バイトの識別子です。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="cf3c9-107">次の手順を使用して、 **MAPIUID**を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="cf3c9-108">定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-108">Define a constant.</span></span>
    
2. <span data-ttu-id="cf3c9-109">Visual Studio の [*GUID の作成*] ツールを起動します。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="cf3c9-110">たとえば、アドレス帳プロバイダーでは、 **MAPIUID**を定義するために、ヘッダーファイルに次の定数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="cf3c9-111">**プロバイダーがアドレス帳またはメッセージストアプロバイダーの場合に MAPIUID を登録するには**</span><span class="sxs-lookup"><span data-stu-id="cf3c9-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="cf3c9-112">Call [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="cf3c9-113">インスタンス化された各ログオンオブジェクトに対して**MAPIUID**を登録し、作成するすべてのエントリ識別子の**ab**メンバーの最初の16バイトにこの**MAPIUID**を含めます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="cf3c9-114">MAPI では、 **MAPIUID**構造を使用してオブジェクトをサービスプロバイダーに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="cf3c9-115">クライアントが[imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出してオブジェクトを開くと、MAPI はエントリ識別子の**MAPIUID**部分を調べ、登録されている**MAPIUID**と照合して、開いているログオンオブジェクトを特定します。タキ.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="cf3c9-116">プロバイダーがトランスポートの場合は、MAPI が**IXPLogon:: AddressTypes**メソッドを呼び出すときに1つ以上の**MAPIUID**構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="cf3c9-117">MAPI は、トランスポートプロバイダーによって登録された**MAPIUID**構造を使用して、メッセージ配信の責任を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="cf3c9-118">通常、サービスプロバイダーは1つの**MAPIUID**を登録しますが、複数の**MAPIUID**構造体を登録することは可能です。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="cf3c9-119">ユーザーが自分のプロファイルにプロバイダーの複数のインスタンスを追加することを許可することによって、アドレス帳またはメッセージストアプロバイダーが複数のログオンオブジェクトをサポートしている場合は、各ログオンオブジェクトに異なる**MAPIUID**を実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="cf3c9-120">複数の**MAPIUID**をサポートする理由は、他にもいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="cf3c9-121">プロバイダーの複数のバージョンをサポートする必要があります。また、エントリ識別子は適切なバージョンを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="cf3c9-122">各バージョンに異なる**MAPIUID**を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="cf3c9-123">サポートするオブジェクトの種類を区別する場合。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="cf3c9-124">たとえば、アドレス帳プロバイダーは、メッセージングユーザーオブジェクトのエントリ識別子で使用する1つの**MAPIUID**と、配布リストに使用する別の**MAPIUID**を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="cf3c9-125">同時にアクティブな複数のログオンオブジェクトがある場合は、それぞれに固有の**MAPIUID**構造があるという意味になります。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="cf3c9-126">これにより、MAPI がサービスプロバイダーにエントリ識別子を一致させ、一部の作業を節約できるため、精度が向上します。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="cf3c9-127">すべてのログオンオブジェクトに固有の識別子がある場合、MAPI は、ログオンオブジェクトにルーティングするすべての要求がそのオブジェクトによって処理されることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="cf3c9-128">ログオンオブジェクトが**MAPIUID**構造を共有する場合、MAPI は、 **MAPIUID**によって識別される最初のログオンオブジェクトに要求をルーティングします。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="cf3c9-129">ログオンオブジェクトのいずれかがエントリ識別子を処理できないため処理できないという要求を受信した場合は、エラーを返す前に、要求を次のログオンオブジェクトに渡します。</span><span class="sxs-lookup"><span data-stu-id="cf3c9-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf3c9-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf3c9-130">See also</span></span>



[<span data-ttu-id="cf3c9-131">サービスプロバイダーログオンの実装</span><span class="sxs-lookup"><span data-stu-id="cf3c9-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

