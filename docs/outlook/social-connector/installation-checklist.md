---
title: インストール チェックリスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: このトピックでは、Outlook Social Connector (OSC) プロバイダーを正常にインストールするための前提条件と、プロバイダー インストーラーが正常に動作するために完了する必要があるインストール チェックについて説明します。
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286342"
---
# <a name="installation-checklist"></a><span data-ttu-id="d5c2b-103">インストール チェックリスト</span><span class="sxs-lookup"><span data-stu-id="d5c2b-103">Installation checklist</span></span>

<span data-ttu-id="d5c2b-104">このトピックでは、Outlook Social Connector (OSC) プロバイダーを正常にインストールするための前提条件と、プロバイダー インストーラーが正常に動作するために完了する必要があるインストール チェックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-104">This topic describes prerequisites for successfully installing an Outlook Social Connector (OSC) provider, and the installation checks that your provider installer should complete to work correctly.</span></span>
  
## <a name="installation-overview"></a><span data-ttu-id="d5c2b-105">インストールの概要</span><span class="sxs-lookup"><span data-stu-id="d5c2b-105">Installation overview</span></span>

<span data-ttu-id="d5c2b-106">ユーザーは、サポート されているバージョンの OSC プロバイダーが存在し、Outlook コンピューターに OSC がインストールされ、有効になっている場合にのみ、OSC プロバイダーをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-106">Users should install OSC providers only if a supporting version of Outlook is present and the OSC is installed and enabled on the client computer.</span></span> <span data-ttu-id="d5c2b-107">Outlook のサポート バージョンは、Office Outlook 2003、Office Outlook 2007、Outlook 2010、Outlook 2013 です (クライアント コンピューターにインストールされている場合、または Outlook 2010 および Outlook 2013 の場合は、クライアント コンピューターで クイック実行 によって配信されます)。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-107">Supporting versions of Outlook are Office Outlook 2003, Office Outlook 2007, Outlook 2010 and Outlook 2013 (installed on the client computer or, in the case of Outlook 2010 and Outlook 2013, delivered by Click-to-Run on the client computer).</span></span> <span data-ttu-id="d5c2b-108">インストールが正常に完了するには、プロバイダー インストーラーで次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-108">To ensure a successful installation, your provider installer should do the following:</span></span>
  
- <span data-ttu-id="d5c2b-109">サポートされているバージョンのファイルが存在Outlook確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-109">Verify whether a supported version of Outlook is present.</span></span>
    
- <span data-ttu-id="d5c2b-110">OSC がインストールされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-110">Verify whether the OSC is installed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d5c2b-111">クイック実行は、Outlook 2010 (32 ビット) または Outlook 2013 (32 ビット) を実行できる仮想環境です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-111">Click-to-Run is a virtual environment in which Outlook 2010 (32-bit) or Outlook 2013 (32-bit) can run.</span></span> <span data-ttu-id="d5c2b-112">2013 Outlook、VirtualOutlook キーがレジストリのHKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook存在Windowsします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-112">For Outlook 2013, verify if the VirtualOutlook key exists in HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook of the Windows registry.</span></span> <span data-ttu-id="d5c2b-113">クライアント コンピューターで クイック実行 製品として Outlook を配信する方法の詳細については[、「how to Verify if Outlook](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)is Available on a computer as a クイック実行 Product」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-113">For more information about delivering Outlook as a Click-to-Run product on a client computer, see [How to Verify if Outlook is Available on a Computer as a Click-to-Run Product](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx).</span></span> 
  
<span data-ttu-id="d5c2b-114">ただし、ユーザーは、プロバイダーをインストールする前に OSC が有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-114">The user, however, has to ensure that the OSC is enabled before installing the provider.</span></span>
  
<span data-ttu-id="d5c2b-115">OSC プロバイダーを含むサード パーティは、OSC を再配布できません。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-115">Third parties, including OSC providers, cannot redistribute the OSC.</span></span> <span data-ttu-id="d5c2b-116">ただし、OSC がインストールされていない場合、プロバイダー インストーラーは適切な g-links を使用して OSC をクライアント コンピューターにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-116">However, if the OSC is not installed, the provider installer can use appropriate g-links to install the OSC on the client computer.</span></span> <span data-ttu-id="d5c2b-117">g-link は、ユーザーを対応する Web ページに転送して OSC をダウンロードする特別に構築された https://g.live.com URL です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-117">A g-link is a specially constructed URL on https://g.live.com that forwards a user to a corresponding webpage to download the OSC.</span></span> <span data-ttu-id="d5c2b-118">OSC g-link は https://g.live.com/0CR _LCID_ /  _Glink_ として書式設定され _、LCID_ と _Glink_ はクライアント コンピューター上の Outlookのロケール、バージョン、およびビット数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-118">An OSC g-link is formatted as https://g.live.com/0CR _LCID_/ _Glink_, where  _LCID_ and  _Glink_ specify the locale, version, and bitness of Outlook on the client computer.</span></span> <span data-ttu-id="d5c2b-119">各 g-link は実行可能ファイルをポイントし、指定された  _LCID_ 値と  _Glink 値に固有_ です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-119">Each g-link points to an executable and is specific to the specified  _LCID_ and  _Glink_ values.</span></span> 
  
