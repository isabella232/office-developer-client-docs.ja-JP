---
title: インストール チェックリスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーを正常にインストールするための前提条件について説明します。また、プロバイダーのインストーラーが正常に動作することを確認する必要があります。
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286342"
---
# <a name="installation-checklist"></a><span data-ttu-id="dbfdc-103">インストール チェックリスト</span><span class="sxs-lookup"><span data-stu-id="dbfdc-103">Installation checklist</span></span>

<span data-ttu-id="dbfdc-104">このトピックでは、Outlook Social Connector (.osc) プロバイダーを正常にインストールするための前提条件について説明します。また、プロバイダーのインストーラーが正常に動作することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-104">This topic describes prerequisites for successfully installing an Outlook Social Connector (OSC) provider, and the installation checks that your provider installer should complete to work correctly.</span></span>
  
## <a name="installation-overview"></a><span data-ttu-id="dbfdc-105">インストールの概要</span><span class="sxs-lookup"><span data-stu-id="dbfdc-105">Installation overview</span></span>

<span data-ttu-id="dbfdc-106">ユーザーは、Outlook のサポートバージョンが存在し、.osc がインストールされてクライアントコンピューターに有効になっている場合にのみ、.osc プロバイダーをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-106">Users should install OSC providers only if a supporting version of Outlook is present and the OSC is installed and enabled on the client computer.</span></span> <span data-ttu-id="dbfdc-107">outlook のバージョンをサポートしているのは、office outlook 2003、office outlook 2007、outlook 2010、outlook 2013 (クライアントコンピューターにインストールされているか、outlook 2010 および outlook の場合は、クライアントコンピューター上でクイック実行が配信される場合) です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-107">Supporting versions of Outlook are Office Outlook 2003, Office Outlook 2007, Outlook 2010 and Outlook 2013 (installed on the client computer or, in the case of Outlook 2010 and Outlook 2013, delivered by Click-to-Run on the client computer).</span></span> <span data-ttu-id="dbfdc-108">インストールが正常に行われるように、プロバイダーのインストーラーは次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-108">To ensure a successful installation, your provider installer should do the following:</span></span>
  
- <span data-ttu-id="dbfdc-109">サポートされているバージョンの Outlook があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-109">Verify whether a supported version of Outlook is present.</span></span>
    
- <span data-ttu-id="dbfdc-110">.osc がインストールされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-110">Verify whether the OSC is installed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="dbfdc-111">クイック実行は、outlook 2010 (32 ビット) または outlook 2013 (32 ビット) が実行できる仮想環境です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-111">Click-to-Run is a virtual environment in which Outlook 2010 (32-bit) or Outlook 2013 (32-bit) can run.</span></span> <span data-ttu-id="dbfdc-112">Outlook 2013 の場合は、Windows レジストリの HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook に virtualoutlook キーが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-112">For Outlook 2013, verify if the VirtualOutlook key exists in HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook of the Windows registry.</span></span> <span data-ttu-id="dbfdc-113">クイック実行製品として outlook をクライアントコンピューターに配信する方法の詳細については、「[クイック実行製品としてコンピューター上で outlook が利用可能かどうかを確認する方法](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-113">For more information about delivering Outlook as a Click-to-Run product on a client computer, see [How to Verify if Outlook is Available on a Computer as a Click-to-Run Product](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx).</span></span> 
  
<span data-ttu-id="dbfdc-114">ただし、ユーザーは、プロバイダーをインストールする前に、.osc が有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-114">The user, however, has to ensure that the OSC is enabled before installing the provider.</span></span>
  
<span data-ttu-id="dbfdc-115">.osc プロバイダーを含むサードパーティは、.osc を再配布できません。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-115">Third parties, including OSC providers, cannot redistribute the OSC.</span></span> <span data-ttu-id="dbfdc-116">ただし、.osc がインストールされていない場合、プロバイダーインストーラーは適切な g リンクを使用して、クライアントコンピューターに .osc をインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-116">However, if the OSC is not installed, the provider installer can use appropriate g-links to install the OSC on the client computer.</span></span> <span data-ttu-id="dbfdc-117">g リンクは、ユーザーを対応する web ページhttps://g.live.comに転送して、.osc をダウンロードするための特別に構築された URL です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-117">A g-link is a specially constructed URL on https://g.live.com that forwards a user to a corresponding webpage to download the OSC.</span></span> <span data-ttu-id="dbfdc-118">.osc g リンクは、 https://g.live.com/0CR _lcid_/ _glink_として書式設定されます。 _lcid_と_glink_では、クライアントコンピューター上の Outlook のロケール、バージョン、ビットが指定されます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-118">An OSC g-link is formatted as https://g.live.com/0CR _LCID_/ _Glink_, where  _LCID_ and  _Glink_ specify the locale, version, and bitness of Outlook on the client computer.</span></span> <span data-ttu-id="dbfdc-119">各 g リンクは、実行可能ファイルを指しており、指定された_LCID_および_glink_値に固有のものです。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-119">Each g-link points to an executable and is specific to the specified  _LCID_ and  _Glink_ values.</span></span> 
  
