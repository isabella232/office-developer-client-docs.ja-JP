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
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439556"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="e5877-103">サービス プロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="e5877-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="e5877-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5877-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5877-105">クライアントが MAPI とのセッションを開始した後のある時点で、サービス プロバイダーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="e5877-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="e5877-106">トランスポート プロバイダーは、クライアントがサービスの要求を行う際に開始されます。</span><span class="sxs-lookup"><span data-stu-id="e5877-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="e5877-107">アドレス帳とメッセージ ストア プロバイダーは、クライアントのログオン プロセス中に開始されます。</span><span class="sxs-lookup"><span data-stu-id="e5877-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="e5877-108">クライアントは [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) を呼び出して、プロファイルに含まれる各アドレス帳プロバイダーと [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) を読み込み、特定のメッセージ ストア プロバイダーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="e5877-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="e5877-109">メッセージ サービスの一部であるアドレス帳プロバイダーは、サービス内の他のプロバイダーの前に開始されます。</span><span class="sxs-lookup"><span data-stu-id="e5877-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="e5877-110">MAPI は、次の手順を実行して、アクティブ なプロファイル内の各サービス プロバイダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="e5877-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="e5877-111">プロファイル内の DLL の名前を検索します。</span><span class="sxs-lookup"><span data-stu-id="e5877-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="e5877-112">プロバイダー DLL がプロファイルに表示されるのを確認するには、Mapisvc.inf 構成ファイルにプロバイダー DLL の名前を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5877-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="e5877-113">サービス プロバイダーが個別に、またはメッセージ サービスの一部としてプロファイルに追加される場合、プロバイダーに適用される Mapisvc.inf の [サービス プロバイダー **]** セクションはすべてプロファイルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="e5877-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="e5877-114">Mapisvc.inf の構造の詳細については [、「MapiSvc.inf のファイル形式」を参照してください](file-format-of-mapisvc-inf.md)。</span><span class="sxs-lookup"><span data-stu-id="e5877-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="e5877-115">DLL を読みWindows API 関数 **LoadLibrary** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5877-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="e5877-116">MAPI は、(既に読み込まれているかどうかに関係なく) サービス プロバイダー DLL を使用する度に **LoadLibrary** を呼び出すので、サービス プロバイダーは、読み込まれる回数を前提としなくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5877-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="e5877-117">**LoadLibrary** を呼び出すごとに、MAPI はサービス プロバイダー DLL が不要になったWindows API 関数 **FreeLibrary** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5877-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="e5877-118">プロバイダーのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5877-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="e5877-119">MAPI は、ログオン プロセスを開始するためにプロバイダーのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5877-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="e5877-120">エントリ ポイント関数は、MAPI で使用されているバージョンと互換性のあるバージョンのサービス プロバイダー インターフェイス (SPI) を使用している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5877-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="e5877-121">これらの関数は、新しく作成されたプロバイダー オブジェクトへのポインターも返します。</span><span class="sxs-lookup"><span data-stu-id="e5877-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="e5877-122">プロバイダーのエントリ ポイント関数の作成の詳細については、「Service Provider Entry Point Function の実装」 [を参照してください](implementing-a-service-provider-entry-point-function.md)。</span><span class="sxs-lookup"><span data-stu-id="e5877-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5877-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5877-123">See also</span></span>



[<span data-ttu-id="e5877-124">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e5877-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