<span data-ttu-id="d5c2b-120">たとえば、LCID 1033 (米国英語) の Outlook 2003 または Outlook 2007 の OSC の最新バージョンをインストールする g リンクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-120">For example, the g-link to install the latest version of the OSC for Outlook 2003 or Outlook 2007 for the LCID 1033 (US English) is as follows:</span></span>
  
https://g.live.com/0CR1033/80
  
<span data-ttu-id="d5c2b-121">Outlook の異なるバージョンとビット数の Glink 値、およびサポートされている地域の _LCID_ 値の詳細については、以下の「インストール チェックリスト」の「#7」を [参照](#olosc_InstallationOverview_InstallationChecklist)してください。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-121">For details about  _Glink_ values for different versions and bitness of Outlook, and  _LCID_ values for supported locales, see #7 in the section [Installation Checklist](#olosc_InstallationOverview_InstallationChecklist) below.</span></span> 

<span data-ttu-id="d5c2b-122"><a name="olosc_InstallationOverview_InstallationChecklist"> </a></span><span class="sxs-lookup"><span data-stu-id="d5c2b-122"><a name="olosc_InstallationOverview_InstallationChecklist"> </a></span></span>

## <a name="installation-checklist"></a><span data-ttu-id="d5c2b-123">インストール チェックリスト</span><span class="sxs-lookup"><span data-stu-id="d5c2b-123">Installation checklist</span></span>

<span data-ttu-id="d5c2b-124">プロバイダーセットアップ パッケージは、プロバイダーが正常にインストールされたことを確認するために、図 1 に示すように、一連のインストール チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-124">The provider setup package should perform a series of installation checks, as shown in Figure 1, to ensure that the provider installs successfully.</span></span>
  
<span data-ttu-id="d5c2b-125">**図 1.プロバイダーのインストール ロジック**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-125">**Figure 1. Provider installation logic**</span></span>

![インストール チェックリスト](media/odc_ol14_ta_OSC_Fig07.gif)
  
<span data-ttu-id="d5c2b-127">次の手順では、図 1 に示すインストール チェックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-127">The following procedure describes the installation checks outlined in Figure 1.</span></span>
  
1. <span data-ttu-id="d5c2b-128">前提条件として、インストールまたはOutlookを検出し、インストールされている場合または存在する場合は、OSC のバージョンがサポートOutlook判断します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-128">As a prerequisite, detect whether Outlook is installed or present, and if installed or present, determine whether the version of Outlook supports the OSC.</span></span> <span data-ttu-id="d5c2b-129">インストールされているバージョンの検出方法の詳細については、「Outlookバージョンを確認する」を[参照](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx)Outlook。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-129">For more information about detecting the installed version of Outlook, see [Check the Version of Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).</span></span>
    
   - <span data-ttu-id="d5c2b-130">インストール済みバージョンのOutlook 2003 より前Outlookプロバイダーのインストール手順を完了できません。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-130">If the installed version of Outlook is earlier than Outlook 2003, the provider installation procedure cannot complete.</span></span> <span data-ttu-id="d5c2b-131">OSC プロバイダーのインストールに進む前に、サポートされているバージョンOutlook OSC を入手してください。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-131">Inform the user to obtain a supported version of Outlook and the OSC before proceeding to install the OSC provider.</span></span>
    
   - <span data-ttu-id="d5c2b-132">インストールOutlook場合は、手順 2 に進みます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-132">If Outlook is not installed, proceed to step 2.</span></span>
    
   - <span data-ttu-id="d5c2b-133">2003 Outlook 2007 Outlookインストールされている場合は、手順 3 に進みます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-133">If Outlook 2003 or Outlook 2007 is installed, proceed to step 3.</span></span> 
    
   - <span data-ttu-id="d5c2b-134">2010 Outlookまたは 2013 Outlookインストールされている場合は、手順 4 に進みます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-134">If Outlook 2010 or Outlook 2013 is installed, proceed to step 4.</span></span>
    
