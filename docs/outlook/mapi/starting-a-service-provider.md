---
title: サービスプロバイダーの開始
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341714"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="2678a-103">サービスプロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="2678a-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="2678a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2678a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2678a-105">クライアントが MAPI を使用してセッションを開始した後のある時点では、サービスプロバイダーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2678a-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="2678a-106">クライアントがサービスに対して要求を行うと、トランスポートプロバイダーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2678a-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="2678a-107">アドレス帳およびメッセージストアプロバイダーは、クライアントのログオンプロセス中に開始されます。</span><span class="sxs-lookup"><span data-stu-id="2678a-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="2678a-108">クライアントは[imapisession:: OpenAddressBook](imapisession-openaddressbook.md)を呼び出して、プロファイルに含まれている各アドレス帳プロバイダーと[imapisession:: openmsgstore](imapisession-openmsgstore.md)を読み込んで、特定のメッセージストアプロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="2678a-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="2678a-109">メッセージサービスの一部であるアドレス帳プロバイダーは、サービス内の他のプロバイダーよりも前に開始されます。</span><span class="sxs-lookup"><span data-stu-id="2678a-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="2678a-110">MAPI は、アクティブなプロファイルで各サービスプロバイダーを開始します。そのためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2678a-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="2678a-111">プロファイルに DLL の名前を配置する。</span><span class="sxs-lookup"><span data-stu-id="2678a-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="2678a-112">mapisvc.inf 構成ファイルにプロバイダー DLL の名前を登録して、プロファイルに表示されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="2678a-113">サービスプロバイダーがプロファイルに個別に、またはメッセージサービスの一部として追加されると、プロバイダーに適用される mapisvc.inf の **[サービスプロバイダ]** セクションすべてがプロファイルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2678a-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="2678a-114">mapisvc.inf の構造の詳細については、「 [mapisvc.inf のファイル形式](file-format-of-mapisvc-inf.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2678a-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="2678a-115">DLL を読み込むために\*\*\*\* Windows API 関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="2678a-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="2678a-116">MAPI は、 \*\*\*\* (既に読み込まれているかどうかにかかわらず) サービスプロバイダ DLL を使用するたびに、または初めて実行した場合には、サービスプロバイダーがロードされる回数を想定しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="2678a-117">**LoadLibrary**へのすべての呼び出しでは、サービスプロバイダー DLL が不要になったときに、MAPI が Windows API 関数**FreeLibrary**を呼び出すことになります。</span><span class="sxs-lookup"><span data-stu-id="2678a-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="2678a-118">プロバイダーのエントリポイント関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="2678a-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="2678a-119">MAPI は、プロバイダーのエントリポイント関数を呼び出して、ログオンプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2678a-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="2678a-120">エントリポイント関数 MAPI で使用されているバージョンと互換性のあるバージョンのサービスプロバイダインターフェイス (SPI) を使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2678a-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="2678a-121">これらの関数は、新しく作成されたプロバイダオブジェクトへのポインターも返します。</span><span class="sxs-lookup"><span data-stu-id="2678a-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="2678a-122">プロバイダー用のエントリポイント関数を作成する方法の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2678a-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2678a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2678a-123">See also</span></span>



[<span data-ttu-id="2678a-124">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="2678a-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

