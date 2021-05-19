---
title: 読み込む MAPI の特定のバージョンを選択する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344521"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="4e2b0-103">読み込む MAPI の特定のバージョンを選択する</span><span class="sxs-lookup"><span data-stu-id="4e2b0-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="4e2b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e2b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e2b0-105">MAPI の実装に明示的にリンクする場合は、読み込む実装を慎重に選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="4e2b0-106">MAPI の実装に明示的にリンクする 2 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="4e2b0-107">MAPI スタブ ライブラリを読み込み、MAPI 呼び出しを読み込み、ディスパッチするカスタム DLL をレジストリに指定できます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="4e2b0-108">MAPI クライアント参照アルゴリズムを実装して、既定のメール クライアントで使用される MAPI のバージョンを検索し、読み込みできます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="4e2b0-109">[Mapi32.dll ス](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)タブ レジストリ 設定 を変更して、アプリケーションに MAPI の実装を使用することを指示することができますので、テストした MAPI の実装を使用するアプリケーションに指示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="4e2b0-110">次に、両方のリンク方法を明示的に説明します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="4e2b0-111">レジストリからの読み取り</span><span class="sxs-lookup"><span data-stu-id="4e2b0-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="4e2b0-112">レジストリから MAPI 実装情報を読み取る方法</span><span class="sxs-lookup"><span data-stu-id="4e2b0-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="4e2b0-113">メール クライアントのカスタム DLL を示すレジストリ キーは、メール クライアントのキー  `HKLM\Software\Clients\Mail` の下に置きます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="4e2b0-114">次の表では、これらのキーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="4e2b0-115">**キー**</span><span class="sxs-lookup"><span data-stu-id="4e2b0-115">**Key**</span></span>|<span data-ttu-id="4e2b0-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="4e2b0-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="4e2b0-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="4e2b0-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="4e2b0-118">単純Windows MAPI 呼び出しをエクスポートする DLL を識別する、インストーラー PublishComponent カテゴリ ID (GUID) です。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="4e2b0-119">設定されている場合、このキーは **DLLPath** キーまたは **DLLPathEx キーよりも優先** されます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="4e2b0-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="4e2b0-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="4e2b0-121">アプリケーションのロケール識別子 (LCID)。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="4e2b0-122">最初の文字列値はサブキーを識別し、以降の文字列値は、ロケール情報を含むこのキーの下にあるレジストリ値  `HKLM\Software` を識別します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="4e2b0-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="4e2b0-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="4e2b0-124">LCIDs for Microsoft Office。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="4e2b0-125">最初の文字列値はサブキーを識別し、以降の文字列値は、このキーの下のレジストリ値  `HKLM\Software` を識別します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="4e2b0-126">これらのキーから情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="4e2b0-127">前の手順で取得した値を [FGetComponentPath 関数に渡](fgetcomponentpath.md) します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="4e2b0-128">**FGetComponentPath** は、MAPI スタブ ライブラリによってエクスポートされる関数Mapistub.dll。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="4e2b0-129">MAPI のカスタム バージョンのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="4e2b0-130">既定としてマークされている MAPI の実装を読み込むには</span><span class="sxs-lookup"><span data-stu-id="4e2b0-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="4e2b0-131">レジストリ値  `HKLM\Software\Clients\Mail::(default)` を読み取る。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="4e2b0-132">前述のように、指定されたクライアントの情報を参照します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4e2b0-133">既定のメール クライアントは拡張 MAPI を実装しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="4e2b0-134">例</span><span class="sxs-lookup"><span data-stu-id="4e2b0-134">Example</span></span>

<span data-ttu-id="4e2b0-135">MAPI を読み込むには、Outlookでレジストリ キーを検索し、 `HKLM\Software\Clients\Mail\Microsoft Outlook` **それらを FGetComponentPath に渡します**。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="4e2b0-136">**FGetComponentPath** は、MAPI のOutlookパスを返します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="4e2b0-137">キー MSIComponentID、MSIApplicationLCID、および **MSIOfficeLCID** が設定されていない場合は **、DLLPathEx** レジストリ値を確認します。  </span><span class="sxs-lookup"><span data-stu-id="4e2b0-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="4e2b0-138">キーが設定されている場合 **、FGetComponentPath は** クライアントの MAPI 実装のパスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="4e2b0-139">MAPI クライアント 参照アルゴリズムの実装</span><span class="sxs-lookup"><span data-stu-id="4e2b0-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="4e2b0-140">次の表に、MAPI のカスタム実装のパスを検索するために使用される MFCMAPI の 4 つの関数を示します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="4e2b0-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="4e2b0-141">**Function**</span></span>|<span data-ttu-id="4e2b0-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="4e2b0-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="4e2b0-143">MAPI ライブラリ パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="4e2b0-144">MAPI メール レジストリ キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="4e2b0-145">インストーラー識別子Windows取得します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="4e2b0-146">[FGetComponentPath を使用してコンポーネント パスを取得します](fgetcomponentpath.md)。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="4e2b0-147">MFCMAPI は既定で MAPI の既定の実装を読み込むため、MAPI の別の実装を使用する場合は、明示的に指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="4e2b0-148">これは **、Session\Load MAPI ルーチンを使用して実行** されます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="4e2b0-149">これらの関数の動作</span><span class="sxs-lookup"><span data-stu-id="4e2b0-149">How these functions work</span></span>

