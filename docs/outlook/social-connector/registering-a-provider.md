---
title: プロバイダーの登録
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: このトピックでは、Windows ソーシャル コネクタ (OSC) プロバイダーのインストール時に使用Outlookレジストリの場所について説明します。
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421761"
---
# <a name="registering-a-provider"></a><span data-ttu-id="2f221-103">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="2f221-103">Registering a provider</span></span>

<span data-ttu-id="2f221-104">このトピックでは、Windows ソーシャル コネクタ (OSC) プロバイダーのインストール時に使用Outlookレジストリの場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f221-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="2f221-105">COM 登録</span><span class="sxs-lookup"><span data-stu-id="2f221-105">COM registration</span></span>

<span data-ttu-id="2f221-106">インストール時に COM 自己登録または regsvr32 を使用して登録する OSC プロバイダー DLL を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f221-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="2f221-107">プロバイダー DLL の COM 登録は、レジストリ ハイブの下に OSC `HKEY_CLASSES_ROOT` プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="2f221-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="2f221-108">マネージ コードで開発された OSC プロバイダーには、COM に表示されるプロバイダー アセンブリがあります。</span><span class="sxs-lookup"><span data-stu-id="2f221-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="2f221-109">プロバイダー コンポーネントには、別のアプリケーション ドメインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f221-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="2f221-110">それ以外の場合、OSC プロバイダーは、他のコンポーネントで使用される既定の共有アプリケーション ドメインを使用し、プロバイダーが期待した通りに動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2f221-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="2f221-111">プロバイダー ProgID の登録</span><span class="sxs-lookup"><span data-stu-id="2f221-111">Registering provider ProgID</span></span>

<span data-ttu-id="2f221-112">各 OSC プロバイダーは、プログラム識別子 () を登録する必要があります `ProgID` 。</span><span class="sxs-lookup"><span data-stu-id="2f221-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="2f221-113">プロバイダー インストーラーは、次のいずれかの場所を選択して、次の場所を追加または削除できます `ProgID` 。</span><span class="sxs-lookup"><span data-stu-id="2f221-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="2f221-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`プロバイダーが現在ログオンしているユーザーにのみインストールされている場合は、プロバイダーインストーラーでこの &ndash; 場所を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f221-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="2f221-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーインストーラーは、プロバイダーがコンピューター上のすべてのユーザーにインストールされている場合、この場所を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f221-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="2f221-116">OSC は、クライアント コンピューターが 64 ビット オペレーティング システムで 32 ビット Outlookを実行している場合をWindows `ProgID` します。</span><span class="sxs-lookup"><span data-stu-id="2f221-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="2f221-117">このような場合、プロバイダー インストーラーは、次のいずれかの場所またはハイブ内の場所  `HKEY_CURRENT_USER` を選択する必要  `HKEY_LOCAL_MACHINE` があります。</span><span class="sxs-lookup"><span data-stu-id="2f221-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="2f221-118">バージョン 1 クイック実行の場合Officeプロバイダー インストーラーは、次のいずれかの場所を選択する必要があります。HKEY_CURRENT_USERまたはHKEY_LOCAL_MACHINEします。</span><span class="sxs-lookup"><span data-stu-id="2f221-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="2f221-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f221-119">See also</span></span>

- [<span data-ttu-id="2f221-120">インストール チェックリスト</span><span class="sxs-lookup"><span data-stu-id="2f221-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="2f221-121">プロバイダーを開発するための学習のクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="2f221-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="2f221-122">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="2f221-122">Deploying a Provider</span></span>](deploying-a-provider.md)

