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
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804005"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="1d3e2-103">サービス プロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="1d3e2-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="1d3e2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d3e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d3e2-105">ある時点で、クライアントで MAPI セッションを開始した後、サービス ・ プロバイダーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="1d3e2-106">トランスポート プロバイダーは、クライアントがそのサービスの要求を行うときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="1d3e2-107">アドレス帳、メッセージ ストア プロバイダーは、クライアントのログオン処理中に開始されます。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="1d3e2-108">クライアントは、各プロファイルおよび特定のメッセージ ストア プロバイダーをロードするのには[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)に含まれているアドレス帳プロバイダーをロードする[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="1d3e2-109">メッセージ サービスの一部であるアドレス帳プロバイダーは、サービスの他のプロバイダーのいずれかの前に開始されます。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="1d3e2-110">MAPI は、次の手順でアクティブなプロファイルの各サービス プロバイダーを起動します。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="1d3e2-111">プロファイルにその DLL の名前を検索しています。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="1d3e2-112">Mapisvc.inf の構成ファイルのプロファイルに表示されるように、プロバイダー DLL の名前を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="1d3e2-113">個別に、またはメッセージ サービスの一環として、プロファイルに、サービス プロバイダーを追加するときは、プロファイルに、プロバイダーに適用される、Mapisvc.inf から **[サービス プロバイダー]** セクションのすべてコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="1d3e2-114">Mapisvc.inf の構造の詳細については、 [MapiSvc.inf のファイル形式](file-format-of-mapisvc-inf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="1d3e2-115">DLL を読み込むには、 **LoadLibrary**の Windows API 関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="1d3e2-116">MAPI は、初回のみまたはそのいずれかの方法に関係なくかどうかそれが既に読み込まれています) は、サービス プロバイダーの DLL を使用するたびに**LoadLibrary**を呼び出し、ため、サービス ・ プロバイダーを行ってはいけません、読み込まれる回数についての前提条件。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="1d3e2-117">**LoadLibrary**への呼び出しごとに、MAPI が**終わった**とき、サービス ・ プロバイダー DLL が不要になった Windows API 関数の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="1d3e2-118">プロバイダーのエントリ ポイント関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="1d3e2-119">MAPI は、ログオン プロセスを開始するは、プロバイダーのエントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="1d3e2-120">エントリ ポイント関数では、MAPI が使用しているバージョンと互換性のあるサービス プロバイダー インターフェイス (SPI) のバージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="1d3e2-121">これらの関数は、新しく作成したプロバイダーのオブジェクトにポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="1d3e2-122">エントリの作成の詳細については関数を使用してプロバイダーのポイントは、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d3e2-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d3e2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d3e2-123">See also</span></span>



[<span data-ttu-id="1d3e2-124">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1d3e2-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