1. <span data-ttu-id="4e2b0-150">MFCMAPI は、既定の MAPI 実装を読み込むには、クライアント パラメーター  `GetMAPIPath` に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="4e2b0-151">`GetMAPIPath``GetMapiMsiIds` **MSIComponentID、MSIApplicationLCID、\*\*\*\*および MSIOfficeLCID** の値を読み取 **る呼び出し**。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="4e2b0-152">`GetMapiMsiIds` 既定  `GetMailKey` のメール クライアントのレジストリ キーを開く呼び出し。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="4e2b0-153">`GetMapiMsiIds``GetMailKey` **MSIComponentID、MSIApplicationLCID、および** **MSIOfficeLCID** の値を検索するために返されるレジストリ ハンドルを使用します。 </span><span class="sxs-lookup"><span data-stu-id="4e2b0-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="4e2b0-154">MSIComponentID、MSIApplicationLCID、**および MSIOfficeLCID** の値がに返されます `GetMAPIPath` 。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="4e2b0-155">`GetMAPIPath` 次に、それらをに渡します  `GetComponentPath` 。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="4e2b0-156">`GetComponentPath` システム ディレクトリから MAPI スタブ ライブラリMapi32.dll読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="4e2b0-157">`GetComponentPath` 次に **、FGetComponentPath** 関数のアドレスを取得Mapi32.dll **FGetComponentPath** をエクスポートMapi32.dll仮定します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="4e2b0-158">**FGetComponentPath** のアドレスを取得すると、Mapi32.dllからアドレス `GetComponentPath` を取得Mapistub.dll。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="4e2b0-159">`GetComponentPath` 次に、既定のバージョンの MAPI のパスを取得する **FGetComponentPath** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="4e2b0-160">`GetMAPIPath` 次に、このパスを呼び出し元に返し、MAPI を読み込み、MAPI 関数へのリンクの説明に従って明示的に [リンクします](how-to-link-to-mapi-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="4e2b0-161">英語および英語以外のロケール用に MAPI のローカライズされたコピーをサポートするには  `GetMAPIPath` **、MSIApplicationLCID** サブキーと **MSIOfficeLCID** サブキーの値を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="4e2b0-162">`GetMAPIPath` 次に **、FGetComponentPath** を呼び出し、まず **MSIApplicationLCID** を **szQualifier** として指定し **、MSIOfficeLCID** を **szQualifier** として指定します。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="4e2b0-163">英語以外の言語をサポートするメール クライアントのレジストリ キーの詳細については、「MAPI DLL の MSI キーのセットアップ」 [を参照してください](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="4e2b0-164">MFCMAPI が MAPI のパスを使用して受信しない場合は、システム ディレクトリから MAPI スタブ  `GetMAPIPath` ライブラリが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="4e2b0-165">「MAPI 呼び出しを [MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) DLL に明示的にマッピングする」で説明されている **MSMapiApps** レジストリ値は、MAPI スタブ ライブラリが使用されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="4e2b0-166">MAPI の特定の実装を読み込むアプリケーション、または既定の実装を読み込むアプリケーションは **、MSMapiApps** レジストリ キーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e2b0-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4e2b0-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e2b0-167">See also</span></span>

- [<span data-ttu-id="4e2b0-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="4e2b0-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="4e2b0-169">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="4e2b0-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="4e2b0-170">MAPI 関数へのリンク</span><span class="sxs-lookup"><span data-stu-id="4e2b0-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="4e2b0-171">Mapi32.dllスタブ レジストリ 設定</span><span class="sxs-lookup"><span data-stu-id="4e2b0-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="4e2b0-172">MAPI DLL の MSI キーのセットアップ</span><span class="sxs-lookup"><span data-stu-id="4e2b0-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="4e2b0-173">MAPI 呼び出しを MAPI DLL に明示的にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4e2b0-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

