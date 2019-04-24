---
title: プロバイダーの登録
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーをインストールするときに使用される Windows レジストリの場所について説明します。
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329212"
---
# <a name="registering-a-provider"></a><span data-ttu-id="89cd6-103">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="89cd6-103">Registering a provider</span></span>

<span data-ttu-id="89cd6-104">このトピックでは、Outlook Social Connector (.osc) プロバイダーをインストールするときに使用される Windows レジストリの場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="89cd6-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="89cd6-105">COM 登録</span><span class="sxs-lookup"><span data-stu-id="89cd6-105">COM registration</span></span>

<span data-ttu-id="89cd6-106">インストール時に COM の自己登録または regsvr32 を使用して登録するように、.osc プロバイダー DLL を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="89cd6-107">プロバイダー DLL の COM 登録は、 `HKEY_CLASSES_ROOT`レジストリハイブの下に、.osc プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="89cd6-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="89cd6-108">マネージコードで開発された .osc プロバイダには、COM で参照できるプロバイダアセンブリがあります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="89cd6-109">プロバイダーコンポーネントには、別のアプリケーションドメインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="89cd6-110">それ以外の場合、.osc プロバイダーは、他のコンポーネントで使用されている既定の共有アプリケーションドメインを使用しますが、プロバイダーは期待どおりに動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="89cd6-111">プロバイダー ProgID の登録</span><span class="sxs-lookup"><span data-stu-id="89cd6-111">Registering provider ProgID</span></span>

<span data-ttu-id="89cd6-112">各 .osc プロバイダーは、プログラム id (`ProgID`) を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="89cd6-113">プロバイダーインストーラーは、次のいずれかの場所を選択して、 `ProgID`を追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="89cd6-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="89cd6-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーのインストーラーは、プロバイダーが現在ログオンしているユーザーに対してのみインストールされている場合は、この場所を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="89cd6-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーインストーラーは、プロバイダーがコンピューター上のすべてのユーザーに対してインストールされている場合に、この場所を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="89cd6-116">クライアントコンピューターに32ビットの`ProgID` Outlook が64ビットの Windows オペレーティングシステムで実行されている場合を除き、.osc は上記の場所でプロバイダーを探します。</span><span class="sxs-lookup"><span data-stu-id="89cd6-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="89cd6-117">このような場合`HKEY_CURRENT_USER`は、プロバイダーのインストーラーで、または`HKEY_LOCAL_MACHINE`ハイブに次のいずれかの場所を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="89cd6-118">クイック実行バージョンの Office の場合、プロバイダーのインストーラーは、HKEY_CURRENT_USER または HKEY_LOCAL_MACHINE ハイブの次のいずれかの場所を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89cd6-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="89cd6-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="89cd6-119">See also</span></span>

- [<span data-ttu-id="89cd6-120">インストールチェックリスト</span><span class="sxs-lookup"><span data-stu-id="89cd6-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="89cd6-121">プロバイダーを開発するための簡単な手順</span><span class="sxs-lookup"><span data-stu-id="89cd6-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="89cd6-122">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="89cd6-122">Deploying a Provider</span></span>](deploying-a-provider.md)