<span data-ttu-id="dbfdc-120">たとえば、LCID 1033 (米国英語) 用の outlook 2003 または outlook 2007 用の最新バージョンの .osc をインストールするための g リンクは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-120">For example, the g-link to install the latest version of the OSC for Outlook 2003 or Outlook 2007 for the LCID 1033 (US English) is as follows:</span></span>
  
https://g.live.com/0CR1033/80
  
<span data-ttu-id="dbfdc-121">Outlook のさまざまなバージョンとビットの_リンク_値、およびサポートされるロケールの_LCID_値の詳細については、次のセクション「[インストールチェックリスト](#olosc_InstallationOverview_InstallationChecklist)」の「#7」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-121">For details about  _Glink_ values for different versions and bitness of Outlook, and  _LCID_ values for supported locales, see #7 in the section [Installation Checklist](#olosc_InstallationOverview_InstallationChecklist) below.</span></span> 

<span data-ttu-id="dbfdc-122"><a name="olosc_InstallationOverview_InstallationChecklist"> </a></span><span class="sxs-lookup"><span data-stu-id="dbfdc-122"></span></span>

## <a name="installation-checklist"></a><span data-ttu-id="dbfdc-123">インストール チェックリスト</span><span class="sxs-lookup"><span data-stu-id="dbfdc-123">Installation checklist</span></span>

<span data-ttu-id="dbfdc-124">プロバイダーのセットアップパッケージは、図1に示すように、一連のインストールチェックを実行して、プロバイダーが正常にインストールされるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-124">The provider setup package should perform a series of installation checks, as shown in Figure 1, to ensure that the provider installs successfully.</span></span>
  
<span data-ttu-id="dbfdc-125">**図1。プロバイダーのインストールロジック**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-125">**Figure 1. Provider installation logic**</span></span>

![インストール チェックリスト](media/odc_ol14_ta_OSC_Fig07.gif)
  
<span data-ttu-id="dbfdc-127">次の手順では、図1に示されているインストールの確認について説明します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-127">The following procedure describes the installation checks outlined in Figure 1.</span></span>
  
1. <span data-ttu-id="dbfdc-128">前提条件として、outlook がインストールされているかどうかを検出し、インストールされているか存在している場合は、outlook のバージョンが .osc をサポートしているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-128">As a prerequisite, detect whether Outlook is installed or present, and if installed or present, determine whether the version of Outlook supports the OSC.</span></span> <span data-ttu-id="dbfdc-129">インストールされている outlook のバージョンを検出する方法については、「 [outlook のバージョンを確認](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-129">For more information about detecting the installed version of Outlook, see [Check the Version of Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).</span></span>
    
   - <span data-ttu-id="dbfdc-130">インストールされている outlook のバージョンが outlook 2003 より前の場合は、プロバイダーのインストール手順を完了できません。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-130">If the installed version of Outlook is earlier than Outlook 2003, the provider installation procedure cannot complete.</span></span> <span data-ttu-id="dbfdc-131">ユーザーに、サポートされているバージョンの Outlook と .osc を入手してから、.osc プロバイダーをインストールするように通知します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-131">Inform the user to obtain a supported version of Outlook and the OSC before proceeding to install the OSC provider.</span></span>
    
   - <span data-ttu-id="dbfdc-132">Outlook がインストールされていない場合は、手順2に進みます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-132">If Outlook is not installed, proceed to step 2.</span></span>
    
   - <span data-ttu-id="dbfdc-133">outlook 2003 または outlook 2007 がインストールされている場合は、手順3に進みます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-133">If Outlook 2003 or Outlook 2007 is installed, proceed to step 3.</span></span> 
    
   - <span data-ttu-id="dbfdc-134">outlook 2010 または outlook 2013 がインストールされている場合は、手順4に進みます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-134">If Outlook 2010 or Outlook 2013 is installed, proceed to step 4.</span></span>
    
2. <span data-ttu-id="dbfdc-135">**クライアントコンピューターに Outlook がインストールされていない場合は、次の手順を続行します。**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-135">**Proceed with this step if Outlook is not installed on the client computer:**</span></span>
    
   1. <span data-ttu-id="dbfdc-136">outlook 2010 または outlook 2013 のクイック実行インストールの既定のコンポーネントとして、.osc がインストールされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-136">Check whether the OSC is installed as a default component of a Click-to-Run installation of Outlook 2010 or Outlook 2013.</span></span> <span data-ttu-id="dbfdc-137">Windows レジストリ`VirtualOutlook`の次の場所にあるキーを調べます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-137">Examine the  `VirtualOutlook` key in the following location in the Windows registry:</span></span> 
      
      - <span data-ttu-id="dbfdc-138">Outlook 2010 の場合`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`</span><span class="sxs-lookup"><span data-stu-id="dbfdc-138">For Outlook 2010,  `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`</span></span>
      
      - <span data-ttu-id="dbfdc-139">Outlook Social Connector 2013 の場合`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`</span><span class="sxs-lookup"><span data-stu-id="dbfdc-139">For Outlook Social Connector 2013,  `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`</span></span>
      
      <span data-ttu-id="dbfdc-140">`VirtualOutlook`キーは、インストールされている製品の "en-us" などのロケールタグを含む REG_SZ 値です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-140">The  `VirtualOutlook` key is a REG_SZ value that contains the locale tag, such as "en-us", of the installed product.</span></span> 
      
   2. <span data-ttu-id="dbfdc-141">この`VirtualOutlook`キーが存在しない場合、Outlook はクライアントコンピューターに存在せず、プロバイダーのインストール手順を完了できません。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-141">If the  `VirtualOutlook` key does not exist, Outlook is not present on the client computer, and the provider installation procedure cannot complete.</span></span> <span data-ttu-id="dbfdc-142">ユーザーに、サポートされているバージョンの Outlook と .osc を入手してから、.osc プロバイダーをインストールするように通知します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-142">Inform the user to obtain a supported version of Outlook and the OSC before proceeding to install the OSC provider.</span></span> 
      
   3. <span data-ttu-id="dbfdc-143">このキー `VirtualOutlook`が存在する場合、Outlook はクイック実行でクライアントコンピューターに配信されていました。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-143">If the  `VirtualOutlook` key does exist, Outlook was delivered by Click-to-Run on the client computer.</span></span> <span data-ttu-id="dbfdc-144">Windows レジストリの次の場所にある`OSCVersion`キーを調べて、インストールされている .osc タイプライブラリのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-144">Proceed to check the installed version of the OSC type library by examining the  `OSCVersion` key in the following location in the Windows registry:</span></span> 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      <span data-ttu-id="dbfdc-145">の`OSCVersion`値は、形式ライブラリのバージョン番号を指定する文字列です (たとえば、"1.0"、"1.1"、または "15")。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-145">The value of  `OSCVersion` is a string that specifies the type library version number of Socialprovider.dll (for example, "1.0", "1.1", or "15").</span></span> 
      
   4. <span data-ttu-id="dbfdc-146">が`OSCVersion` "1.0"、"1.1"、または "15" の場合は、適切なバージョンの .osc がインストールされています。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-146">If  `OSCVersion` is "1.0", "1.1" or "15", an appropriate version of OSC is installed.</span></span> <span data-ttu-id="dbfdc-147">手順6に進み、最新バージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-147">Proceed to step 6 to find the current Outlook user interface locale to prepare for installing the latest version of the OSC.</span></span> 
      
   5. <span data-ttu-id="dbfdc-148">それ以外`OSCVersion`の場合は、予期される値を含みません。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-148">Otherwise,  `OSCVersion` does not contain an expected value.</span></span> <span data-ttu-id="dbfdc-149">手順6に進み、適切なバージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-149">Proceed to step 6 to find the current Outlook user interface locale to prepare for installing an appropriate version of the OSC.</span></span> 
    
3. <span data-ttu-id="dbfdc-150">**outlook 2003 または outlook 2007 がクライアントコンピューターにインストールされている場合は、次の手順を続行します。**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-150">**Proceed with this step if Outlook 2003 or Outlook 2007 is installed on the client computer:**</span></span>
    
   1. <span data-ttu-id="dbfdc-151">次の修飾されたコンポーネント ID が存在するかどうかをテストするインストーラーカスタムアクションを記述して、.osc がインストールされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-151">Verify whether the OSC is installed by writing an installer custom action to test for the existence of the following qualified component ID:</span></span>
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      <span data-ttu-id="dbfdc-152">修飾コンポーネント ID は、ポインターに似た単一レベルの間接的なメソッドを提供する GUID です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-152">The qualified component ID is a GUID that provides a method of single-level indirection, similar to a pointer.</span></span> <span data-ttu-id="dbfdc-153">windows インストーラーの詳細については、「 [windows インストーラーのドキュメントのロードマップ](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-153">For more information about Windows Installer, see [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).</span></span>
      
   2. <span data-ttu-id="dbfdc-154">指定した修飾コンポーネントが存在する場合は、.osc のバージョンがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-154">If the specified qualified component exists, a version of the OSC is installed.</span></span> <span data-ttu-id="dbfdc-155">手順5に進み、最新バージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-155">Proceed to step 5 to find the current Outlook user interface locale to prepare for installing the latest version of the OSC.</span></span>
      
   3. <span data-ttu-id="dbfdc-156">それ以外の場合は、.osc がインストールされません。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-156">Otherwise, the OSC is not installed.</span></span> <span data-ttu-id="dbfdc-157">手順6に進み、適切なバージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-157">Proceed to step 6 to find the current Outlook user interface locale to prepare for installing an appropriate version of the OSC.</span></span>
      
4. <span data-ttu-id="dbfdc-158">**outlook 2010 または outlook 2013 がクライアントコンピューターにインストールされている場合は、次の手順を続行します。**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-158">**Proceed with this step if Outlook 2010 or Outlook 2013 is installed on the client computer:**</span></span>
    
   1. <span data-ttu-id="dbfdc-159">Windows レジストリの以下の場所にある`Bitness`キーを調べて、インストールされている Outlook のバージョンのビット数を確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-159">Determine the bitness of the installed version of Outlook by examining the  `Bitness` key in the following location in the Windows registry:</span></span> 
      
      - <span data-ttu-id="dbfdc-160">Outlook 2010 の場合は、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`</span><span class="sxs-lookup"><span data-stu-id="dbfdc-160">For Outlook 2010, look at  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`</span></span>
      
      - <span data-ttu-id="dbfdc-161">Outlook 2013 の場合は、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`</span><span class="sxs-lookup"><span data-stu-id="dbfdc-161">For Outlook 2013, look at  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`</span></span>
      
      <span data-ttu-id="dbfdc-162">キー `Bitness`は、32ビット outlook の場合は "x86"、64ビットの outlook の場合は "x64" です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-162">The  `Bitness` key is "x86" for 32-bit Outlook, or "x64" for 64-bit Outlook.</span></span> 
      
   2. <span data-ttu-id="dbfdc-163">プロバイダーがマネージドプロバイダーで、ターゲットプラットフォームを指定したプロバイダコンポーネントを**任意の CPU**としてコンパイルした場合は、手順6に進み、最新バージョンの .osc のインストールを準備するための現在の Outlook ユーザーインターフェイスロケールを見つけます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-163">If your provider is a managed provider, and you compiled the provider component specifying the target platform as **Any CPU**, proceed with step 6 to find the current Outlook user interface locale to prepare for installing the latest version of the OSC.</span></span> <span data-ttu-id="dbfdc-164">プロバイダーは、この .osc の32ビットバージョンと64ビットバージョンの両方で機能します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-164">Your provider will work on both 32-bit and 64-bit versions of the OSC.</span></span>
      
   3. <span data-ttu-id="dbfdc-165">プロバイダーがネイティブ COM コンポーネントの場合は、インストールされている Outlook のバージョンのビット数を確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-165">If your provider is a native COM component, examine the bitness of the installed version of Outlook:</span></span>
      
      - <span data-ttu-id="dbfdc-166">インストールされている Outlook のバージョンが32ビットである場合は、適切な .osc がインストールされていることを確認した後に、インストール手順で32ビットのプロバイダー (手順 8) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-166">If the installed version of Outlook is 32-bit, your installation procedure will have to install a 32-bit provider (in step 8), after ensuring that an appropriate OSC is installed.</span></span>
      
      - <span data-ttu-id="dbfdc-167">インストールされている Outlook のバージョンが64ビットである場合は、適切な .osc がインストールされていることを確認した後、インストール手順で64ビットのプロバイダー (手順 8) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-167">Otherwise, the installed version of Outlook is 64-bit, and your installation procedure will have to install a 64-bit provider (in step 8), after ensuring that an appropriate OSC is installed.</span></span> 
      
   4. <span data-ttu-id="dbfdc-168">手順6に進み、適切なバージョンの .osc をインストールするための準備として、現在の Outlook ユーザーインターフェイスのロケールを検索します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-168">Proceed with step 6 to find the current Outlook user interface locale to prepare for installing an appropriate version of the OSC.</span></span>
    
5. <span data-ttu-id="dbfdc-169">**outlook 2003 または outlook 2007 がインストールされており、クライアントコンピューターに .osc がインストールされている場合は、この手順を続行します。** Windows レジストリの次の場所にある`OSCLcid`キーを調べて、現在の Outlook ユーザーインターフェイスのロケールを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-169">**Proceed with this step if Outlook 2003 or Outlook 2007 is installed, and the OSC is installed on the client computer:** Check the current Outlook user interface locale by examining the  `OSCLcid` key in the following location in the Windows registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   <span data-ttu-id="dbfdc-170">`OSCLcid`キーは、現在の Outlook ユーザーインターフェイスのロケールを表す、インターネット技術標準化委員会 (IETF) のロケールタグ ( [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)および[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)で定義) を指定する DWORD 値です。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-170">The  `OSCLcid` key is a DWORD value that specifies the Internet Engineering Task Force (IETF) locale tag (defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), that represents the current Outlook user interface locale.</span></span> <span data-ttu-id="dbfdc-171">手順7に進み、クライアントコンピューターに最新の .osc をインストールします。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-171">Proceed with step 7 to install the latest OSC on the client computer.</span></span>
    
6. <span data-ttu-id="dbfdc-172">**outlook 2003 または outlook 2007 がインストールされているか、outlook 2010 または outlook 2013 がインストールされている場合に、この手順を続行します。ただし、最新の .osc が必ずしもクライアントコンピューターにインストールされるとは限りません。**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-172">**Proceed with this step if Outlook 2003 or Outlook 2007 is installed, or Outlook 2010 or Outlook 2013 is present, but the latest OSC is not necessarily installed on the client computer:**</span></span>
    
   <span data-ttu-id="dbfdc-173">**言語設定**オブジェクトを使用して、Outlook ユーザーインターフェイスのロケールの LCID を特定します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-173">Use the **LanguageSettings** object to determine the LCID of the Outlook user interface locale.</span></span> <span data-ttu-id="dbfdc-174">次の Visual Basic Scripting Edition (VBScript) コードスニペットは、Outlook ユーザーインターフェイスロケールの LCID を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-174">The following Visual Basic Scripting Edition (VBScript) code snippet demonstrates how to obtain the LCID of the Outlook user interface locale.</span></span> 
    
   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. <span data-ttu-id="dbfdc-175">**インストーラーにインストールされているバージョンの Outlook の LCID がある場合は、次の手順に進みます。最新の .osc は、必ずしもクライアントコンピューターにインストールされません。**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-175">**Proceed with this step if the installer has the LCID of the installed version of Outlook, but the latest OSC is not necessarily installed on the client computer:**</span></span>
    
   <span data-ttu-id="dbfdc-176">インストールパッケージに g リンクをチェーンして、最新バージョンの .osc がクライアントコンピューターにインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-176">Chain a g-link into your installation package to ensure that the latest version of the OSC is installed on the client computer.</span></span> <span data-ttu-id="dbfdc-177">g リンクの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-177">The g-link format is as follows:</span></span>
    
   <span data-ttu-id="dbfdc-178">https://g.live.com/0CR_LCID_/  _glink_</span><span class="sxs-lookup"><span data-stu-id="dbfdc-178">https://g.live.com/0CR _LCID_/ _Glink_</span></span>
    
   <span data-ttu-id="dbfdc-179">サポートされている_LCID_値については、表1を参照してください。サポートされている_glink_値については、表2を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-179">Refer to Table 1 below for the supported  _LCID_ values, and Table 2 for the supported  _Glink_ values.</span></span> <span data-ttu-id="dbfdc-180">たとえば、次のように、32ビットの Outlook Social Connector 2013 (米国英語) 用に32ビットの .osc の最新バージョンをインストールするための g リンクがあります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-180">For example, the g-link to install the latest version of the 32-bit OSC for 32-bit Outlook Social Connector 2013 (US English) is as follows:</span></span> 
    
   https://g.live.com/0CR1033/82
    
8. <span data-ttu-id="dbfdc-181">プロバイダーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-181">Install the provider.</span></span> <span data-ttu-id="dbfdc-182">プロバイダーのインストール手順では、プログラム id (ProgID) を適切な Windows レジストリの場所に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-182">The provider installation procedure must register the programmatic identifier (ProgID) in the appropriate Windows registry location.</span></span> <span data-ttu-id="dbfdc-183">詳細については、「[プロバイダーの登録](registering-a-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-183">For more information, see [Registering a Provider](registering-a-provider.md).</span></span> <span data-ttu-id="dbfdc-184">また、インストールするプロバイダーのビット数が、クライアントコンピューター上に存在する Outlook のバージョンのビットと同じであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-184">Also, be sure that the bitness of the provider to be installed is the same as the bitness of the version of Outlook present on the client computer.</span></span> <span data-ttu-id="dbfdc-185">たとえば、32ビットの outlook 2013 が存在する場合は、32ビットのプロバイダーをインストールし、64ビットの outlook をインストールしている場合は、64ビットのプロバイダーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-185">For example, install a 32-bit provider if 32-bit Outlook 2013 is present, and a 64-bit provider if 64-bit Outlook 2013 is installed.</span></span> <span data-ttu-id="dbfdc-186">Outlook 2003 または2007の場合は、使用しているプロバイダーの32ビットバージョンのみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-186">For Outlook 2003 or 2007, only the 32-bit version of your provider applies.</span></span> 
    
<span data-ttu-id="dbfdc-187">**表 1: サポートされているロケールおよび対応する LCID 値を、.osc の16進数で指定します。**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-187">**Table 1: Supported locale and corresponding LCID values in hexadecimal for the OSC**</span></span>
  
|<span data-ttu-id="dbfdc-188">**Locale**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-188">**Locale**</span></span>|<span data-ttu-id="dbfdc-189">**LCID**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-189">**LCID**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbfdc-190">ar-sa</span><span class="sxs-lookup"><span data-stu-id="dbfdc-190">ar-sa</span></span>  <br/> |<span data-ttu-id="dbfdc-191">1025</span><span class="sxs-lookup"><span data-stu-id="dbfdc-191">1025</span></span>  <br/> |
|<span data-ttu-id="dbfdc-192">bg-bg</span><span class="sxs-lookup"><span data-stu-id="dbfdc-192">bg-bg</span></span>  <br/> |<span data-ttu-id="dbfdc-193">1026</span><span class="sxs-lookup"><span data-stu-id="dbfdc-193">1026</span></span>  <br/> |
|<span data-ttu-id="dbfdc-194">ca-es</span><span class="sxs-lookup"><span data-stu-id="dbfdc-194">ca-es</span></span>  <br/> |<span data-ttu-id="dbfdc-195">1027</span><span class="sxs-lookup"><span data-stu-id="dbfdc-195">1027</span></span>  <br/> |
|<span data-ttu-id="dbfdc-196">cs-cz</span><span class="sxs-lookup"><span data-stu-id="dbfdc-196">cs-cz</span></span>  <br/> |<span data-ttu-id="dbfdc-197">1029</span><span class="sxs-lookup"><span data-stu-id="dbfdc-197">1029</span></span>  <br/> |
|<span data-ttu-id="dbfdc-198">da-dk</span><span class="sxs-lookup"><span data-stu-id="dbfdc-198">da-dk</span></span>  <br/> |<span data-ttu-id="dbfdc-199">1030</span><span class="sxs-lookup"><span data-stu-id="dbfdc-199">1030</span></span>  <br/> |
|<span data-ttu-id="dbfdc-200">de-de</span><span class="sxs-lookup"><span data-stu-id="dbfdc-200">de-de</span></span>  <br/> |<span data-ttu-id="dbfdc-201">1031</span><span class="sxs-lookup"><span data-stu-id="dbfdc-201">1031</span></span>  <br/> |
|<span data-ttu-id="dbfdc-202">el-gr</span><span class="sxs-lookup"><span data-stu-id="dbfdc-202">el-gr</span></span>  <br/> |<span data-ttu-id="dbfdc-203">1032</span><span class="sxs-lookup"><span data-stu-id="dbfdc-203">1032</span></span>  <br/> |
|<span data-ttu-id="dbfdc-204">ja-jp</span><span class="sxs-lookup"><span data-stu-id="dbfdc-204">en-us</span></span>  <br/> |<span data-ttu-id="dbfdc-205">1033</span><span class="sxs-lookup"><span data-stu-id="dbfdc-205">1033</span></span>  <br/> |
|<span data-ttu-id="dbfdc-206">es-es</span><span class="sxs-lookup"><span data-stu-id="dbfdc-206">es-es</span></span>  <br/> |<span data-ttu-id="dbfdc-207">3082</span><span class="sxs-lookup"><span data-stu-id="dbfdc-207">3082</span></span>  <br/> |
|<span data-ttu-id="dbfdc-208">et-ee</span><span class="sxs-lookup"><span data-stu-id="dbfdc-208">et-ee</span></span>  <br/> |<span data-ttu-id="dbfdc-209">1061</span><span class="sxs-lookup"><span data-stu-id="dbfdc-209">1061</span></span>  <br/> |
|<span data-ttu-id="dbfdc-210">eu-es</span><span class="sxs-lookup"><span data-stu-id="dbfdc-210">eu-es</span></span>  <br/> |<span data-ttu-id="dbfdc-211">1069</span><span class="sxs-lookup"><span data-stu-id="dbfdc-211">1069</span></span>  <br/> |
|<span data-ttu-id="dbfdc-212">fi-fi</span><span class="sxs-lookup"><span data-stu-id="dbfdc-212">fi-fi</span></span>  <br/> |<span data-ttu-id="dbfdc-213">1035</span><span class="sxs-lookup"><span data-stu-id="dbfdc-213">1035</span></span>  <br/> |
|<span data-ttu-id="dbfdc-214">fr-fr</span><span class="sxs-lookup"><span data-stu-id="dbfdc-214">fr-fr</span></span>  <br/> |<span data-ttu-id="dbfdc-215">1036</span><span class="sxs-lookup"><span data-stu-id="dbfdc-215">1036</span></span>  <br/> |
|<span data-ttu-id="dbfdc-216">gl-es</span><span class="sxs-lookup"><span data-stu-id="dbfdc-216">gl-es</span></span>  <br/> |<span data-ttu-id="dbfdc-217">1110</span><span class="sxs-lookup"><span data-stu-id="dbfdc-217">1110</span></span>  <br/> |
|<span data-ttu-id="dbfdc-218">he-il</span><span class="sxs-lookup"><span data-stu-id="dbfdc-218">he-il</span></span>  <br/> |<span data-ttu-id="dbfdc-219">1037</span><span class="sxs-lookup"><span data-stu-id="dbfdc-219">1037</span></span>  <br/> |
|<span data-ttu-id="dbfdc-220">hi-in</span><span class="sxs-lookup"><span data-stu-id="dbfdc-220">hi-in</span></span>  <br/> |<span data-ttu-id="dbfdc-221">1081</span><span class="sxs-lookup"><span data-stu-id="dbfdc-221">1081</span></span>  <br/> |
|<span data-ttu-id="dbfdc-222">hr-hr</span><span class="sxs-lookup"><span data-stu-id="dbfdc-222">hr-hr</span></span>  <br/> |<span data-ttu-id="dbfdc-223">1050</span><span class="sxs-lookup"><span data-stu-id="dbfdc-223">1050</span></span>  <br/> |
|<span data-ttu-id="dbfdc-224">hu-hu</span><span class="sxs-lookup"><span data-stu-id="dbfdc-224">hu-hu</span></span>  <br/> |<span data-ttu-id="dbfdc-225">1038</span><span class="sxs-lookup"><span data-stu-id="dbfdc-225">1038</span></span>  <br/> |
|<span data-ttu-id="dbfdc-226">it-it</span><span class="sxs-lookup"><span data-stu-id="dbfdc-226">it-it</span></span>  <br/> |<span data-ttu-id="dbfdc-227">1040</span><span class="sxs-lookup"><span data-stu-id="dbfdc-227">1040</span></span>  <br/> |
|<span data-ttu-id="dbfdc-228">ja-jp</span><span class="sxs-lookup"><span data-stu-id="dbfdc-228">ja-jp</span></span>  <br/> |<span data-ttu-id="dbfdc-229">1041</span><span class="sxs-lookup"><span data-stu-id="dbfdc-229">1041</span></span>  <br/> |
|<span data-ttu-id="dbfdc-230">kk-kz</span><span class="sxs-lookup"><span data-stu-id="dbfdc-230">kk-kz</span></span>  <br/> |<span data-ttu-id="dbfdc-231">1087</span><span class="sxs-lookup"><span data-stu-id="dbfdc-231">1087</span></span>  <br/> |
|<span data-ttu-id="dbfdc-232">ko-kr</span><span class="sxs-lookup"><span data-stu-id="dbfdc-232">ko-kr</span></span>  <br/> |<span data-ttu-id="dbfdc-233">1042</span><span class="sxs-lookup"><span data-stu-id="dbfdc-233">1042</span></span>  <br/> |
|<span data-ttu-id="dbfdc-234">lt-lt</span><span class="sxs-lookup"><span data-stu-id="dbfdc-234">lt-lt</span></span>  <br/> |<span data-ttu-id="dbfdc-235">1063</span><span class="sxs-lookup"><span data-stu-id="dbfdc-235">1063</span></span>  <br/> |
|<span data-ttu-id="dbfdc-236">lv-lv</span><span class="sxs-lookup"><span data-stu-id="dbfdc-236">lv-lv</span></span>  <br/> |<span data-ttu-id="dbfdc-237">1062</span><span class="sxs-lookup"><span data-stu-id="dbfdc-237">1062</span></span>  <br/> |
|<span data-ttu-id="dbfdc-238">nb-no</span><span class="sxs-lookup"><span data-stu-id="dbfdc-238">nb-no</span></span>  <br/> |<span data-ttu-id="dbfdc-239">1044</span><span class="sxs-lookup"><span data-stu-id="dbfdc-239">1044</span></span>  <br/> |
|<span data-ttu-id="dbfdc-240">nl-nl</span><span class="sxs-lookup"><span data-stu-id="dbfdc-240">nl-nl</span></span>  <br/> |<span data-ttu-id="dbfdc-241">1043</span><span class="sxs-lookup"><span data-stu-id="dbfdc-241">1043</span></span>  <br/> |
|<span data-ttu-id="dbfdc-242">pl-pl</span><span class="sxs-lookup"><span data-stu-id="dbfdc-242">pl-pl</span></span>  <br/> |<span data-ttu-id="dbfdc-243">1045</span><span class="sxs-lookup"><span data-stu-id="dbfdc-243">1045</span></span>  <br/> |
|<span data-ttu-id="dbfdc-244">pt-br</span><span class="sxs-lookup"><span data-stu-id="dbfdc-244">pt-br</span></span>  <br/> |<span data-ttu-id="dbfdc-245">1046</span><span class="sxs-lookup"><span data-stu-id="dbfdc-245">1046</span></span>  <br/> |
|<span data-ttu-id="dbfdc-246">pt-pt</span><span class="sxs-lookup"><span data-stu-id="dbfdc-246">pt-pt</span></span>  <br/> |<span data-ttu-id="dbfdc-247">2070</span><span class="sxs-lookup"><span data-stu-id="dbfdc-247">2070</span></span>  <br/> |
|<span data-ttu-id="dbfdc-248">ro-ro</span><span class="sxs-lookup"><span data-stu-id="dbfdc-248">ro-ro</span></span>  <br/> |<span data-ttu-id="dbfdc-249">1048</span><span class="sxs-lookup"><span data-stu-id="dbfdc-249">1048</span></span>  <br/> |
|<span data-ttu-id="dbfdc-250">ru-ru</span><span class="sxs-lookup"><span data-stu-id="dbfdc-250">ru-ru</span></span>  <br/> |<span data-ttu-id="dbfdc-251">1049</span><span class="sxs-lookup"><span data-stu-id="dbfdc-251">1049</span></span>  <br/> |
|<span data-ttu-id="dbfdc-252">sk-sk</span><span class="sxs-lookup"><span data-stu-id="dbfdc-252">sk-sk</span></span>  <br/> |<span data-ttu-id="dbfdc-253">1051</span><span class="sxs-lookup"><span data-stu-id="dbfdc-253">1051</span></span>  <br/> |
|<span data-ttu-id="dbfdc-254">sl-si</span><span class="sxs-lookup"><span data-stu-id="dbfdc-254">sl-si</span></span>  <br/> |<span data-ttu-id="dbfdc-255">1060</span><span class="sxs-lookup"><span data-stu-id="dbfdc-255">1060</span></span>  <br/> |
|<span data-ttu-id="dbfdc-256">cyrl-cs</span><span class="sxs-lookup"><span data-stu-id="dbfdc-256">sr-cyrl-cs</span></span>  <br/> |<span data-ttu-id="dbfdc-257">3098</span><span class="sxs-lookup"><span data-stu-id="dbfdc-257">3098</span></span>  <br/> |
|<span data-ttu-id="dbfdc-258">latn-cs</span><span class="sxs-lookup"><span data-stu-id="dbfdc-258">sr-latn-cs</span></span>  <br/> |<span data-ttu-id="dbfdc-259">2074</span><span class="sxs-lookup"><span data-stu-id="dbfdc-259">2074</span></span>  <br/> |
|<span data-ttu-id="dbfdc-260">sv-se</span><span class="sxs-lookup"><span data-stu-id="dbfdc-260">sv-se</span></span>  <br/> |<span data-ttu-id="dbfdc-261">1053</span><span class="sxs-lookup"><span data-stu-id="dbfdc-261">1053</span></span>  <br/> |
|<span data-ttu-id="dbfdc-262">th-th</span><span class="sxs-lookup"><span data-stu-id="dbfdc-262">th-th</span></span>  <br/> |<span data-ttu-id="dbfdc-263">1054</span><span class="sxs-lookup"><span data-stu-id="dbfdc-263">1054</span></span>  <br/> |
|<span data-ttu-id="dbfdc-264">tr-tr</span><span class="sxs-lookup"><span data-stu-id="dbfdc-264">tr-tr</span></span>  <br/> |<span data-ttu-id="dbfdc-265">1055</span><span class="sxs-lookup"><span data-stu-id="dbfdc-265">1055</span></span>  <br/> |
|<span data-ttu-id="dbfdc-266">uk-ua</span><span class="sxs-lookup"><span data-stu-id="dbfdc-266">uk-ua</span></span>  <br/> |<span data-ttu-id="dbfdc-267">1058</span><span class="sxs-lookup"><span data-stu-id="dbfdc-267">1058</span></span>  <br/> |
|<span data-ttu-id="dbfdc-268">zh-cn</span><span class="sxs-lookup"><span data-stu-id="dbfdc-268">zh-cn</span></span>  <br/> |<span data-ttu-id="dbfdc-269">2052</span><span class="sxs-lookup"><span data-stu-id="dbfdc-269">2052</span></span>  <br/> |
|<span data-ttu-id="dbfdc-270">zh-tw</span><span class="sxs-lookup"><span data-stu-id="dbfdc-270">zh-tw</span></span>  <br/> |<span data-ttu-id="dbfdc-271">1028</span><span class="sxs-lookup"><span data-stu-id="dbfdc-271">1028</span></span>  <br/> |
   
<span data-ttu-id="dbfdc-272">**表 2: .osc のサポートされている glink 値**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-272">**Table 2: Supported Glink values for the OSC**</span></span>
  
|<span data-ttu-id="dbfdc-273">**glink 値**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-273">**Glink value**</span></span>|<span data-ttu-id="dbfdc-274">**Function**</span><span class="sxs-lookup"><span data-stu-id="dbfdc-274">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbfdc-275">80</span><span class="sxs-lookup"><span data-stu-id="dbfdc-275">80</span></span>  <br/> |<span data-ttu-id="dbfdc-276">outlook 2003 または outlook 2007 用の最新バージョンの .osc をインストールします。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-276">Installs the latest version of OSC for Outlook 2003 or Outlook 2007.</span></span>  <br/> |
|<span data-ttu-id="dbfdc-277">82</span><span class="sxs-lookup"><span data-stu-id="dbfdc-277">82</span></span>  <br/> |<span data-ttu-id="dbfdc-278">outlook 2007、outlook 2010、または outlook Social Connector 2013 用に32ビットの詳細な更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-278">Installs the latest patch of 32-bit OSC for Outlook 2007, Outlook 2010, or Outlook Social Connector 2013.</span></span>  <br/> |
|<span data-ttu-id="dbfdc-279">83</span><span class="sxs-lookup"><span data-stu-id="dbfdc-279">83</span></span>  <br/> |<span data-ttu-id="dbfdc-280">outlook 2010 または outlook Social Connector 2013 用に64ビットの詳細な更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dbfdc-280">Installs the latest patch of 64-bit OSC for Outlook 2010 or Outlook Social Connector 2013.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbfdc-281">関連項目</span><span class="sxs-lookup"><span data-stu-id="dbfdc-281">See also</span></span>

- [<span data-ttu-id="dbfdc-282">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="dbfdc-282">Registering a Provider</span></span>](registering-a-provider.md) 
- [<span data-ttu-id="dbfdc-283">プロバイダーを開発するための簡単な手順</span><span class="sxs-lookup"><span data-stu-id="dbfdc-283">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="dbfdc-284">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="dbfdc-284">Deploying a Provider</span></span>](deploying-a-provider.md)

