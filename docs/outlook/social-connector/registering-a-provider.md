---
title: プロバイダーの登録
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: このトピックでは、Outlook ソーシャル コネクタ (OSC) プロバイダーをインストールするときに使用される Windows のレジストリの場所について説明します。
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804452"
---
# <a name="registering-a-provider"></a><span data-ttu-id="3051e-103">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="3051e-103">Registering a provider</span></span>

<span data-ttu-id="3051e-104">このトピックでは、Outlook ソーシャル コネクタ (OSC) プロバイダーをインストールするときに使用される Windows のレジストリの場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="3051e-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="3051e-105">COM の登録</span><span class="sxs-lookup"><span data-stu-id="3051e-105">COM registration</span></span>

<span data-ttu-id="3051e-106">OSC プロバイダーのインストール中に、COM 登録または regsvr32 を使用して登録するのには DLL を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3051e-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="3051e-107">OSC プロバイダーを登録するプロバイダーの DLL の COM 登録、`HKEY_CLASSES_ROOT`のレジストリ ハイブです。</span><span class="sxs-lookup"><span data-stu-id="3051e-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="3051e-108">OSC プロバイダーがマネージ コードで開発されたは、プロバイダー アセンブリを COM 参照可能です。</span><span class="sxs-lookup"><span data-stu-id="3051e-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="3051e-109">プロバイダー コンポーネントの個別のアプリケーション ドメインを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3051e-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="3051e-110">それ以外の場合、OSC プロバイダーは、他のコンポーネントによって使用される既定の共有のアプリケーション ドメインを使用し、期待どおりに、プロバイダーが動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3051e-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="3051e-111">プロバイダーの ProgID を登録します。</span><span class="sxs-lookup"><span data-stu-id="3051e-111">Registering provider ProgID</span></span>

<span data-ttu-id="3051e-112">各 OSC プロバイダーは、プログラム識別子を登録する必要があります (`ProgID`)。</span><span class="sxs-lookup"><span data-stu-id="3051e-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="3051e-113">プロバイダーのインストーラーは、次の場所を追加または削除のいずれかを選択できます、 `ProgID`。</span><span class="sxs-lookup"><span data-stu-id="3051e-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="3051e-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーが現在ログオンしているユーザーだけにインストールされている場合に、プロバイダーのインストーラーがこの場所を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3051e-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="3051e-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーは、コンピューター上のすべてのユーザーに対してインストールされている場合に、プロバイダーのインストーラーがこの場所を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3051e-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="3051e-116">OSC プロバイダーの次の`ProgID`で上記の場所では、クライアント コンピューターは、64 ビット Windows オペレーティング システムで実行されている 32 ビットの Outlook を持っていない限り、します。</span><span class="sxs-lookup"><span data-stu-id="3051e-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="3051e-117">このような場合は、プロバイダー インストーラーする必要がありますを選択して次の場所のいずれか、`HKEY_CURRENT_USER`または`HKEY_LOCAL_MACHINE`ハイブ。</span><span class="sxs-lookup"><span data-stu-id="3051e-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="3051e-118">クイック実行バージョンの Office には、プロバイダー インストーラーする必要がありますを選択して次の場所のいずれかの HKEY_CURRENT_USER または HKEY_LOCAL_MACHINE ハイブに。</span><span class="sxs-lookup"><span data-stu-id="3051e-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="3051e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="3051e-119">See also</span></span>

- [<span data-ttu-id="3051e-120">インストールのチェックリスト</span><span class="sxs-lookup"><span data-stu-id="3051e-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="3051e-121">プロバイダーを開発する学習のためのクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="3051e-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="3051e-122">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="3051e-122">Deploying a Provider</span></span>](deploying-a-provider.md)