2. <span data-ttu-id="d5c2b-135">**クライアント コンピューターにインストールされていない場合Outlook手順を実行します。**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-135">**Proceed with this step if Outlook is not installed on the client computer:**</span></span>
    
   1. <span data-ttu-id="d5c2b-136">OSC が 2010 または 2013 の クイック実行 インストールの既定のOutlookインストールOutlookします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-136">Check whether the OSC is installed as a default component of a Click-to-Run installation of Outlook 2010 or Outlook 2013.</span></span> <span data-ttu-id="d5c2b-137">レジストリ内 `VirtualOutlook` の次の場所にあるキー Windowsします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-137">Examine the  `VirtualOutlook` key in the following location in the Windows registry:</span></span> 
      
      - <span data-ttu-id="d5c2b-138">2010 Outlookの場合、`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`</span><span class="sxs-lookup"><span data-stu-id="d5c2b-138">For Outlook 2010,  `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`</span></span>
      
      - <span data-ttu-id="d5c2b-139">ソーシャル Outlook 2013 の場合、`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`</span><span class="sxs-lookup"><span data-stu-id="d5c2b-139">For Outlook Social Connector 2013,  `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`</span></span>
      
      <span data-ttu-id="d5c2b-140">キー  `VirtualOutlook` は、REG_SZのロケール タグ ("en-us" など) を含む値です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-140">The  `VirtualOutlook` key is a REG_SZ value that contains the locale tag, such as "en-us", of the installed product.</span></span> 
      
   2. <span data-ttu-id="d5c2b-141">キーが存在しない場合Outlookクライアント コンピューターに存在しない場合、プロバイダーのインストール手順 `VirtualOutlook` を完了できません。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-141">If the  `VirtualOutlook` key does not exist, Outlook is not present on the client computer, and the provider installation procedure cannot complete.</span></span> <span data-ttu-id="d5c2b-142">OSC プロバイダーのインストールに進む前に、サポートされているバージョンOutlook OSC を入手してください。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-142">Inform the user to obtain a supported version of Outlook and the OSC before proceeding to install the OSC provider.</span></span> 
      
   3. <span data-ttu-id="d5c2b-143">キーが `VirtualOutlook` 存在する場合は、Outlookコンピュータークイック実行によって配信されました。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-143">If the  `VirtualOutlook` key does exist, Outlook was delivered by Click-to-Run on the client computer.</span></span> <span data-ttu-id="d5c2b-144">OSC タイプ ライブラリのインストール済みバージョンを確認するには、次の場所にあるキーをレジストリWindows `OSCVersion` します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-144">Proceed to check the installed version of the OSC type library by examining the  `OSCVersion` key in the following location in the Windows registry:</span></span> 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      <span data-ttu-id="d5c2b-145">値は、タイプ ライブラリのバージョン番号  `OSCVersion` Socialprovider.dll ("1.0"、"1.1"、または "15" など) を指定する文字列です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-145">The value of  `OSCVersion` is a string that specifies the type library version number of Socialprovider.dll (for example, "1.0", "1.1", or "15").</span></span> 
      
   4. <span data-ttu-id="d5c2b-146">`OSCVersion`"1.0"、"1.1" または "15" の場合は、適切なバージョンの OSC がインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-146">If  `OSCVersion` is "1.0", "1.1" or "15", an appropriate version of OSC is installed.</span></span> <span data-ttu-id="d5c2b-147">手順 6 に進み、最新バージョンの OSC Outlookを準備するために、現在のユーザー インターフェイス ロケールを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-147">Proceed to step 6 to find the current Outlook user interface locale to prepare for installing the latest version of the OSC.</span></span> 
      
   5. <span data-ttu-id="d5c2b-148">それ以外の場合  `OSCVersion` 、予期される値は含めされません。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-148">Otherwise,  `OSCVersion` does not contain an expected value.</span></span> <span data-ttu-id="d5c2b-149">手順 6 に進み、適切なバージョンの OSC をインストールOutlookする現在のユーザー インターフェイス ロケールを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-149">Proceed to step 6 to find the current Outlook user interface locale to prepare for installing an appropriate version of the OSC.</span></span> 
    
3. <span data-ttu-id="d5c2b-150">**クライアント コンピューターに 2003 Outlook 2007 Outlookインストールされている場合は、次の手順に進みます。**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-150">**Proceed with this step if Outlook 2003 or Outlook 2007 is installed on the client computer:**</span></span>
    
   1. <span data-ttu-id="d5c2b-151">次の修飾されたコンポーネント ID が存在するかどうかをテストするインストーラー カスタム アクションを記述して、OSC がインストールされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-151">Verify whether the OSC is installed by writing an installer custom action to test for the existence of the following qualified component ID:</span></span>
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      <span data-ttu-id="d5c2b-152">修飾されたコンポーネント ID は、ポインターと同様に、単一レベルの間接参照のメソッドを提供する GUID です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-152">The qualified component ID is a GUID that provides a method of single-level indirection, similar to a pointer.</span></span> <span data-ttu-id="d5c2b-153">インストーラーの詳細については、「Windowsドキュメント[へのロードマップ」をWindowsしてください](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation)。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-153">For more information about Windows Installer, see [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).</span></span>
      
   2. <span data-ttu-id="d5c2b-154">指定した修飾コンポーネントが存在する場合は、OSC のバージョンがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-154">If the specified qualified component exists, a version of the OSC is installed.</span></span> <span data-ttu-id="d5c2b-155">手順 5 に進み、最新バージョンの OSC Outlook準備するために、現在のユーザー インターフェイス ロケールを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-155">Proceed to step 5 to find the current Outlook user interface locale to prepare for installing the latest version of the OSC.</span></span>
      
   3. <span data-ttu-id="d5c2b-156">それ以外の場合、OSC はインストールされません。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-156">Otherwise, the OSC is not installed.</span></span> <span data-ttu-id="d5c2b-157">手順 6 に進み、適切なバージョンの OSC をインストールOutlookする現在のユーザー インターフェイス ロケールを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-157">Proceed to step 6 to find the current Outlook user interface locale to prepare for installing an appropriate version of the OSC.</span></span>
      
