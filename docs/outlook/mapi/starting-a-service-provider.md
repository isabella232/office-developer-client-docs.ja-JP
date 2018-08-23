---
title: サービス プロバイダーの開始
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: d14a9961002d63733423af474e147ec5001051fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586334"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="c7b66-103">サービス プロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="c7b66-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="c7b66-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7b66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7b66-105">ある時点で、クライアントで MAPI セッションを開始した後、サービス ・ プロバイダーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="c7b66-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="c7b66-106">トランスポート プロバイダーは、クライアントがそのサービスの要求を行うときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="c7b66-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="c7b66-107">アドレス帳、メッセージ ストア プロバイダーは、クライアントのログオン処理中に開始されます。</span><span class="sxs-lookup"><span data-stu-id="c7b66-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="c7b66-108">クライアントは、各プロファイルおよび特定のメッセージ ストア プロバイダーをロードするのには[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)に含まれているアドレス帳プロバイダーをロードする[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c7b66-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="c7b66-109">メッセージ サービスの一部であるアドレス帳プロバイダーは、サービスの他のプロバイダーのいずれかの前に開始されます。</span><span class="sxs-lookup"><span data-stu-id="c7b66-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="c7b66-110">MAPI は、次の手順でアクティブなプロファイルの各サービス プロバイダーを起動します。</span><span class="sxs-lookup"><span data-stu-id="c7b66-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="c7b66-111">プロファイルにその DLL の名前を検索しています。</span><span class="sxs-lookup"><span data-stu-id="c7b66-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="c7b66-112">Mapisvc.inf の構成ファイルのプロファイルに表示されるように、プロバイダー DLL の名前を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7b66-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="c7b66-113">個別に、またはメッセージ サービスの一環として、プロファイルに、サービス プロバイダーを追加するときは、プロファイルに、プロバイダーに適用される、Mapisvc.inf から **[サービス プロバイダー]** セクションのすべてコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c7b66-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="c7b66-114">Mapisvc.inf の構造の詳細については、 [MapiSvc.inf のファイル形式](file-format-of-mapisvc-inf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7b66-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="c7b66-115">DLL を読み込むには、 **LoadLibrary**の Windows API 関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="c7b66-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="c7b66-116">MAPI は、初回のみまたはそのいずれかの方法に関係なくかどうかそれが既に読み込まれています) は、サービス プロバイダーの DLL を使用するたびに**LoadLibrary**を呼び出し、ため、サービス ・ プロバイダーを行ってはいけません、読み込まれる回数についての前提条件。</span><span class="sxs-lookup"><span data-stu-id="c7b66-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="c7b66-117">**LoadLibrary**への呼び出しごとに、MAPI が**終わった**とき、サービス ・ プロバイダー DLL が不要になった Windows API 関数の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="c7b66-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="c7b66-118">プロバイダーのエントリ ポイント関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="c7b66-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="c7b66-119">MAPI は、ログオン プロセスを開始するは、プロバイダーのエントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c7b66-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="c7b66-120">エントリ ポイント関数では、MAPI が使用しているバージョンと互換性のあるサービス プロバイダー インターフェイス (SPI) のバージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c7b66-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="c7b66-121">これらの関数は、新しく作成したプロバイダーのオブジェクトにポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c7b66-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="c7b66-122">エントリの作成の詳細については関数を使用してプロバイダーのポイントは、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7b66-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7b66-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7b66-123">See also</span></span>



[<span data-ttu-id="c7b66-124">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c7b66-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