4. <span data-ttu-id="d5c2b-158">**クライアント コンピューターに 2010 Outlook 2013 Outlookインストールされている場合は、次の手順に進みます。**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-158">**Proceed with this step if Outlook 2010 or Outlook 2013 is installed on the client computer:**</span></span>
    
   1. <span data-ttu-id="d5c2b-159">レジストリ内の次の場所にあるキーを調Outlookして、インストールされているバージョンのコンピューターのビット `Bitness` Windowsします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-159">Determine the bitness of the installed version of Outlook by examining the  `Bitness` key in the following location in the Windows registry:</span></span> 
      
      - <span data-ttu-id="d5c2b-160">2010 Outlookについては、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`</span><span class="sxs-lookup"><span data-stu-id="d5c2b-160">For Outlook 2010, look at  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`</span></span>
      
      - <span data-ttu-id="d5c2b-161">2013 Outlookについては、`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`</span><span class="sxs-lookup"><span data-stu-id="d5c2b-161">For Outlook 2013, look at  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`</span></span>
      
      <span data-ttu-id="d5c2b-162">キーは、32 ビット Outlookの場合は `Bitness` "x86"、64 ビット の場合は "x64" Outlook。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-162">The  `Bitness` key is "x86" for 32-bit Outlook, or "x64" for 64-bit Outlook.</span></span> 
      
   2. <span data-ttu-id="d5c2b-163">プロバイダーが管理プロバイダーであり、ターゲット プラットフォームを **Any CPU** として指定するプロバイダー コンポーネントをコンパイルした場合は、手順 6 に進み、最新バージョンの OSC のインストールを準備するために現在の Outlook ユーザー インターフェイス ロケールを検索します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-163">If your provider is a managed provider, and you compiled the provider component specifying the target platform as **Any CPU**, proceed with step 6 to find the current Outlook user interface locale to prepare for installing the latest version of the OSC.</span></span> <span data-ttu-id="d5c2b-164">プロバイダーは、OSC の 32 ビット バージョンと 64 ビット バージョンの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-164">Your provider will work on both 32-bit and 64-bit versions of the OSC.</span></span>
      
   3. <span data-ttu-id="d5c2b-165">プロバイダーがネイティブ COM コンポーネントの場合は、インストールされているバージョンのデバイスのビット数をOutlook。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-165">If your provider is a native COM component, examine the bitness of the installed version of Outlook:</span></span>
      
      - <span data-ttu-id="d5c2b-166">インストールされているバージョンの Outlook が 32 ビットの場合、適切な OSC がインストールされていることを確認した後、インストール手順で 32 ビット プロバイダーをインストールする必要があります (手順 8)。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-166">If the installed version of Outlook is 32-bit, your installation procedure will have to install a 32-bit provider (in step 8), after ensuring that an appropriate OSC is installed.</span></span>
      
      - <span data-ttu-id="d5c2b-167">それ以外の場合、インストールされているバージョンの Outlook は 64 ビットであり、適切な OSC がインストールされていることを確認した後、インストール手順で 64 ビット プロバイダーをインストールする必要があります (手順 8)。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-167">Otherwise, the installed version of Outlook is 64-bit, and your installation procedure will have to install a 64-bit provider (in step 8), after ensuring that an appropriate OSC is installed.</span></span> 
      
   4. <span data-ttu-id="d5c2b-168">手順 6 に進み、適切なバージョンの OSC Outlookを準備するために、現在のユーザー インターフェイス ロケールを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-168">Proceed with step 6 to find the current Outlook user interface locale to prepare for installing an appropriate version of the OSC.</span></span>
    
5. <span data-ttu-id="d5c2b-169">**2003 または Outlook 2007** Outlook OSC がクライアント コンピューターにインストールされている場合は、次の手順に進みます。ユーザー インターフェイスの現在Outlookロケールを確認するには、次の場所にあるキーをレジストリ `OSCLcid` Windowsします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-169">**Proceed with this step if Outlook 2003 or Outlook 2007 is installed, and the OSC is installed on the client computer:** Check the current Outlook user interface locale by examining the  `OSCLcid` key in the following location in the Windows registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   <span data-ttu-id="d5c2b-170">キーは、現在の Outlook ユーザー インターフェイス ロケールを表すインターネット エンジニアリング タスク フォース (IETF) ロケール タグ `OSCLcid` [([RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)で定義) を指定する DWORD 値です。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-170">The  `OSCLcid` key is a DWORD value that specifies the Internet Engineering Task Force (IETF) locale tag (defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), that represents the current Outlook user interface locale.</span></span> <span data-ttu-id="d5c2b-171">手順 7 に進み、最新の OSC をクライアント コンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-171">Proceed with step 7 to install the latest OSC on the client computer.</span></span>
    
6. <span data-ttu-id="d5c2b-172">**Outlook 2003 または Outlook 2007 がインストールされている場合、または Outlook 2010 または Outlook 2013 が存在するが、最新の OSC が必ずしもクライアント コンピューターにインストールされていない場合は、この手順を実行します。**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-172">**Proceed with this step if Outlook 2003 or Outlook 2007 is installed, or Outlook 2010 or Outlook 2013 is present, but the latest OSC is not necessarily installed on the client computer:**</span></span>
    
   <span data-ttu-id="d5c2b-173">**LanguageSettings オブジェクトを使用** して、ユーザー インターフェイス ロケールの LCID Outlook決定します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-173">Use the **LanguageSettings** object to determine the LCID of the Outlook user interface locale.</span></span> <span data-ttu-id="d5c2b-174">次のVisual Basicスクリプト エディション (VBScript) コード スニペットは、ユーザー インターフェイス ロケールの LCID を取得Outlook示しています。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-174">The following Visual Basic Scripting Edition (VBScript) code snippet demonstrates how to obtain the LCID of the Outlook user interface locale.</span></span> 
    
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

7. <span data-ttu-id="d5c2b-175">**インストーラーにインストールされているバージョンの LCID Outlook があるが、最新の OSC が必ずしもクライアント コンピューターにインストールされていない場合は、次の手順を実行します。**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-175">**Proceed with this step if the installer has the LCID of the installed version of Outlook, but the latest OSC is not necessarily installed on the client computer:**</span></span>
    
   <span data-ttu-id="d5c2b-176">g-link をインストール パッケージにチェーンして、最新バージョンの OSC がクライアント コンピューターにインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-176">Chain a g-link into your installation package to ensure that the latest version of the OSC is installed on the client computer.</span></span> <span data-ttu-id="d5c2b-177">g-link 形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-177">The g-link format is as follows:</span></span>
    
   <span data-ttu-id="d5c2b-178"> https://g.live.com/0CR_LCID_ / _Glink_</span><span class="sxs-lookup"><span data-stu-id="d5c2b-178">https://g.live.com/0CR _LCID_/ _Glink_</span></span>
    
   <span data-ttu-id="d5c2b-179">サポートされている LCID 値については、以下の表 1、サポートされている  _Glink_ 値については表 2  _を参照_ してください。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-179">Refer to Table 1 below for the supported  _LCID_ values, and Table 2 for the supported  _Glink_ values.</span></span> <span data-ttu-id="d5c2b-180">たとえば、32 ビット Outlook Social Connector 2013 (米国英語) 用の 32 ビット OSC の最新バージョンをインストールする g-link は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-180">For example, the g-link to install the latest version of the 32-bit OSC for 32-bit Outlook Social Connector 2013 (US English) is as follows:</span></span> 
    
   https://g.live.com/0CR1033/82
    
8. <span data-ttu-id="d5c2b-181">プロバイダーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-181">Install the provider.</span></span> <span data-ttu-id="d5c2b-182">プロバイダーのインストール手順では、プログラム識別子 (ProgID) をレジストリの適切な場所Windowsする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-182">The provider installation procedure must register the programmatic identifier (ProgID) in the appropriate Windows registry location.</span></span> <span data-ttu-id="d5c2b-183">詳細については、「プロバイダーの [登録」を参照してください](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-183">For more information, see [Registering a Provider](registering-a-provider.md).</span></span> <span data-ttu-id="d5c2b-184">また、インストールするプロバイダーのビット数が、クライアント コンピューターに存在するバージョンのビットOutlook同じことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-184">Also, be sure that the bitness of the provider to be installed is the same as the bitness of the version of Outlook present on the client computer.</span></span> <span data-ttu-id="d5c2b-185">たとえば、32 ビット Outlook 2013 が存在する場合は 32 ビット プロバイダーをインストールし、64 ビット Outlook 2013 がインストールされている場合は 64 ビット プロバイダーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-185">For example, install a 32-bit provider if 32-bit Outlook 2013 is present, and a 64-bit provider if 64-bit Outlook 2013 is installed.</span></span> <span data-ttu-id="d5c2b-186">2003 Outlook 2007 の場合、プロバイダーの 32 ビット バージョンだけが適用されます。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-186">For Outlook 2003 or 2007, only the 32-bit version of your provider applies.</span></span> 
    
<span data-ttu-id="d5c2b-187">**表 1: OSC でサポートされているロケールと対応する LCID 値 (16 進数)**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-187">**Table 1: Supported locale and corresponding LCID values in hexadecimal for the OSC**</span></span>
  
|<span data-ttu-id="d5c2b-188">**Locale**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-188">**Locale**</span></span>|<span data-ttu-id="d5c2b-189">**LCID**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-189">**LCID**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5c2b-190">ar-sa</span><span class="sxs-lookup"><span data-stu-id="d5c2b-190">ar-sa</span></span>  <br/> |<span data-ttu-id="d5c2b-191">1025</span><span class="sxs-lookup"><span data-stu-id="d5c2b-191">1025</span></span>  <br/> |
|<span data-ttu-id="d5c2b-192">bg-bg</span><span class="sxs-lookup"><span data-stu-id="d5c2b-192">bg-bg</span></span>  <br/> |<span data-ttu-id="d5c2b-193">1026</span><span class="sxs-lookup"><span data-stu-id="d5c2b-193">1026</span></span>  <br/> |
|<span data-ttu-id="d5c2b-194">ca-es</span><span class="sxs-lookup"><span data-stu-id="d5c2b-194">ca-es</span></span>  <br/> |<span data-ttu-id="d5c2b-195">1027</span><span class="sxs-lookup"><span data-stu-id="d5c2b-195">1027</span></span>  <br/> |
|<span data-ttu-id="d5c2b-196">cs-cz</span><span class="sxs-lookup"><span data-stu-id="d5c2b-196">cs-cz</span></span>  <br/> |<span data-ttu-id="d5c2b-197">1029</span><span class="sxs-lookup"><span data-stu-id="d5c2b-197">1029</span></span>  <br/> |
|<span data-ttu-id="d5c2b-198">da-dk</span><span class="sxs-lookup"><span data-stu-id="d5c2b-198">da-dk</span></span>  <br/> |<span data-ttu-id="d5c2b-199">1030</span><span class="sxs-lookup"><span data-stu-id="d5c2b-199">1030</span></span>  <br/> |
|<span data-ttu-id="d5c2b-200">de-de</span><span class="sxs-lookup"><span data-stu-id="d5c2b-200">de-de</span></span>  <br/> |<span data-ttu-id="d5c2b-201">1031</span><span class="sxs-lookup"><span data-stu-id="d5c2b-201">1031</span></span>  <br/> |
|<span data-ttu-id="d5c2b-202">el-gr</span><span class="sxs-lookup"><span data-stu-id="d5c2b-202">el-gr</span></span>  <br/> |<span data-ttu-id="d5c2b-203">1032</span><span class="sxs-lookup"><span data-stu-id="d5c2b-203">1032</span></span>  <br/> |
|<span data-ttu-id="d5c2b-204">ja-jp</span><span class="sxs-lookup"><span data-stu-id="d5c2b-204">en-us</span></span>  <br/> |<span data-ttu-id="d5c2b-205">1033</span><span class="sxs-lookup"><span data-stu-id="d5c2b-205">1033</span></span>  <br/> |
|<span data-ttu-id="d5c2b-206">es-es</span><span class="sxs-lookup"><span data-stu-id="d5c2b-206">es-es</span></span>  <br/> |<span data-ttu-id="d5c2b-207">3082</span><span class="sxs-lookup"><span data-stu-id="d5c2b-207">3082</span></span>  <br/> |
|<span data-ttu-id="d5c2b-208">et-ee</span><span class="sxs-lookup"><span data-stu-id="d5c2b-208">et-ee</span></span>  <br/> |<span data-ttu-id="d5c2b-209">1061</span><span class="sxs-lookup"><span data-stu-id="d5c2b-209">1061</span></span>  <br/> |
|<span data-ttu-id="d5c2b-210">eu-es</span><span class="sxs-lookup"><span data-stu-id="d5c2b-210">eu-es</span></span>  <br/> |<span data-ttu-id="d5c2b-211">1069</span><span class="sxs-lookup"><span data-stu-id="d5c2b-211">1069</span></span>  <br/> |
|<span data-ttu-id="d5c2b-212">fi-fi</span><span class="sxs-lookup"><span data-stu-id="d5c2b-212">fi-fi</span></span>  <br/> |<span data-ttu-id="d5c2b-213">1035</span><span class="sxs-lookup"><span data-stu-id="d5c2b-213">1035</span></span>  <br/> |
|<span data-ttu-id="d5c2b-214">fr-fr</span><span class="sxs-lookup"><span data-stu-id="d5c2b-214">fr-fr</span></span>  <br/> |<span data-ttu-id="d5c2b-215">1036</span><span class="sxs-lookup"><span data-stu-id="d5c2b-215">1036</span></span>  <br/> |
|<span data-ttu-id="d5c2b-216">gl-es</span><span class="sxs-lookup"><span data-stu-id="d5c2b-216">gl-es</span></span>  <br/> |<span data-ttu-id="d5c2b-217">1110</span><span class="sxs-lookup"><span data-stu-id="d5c2b-217">1110</span></span>  <br/> |
|<span data-ttu-id="d5c2b-218">he-il</span><span class="sxs-lookup"><span data-stu-id="d5c2b-218">he-il</span></span>  <br/> |<span data-ttu-id="d5c2b-219">1037</span><span class="sxs-lookup"><span data-stu-id="d5c2b-219">1037</span></span>  <br/> |
|<span data-ttu-id="d5c2b-220">hi-in</span><span class="sxs-lookup"><span data-stu-id="d5c2b-220">hi-in</span></span>  <br/> |<span data-ttu-id="d5c2b-221">1081</span><span class="sxs-lookup"><span data-stu-id="d5c2b-221">1081</span></span>  <br/> |
|<span data-ttu-id="d5c2b-222">hr-hr</span><span class="sxs-lookup"><span data-stu-id="d5c2b-222">hr-hr</span></span>  <br/> |<span data-ttu-id="d5c2b-223">1050</span><span class="sxs-lookup"><span data-stu-id="d5c2b-223">1050</span></span>  <br/> |
|<span data-ttu-id="d5c2b-224">hu-hu</span><span class="sxs-lookup"><span data-stu-id="d5c2b-224">hu-hu</span></span>  <br/> |<span data-ttu-id="d5c2b-225">1038</span><span class="sxs-lookup"><span data-stu-id="d5c2b-225">1038</span></span>  <br/> |
|<span data-ttu-id="d5c2b-226">it-it</span><span class="sxs-lookup"><span data-stu-id="d5c2b-226">it-it</span></span>  <br/> |<span data-ttu-id="d5c2b-227">1040</span><span class="sxs-lookup"><span data-stu-id="d5c2b-227">1040</span></span>  <br/> |
|<span data-ttu-id="d5c2b-228">ja-jp</span><span class="sxs-lookup"><span data-stu-id="d5c2b-228">ja-jp</span></span>  <br/> |<span data-ttu-id="d5c2b-229">1041</span><span class="sxs-lookup"><span data-stu-id="d5c2b-229">1041</span></span>  <br/> |
|<span data-ttu-id="d5c2b-230">kk-kz</span><span class="sxs-lookup"><span data-stu-id="d5c2b-230">kk-kz</span></span>  <br/> |<span data-ttu-id="d5c2b-231">1087</span><span class="sxs-lookup"><span data-stu-id="d5c2b-231">1087</span></span>  <br/> |
|<span data-ttu-id="d5c2b-232">ko-kr</span><span class="sxs-lookup"><span data-stu-id="d5c2b-232">ko-kr</span></span>  <br/> |<span data-ttu-id="d5c2b-233">1042</span><span class="sxs-lookup"><span data-stu-id="d5c2b-233">1042</span></span>  <br/> |
|<span data-ttu-id="d5c2b-234">lt-lt</span><span class="sxs-lookup"><span data-stu-id="d5c2b-234">lt-lt</span></span>  <br/> |<span data-ttu-id="d5c2b-235">1063</span><span class="sxs-lookup"><span data-stu-id="d5c2b-235">1063</span></span>  <br/> |
|<span data-ttu-id="d5c2b-236">lv-lv</span><span class="sxs-lookup"><span data-stu-id="d5c2b-236">lv-lv</span></span>  <br/> |<span data-ttu-id="d5c2b-237">1062</span><span class="sxs-lookup"><span data-stu-id="d5c2b-237">1062</span></span>  <br/> |
|<span data-ttu-id="d5c2b-238">nb-no</span><span class="sxs-lookup"><span data-stu-id="d5c2b-238">nb-no</span></span>  <br/> |<span data-ttu-id="d5c2b-239">1044</span><span class="sxs-lookup"><span data-stu-id="d5c2b-239">1044</span></span>  <br/> |
|<span data-ttu-id="d5c2b-240">nl-nl</span><span class="sxs-lookup"><span data-stu-id="d5c2b-240">nl-nl</span></span>  <br/> |<span data-ttu-id="d5c2b-241">1043</span><span class="sxs-lookup"><span data-stu-id="d5c2b-241">1043</span></span>  <br/> |
|<span data-ttu-id="d5c2b-242">pl-pl</span><span class="sxs-lookup"><span data-stu-id="d5c2b-242">pl-pl</span></span>  <br/> |<span data-ttu-id="d5c2b-243">1045</span><span class="sxs-lookup"><span data-stu-id="d5c2b-243">1045</span></span>  <br/> |
|<span data-ttu-id="d5c2b-244">pt-br</span><span class="sxs-lookup"><span data-stu-id="d5c2b-244">pt-br</span></span>  <br/> |<span data-ttu-id="d5c2b-245">1046</span><span class="sxs-lookup"><span data-stu-id="d5c2b-245">1046</span></span>  <br/> |
|<span data-ttu-id="d5c2b-246">pt-pt</span><span class="sxs-lookup"><span data-stu-id="d5c2b-246">pt-pt</span></span>  <br/> |<span data-ttu-id="d5c2b-247">2070</span><span class="sxs-lookup"><span data-stu-id="d5c2b-247">2070</span></span>  <br/> |
|<span data-ttu-id="d5c2b-248">ro-ro</span><span class="sxs-lookup"><span data-stu-id="d5c2b-248">ro-ro</span></span>  <br/> |<span data-ttu-id="d5c2b-249">1048</span><span class="sxs-lookup"><span data-stu-id="d5c2b-249">1048</span></span>  <br/> |
|<span data-ttu-id="d5c2b-250">ru-ru</span><span class="sxs-lookup"><span data-stu-id="d5c2b-250">ru-ru</span></span>  <br/> |<span data-ttu-id="d5c2b-251">1049</span><span class="sxs-lookup"><span data-stu-id="d5c2b-251">1049</span></span>  <br/> |
|<span data-ttu-id="d5c2b-252">sk-sk</span><span class="sxs-lookup"><span data-stu-id="d5c2b-252">sk-sk</span></span>  <br/> |<span data-ttu-id="d5c2b-253">1051</span><span class="sxs-lookup"><span data-stu-id="d5c2b-253">1051</span></span>  <br/> |
|<span data-ttu-id="d5c2b-254">sl-si</span><span class="sxs-lookup"><span data-stu-id="d5c2b-254">sl-si</span></span>  <br/> |<span data-ttu-id="d5c2b-255">1060</span><span class="sxs-lookup"><span data-stu-id="d5c2b-255">1060</span></span>  <br/> |
|<span data-ttu-id="d5c2b-256">sr-cyrl-cs</span><span class="sxs-lookup"><span data-stu-id="d5c2b-256">sr-cyrl-cs</span></span>  <br/> |<span data-ttu-id="d5c2b-257">3098</span><span class="sxs-lookup"><span data-stu-id="d5c2b-257">3098</span></span>  <br/> |
|<span data-ttu-id="d5c2b-258">sr-latn-cs</span><span class="sxs-lookup"><span data-stu-id="d5c2b-258">sr-latn-cs</span></span>  <br/> |<span data-ttu-id="d5c2b-259">2074</span><span class="sxs-lookup"><span data-stu-id="d5c2b-259">2074</span></span>  <br/> |
|<span data-ttu-id="d5c2b-260">sv-se</span><span class="sxs-lookup"><span data-stu-id="d5c2b-260">sv-se</span></span>  <br/> |<span data-ttu-id="d5c2b-261">1053</span><span class="sxs-lookup"><span data-stu-id="d5c2b-261">1053</span></span>  <br/> |
|<span data-ttu-id="d5c2b-262">th-th</span><span class="sxs-lookup"><span data-stu-id="d5c2b-262">th-th</span></span>  <br/> |<span data-ttu-id="d5c2b-263">1054</span><span class="sxs-lookup"><span data-stu-id="d5c2b-263">1054</span></span>  <br/> |
|<span data-ttu-id="d5c2b-264">tr-tr</span><span class="sxs-lookup"><span data-stu-id="d5c2b-264">tr-tr</span></span>  <br/> |<span data-ttu-id="d5c2b-265">1055</span><span class="sxs-lookup"><span data-stu-id="d5c2b-265">1055</span></span>  <br/> |
|<span data-ttu-id="d5c2b-266">uk-ua</span><span class="sxs-lookup"><span data-stu-id="d5c2b-266">uk-ua</span></span>  <br/> |<span data-ttu-id="d5c2b-267">1058</span><span class="sxs-lookup"><span data-stu-id="d5c2b-267">1058</span></span>  <br/> |
|<span data-ttu-id="d5c2b-268">zh-cn</span><span class="sxs-lookup"><span data-stu-id="d5c2b-268">zh-cn</span></span>  <br/> |<span data-ttu-id="d5c2b-269">2052</span><span class="sxs-lookup"><span data-stu-id="d5c2b-269">2052</span></span>  <br/> |
|<span data-ttu-id="d5c2b-270">zh-tw</span><span class="sxs-lookup"><span data-stu-id="d5c2b-270">zh-tw</span></span>  <br/> |<span data-ttu-id="d5c2b-271">1028</span><span class="sxs-lookup"><span data-stu-id="d5c2b-271">1028</span></span>  <br/> |
   
<span data-ttu-id="d5c2b-272">**表 2: OSC でサポートされている Glink 値**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-272">**Table 2: Supported Glink values for the OSC**</span></span>
  
|<span data-ttu-id="d5c2b-273">**Glink 値**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-273">**Glink value**</span></span>|<span data-ttu-id="d5c2b-274">**Function**</span><span class="sxs-lookup"><span data-stu-id="d5c2b-274">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5c2b-275">80</span><span class="sxs-lookup"><span data-stu-id="d5c2b-275">80</span></span>  <br/> |<span data-ttu-id="d5c2b-276">最新バージョンの OSC for Outlook 2003 または Outlook 2007 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-276">Installs the latest version of OSC for Outlook 2003 or Outlook 2007.</span></span>  <br/> |
|<span data-ttu-id="d5c2b-277">82</span><span class="sxs-lookup"><span data-stu-id="d5c2b-277">82</span></span>  <br/> |<span data-ttu-id="d5c2b-278">Outlook 2007、Outlook 2010、または Outlook Social Connector 2013 用の 32 ビット OSC の最新パッチをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-278">Installs the latest patch of 32-bit OSC for Outlook 2007, Outlook 2010, or Outlook Social Connector 2013.</span></span>  <br/> |
|<span data-ttu-id="d5c2b-279">83</span><span class="sxs-lookup"><span data-stu-id="d5c2b-279">83</span></span>  <br/> |<span data-ttu-id="d5c2b-280">Outlook 2010 または Outlook Social Connector 2013 用の 64 ビット OSC の最新パッチをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d5c2b-280">Installs the latest patch of 64-bit OSC for Outlook 2010 or Outlook Social Connector 2013.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5c2b-281">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5c2b-281">See also</span></span>

- [<span data-ttu-id="d5c2b-282">プロバイダーの登録</span><span class="sxs-lookup"><span data-stu-id="d5c2b-282">Registering a Provider</span></span>](registering-a-provider.md) 
- [<span data-ttu-id="d5c2b-283">プロバイダーを開発するための学習のクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="d5c2b-283">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="d5c2b-284">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="d5c2b-284">Deploying a Provider</span></span>](deploying-a-provider.md)

