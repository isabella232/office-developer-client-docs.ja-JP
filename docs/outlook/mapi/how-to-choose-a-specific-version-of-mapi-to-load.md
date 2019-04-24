---
title: 読み込む MAPI の特定のバージョンを選択する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344521"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="7bf94-103">読み込む MAPI の特定のバージョンを選択する</span><span class="sxs-lookup"><span data-stu-id="7bf94-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="7bf94-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bf94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bf94-105">MAPI の実装に明示的にリンクする場合は、読み込む実装を慎重に選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf94-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="7bf94-106">MAPI の実装に明示的にリンクするには、2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="7bf94-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="7bf94-107">mapi スタブライブラリを読み込み、レジストリにカスタム DLL を指定して、mapi 呼び出しを読み込んでディスパッチすることができます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="7bf94-108">mapi クライアント参照アルゴリズムを実装すると、既定のメールクライアントで使用される mapi のバージョンを検索し、それを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="7bf94-109">[Mapi32 スタブのレジストリ設定](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)を変更して、mapi の実装を使用するようにアプリケーションに指示することができるため、テストした mapi の実装を使用するようにアプリケーションを指示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7bf94-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="7bf94-110">次に、両方の方法で明示的にリンクする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="7bf94-111">レジストリからの読み取り</span><span class="sxs-lookup"><span data-stu-id="7bf94-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="7bf94-112">レジストリから MAPI 実装情報を読み取るには</span><span class="sxs-lookup"><span data-stu-id="7bf94-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="7bf94-113">メールクライアントのカスタム DLL を示すレジストリキーは、メールクライアントの`HKLM\Software\Clients\Mail`キーの下にあります。</span><span class="sxs-lookup"><span data-stu-id="7bf94-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="7bf94-114">次の表で、これらのキーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="7bf94-115">**キー**</span><span class="sxs-lookup"><span data-stu-id="7bf94-115">**Key**</span></span>|<span data-ttu-id="7bf94-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bf94-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="7bf94-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="7bf94-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="7bf94-118">簡易 MAPI または mapi 呼び出しをエクスポートする DLL を識別する Windows Installer publishcomponent カテゴリ ID (GUID)。</span><span class="sxs-lookup"><span data-stu-id="7bf94-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="7bf94-119">設定すると、このキーは**DLLPath**または**dllpathex**キーよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="7bf94-120">msiapplicationlcid</span><span class="sxs-lookup"><span data-stu-id="7bf94-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="7bf94-121">アプリケーションのロケール識別子 (LCID)。</span><span class="sxs-lookup"><span data-stu-id="7bf94-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="7bf94-122">最初の文字列値は、サブキー `HKLM\Software`とそれに続く文字列値を識別し、ロケール情報を含むこのキーの下にあるレジストリ値を識別します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="7bf94-123">msiofficelcid</span><span class="sxs-lookup"><span data-stu-id="7bf94-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="7bf94-124">Microsoft Office の lcid。</span><span class="sxs-lookup"><span data-stu-id="7bf94-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="7bf94-125">最初の文字列値は、このキーの下`HKLM\Software`にあるレジストリ値を識別するために、サブキーとそれに続く文字列値を識別します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="7bf94-126">これらのキーから情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="7bf94-127">前の手順で取得した値を[FGetComponentPath](fgetcomponentpath.md)関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="7bf94-128">**FGetComponentPath**は、MAPI スタブライブラリ Mapistub によってエクスポートされる関数です。</span><span class="sxs-lookup"><span data-stu-id="7bf94-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="7bf94-129">このメソッドは、MAPI のカスタムバージョンのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="7bf94-130">既定として設定されている MAPI の実装を読み込むには</span><span class="sxs-lookup"><span data-stu-id="7bf94-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="7bf94-131">レジストリ値`HKLM\Software\Clients\Mail::(default)`を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="7bf94-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="7bf94-132">前述の説明に従って、指定したクライアントの情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7bf94-133">既定のメールクライアントでは、拡張 MAPI が実装されていない場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7bf94-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="7bf94-134">例</span><span class="sxs-lookup"><span data-stu-id="7bf94-134">Example</span></span>

<span data-ttu-id="7bf94-135">Outlook で実装された MAPI を読み込むには、で`HKLM\Software\Clients\Mail\Microsoft Outlook`レジストリキーを検索し、 **FGetComponentPath**に渡します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="7bf94-136">**FGetComponentPath**は、Outlook の MAPI の実装のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="7bf94-137">キー **MSIComponentID**、 **msiapplicationlcid**、および**msiofficeelcid**が設定されていない場合は、 **dllpathex**レジストリ値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="7bf94-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="7bf94-138">キーが設定されている場合、 **FGetComponentPath**はクライアントの MAPI の実装のパスを示します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="7bf94-139">MAPI クライアント参照アルゴリズムの実装</span><span class="sxs-lookup"><span data-stu-id="7bf94-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="7bf94-140">次の表は、MAPI のカスタム実装のパスを検索するために使用される、mfcmapi の4つの関数を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bf94-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="7bf94-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="7bf94-141">**Function**</span></span>|<span data-ttu-id="7bf94-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bf94-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="7bf94-143">MAPI ライブラリのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="7bf94-144">MAPI メールのレジストリキーを取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="7bf94-145">Windows インストーラー識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="7bf94-146">[FGetComponentPath](fgetcomponentpath.md)を使用してコンポーネントのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="7bf94-147">mfcmapi は既定で mapi の既定の実装を読み込むため、mapi の別の実装を使用する場合は、明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf94-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="7bf94-148">これは、 **session¥ Load MAPI**ルーチンを使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="7bf94-149">これらの関数のしくみ</span><span class="sxs-lookup"><span data-stu-id="7bf94-149">How these functions work</span></span>

1. <span data-ttu-id="7bf94-150">mfcmapi は`GetMAPIPath`、クライアントパラメーターに NULL を渡すことで、既定の MAPI 実装を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="7bf94-151">`GetMAPIPath`MSIComponentID `GetMapiMsiIds` 、 **msiapplicationlcid**、 \*\*\*\* および**msiofficeelcid**の値を読み取る呼び出し。</span><span class="sxs-lookup"><span data-stu-id="7bf94-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="7bf94-152">`GetMapiMsiIds`[ `GetMailKey`呼び出し] 既定のメールクライアントのレジストリキーを開きます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="7bf94-153">`GetMapiMsiIds`で返されるレジストリハンドルを`GetMailKey`使用して、 **MSIComponentID**、 **msiapplicationlcid**、および**msiofficeelcid**の値を検索します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="7bf94-154">**MSIComponentID**、 **msiapplicationlcid**、および**msiofficeelcid**の値はに`GetMAPIPath`戻されます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="7bf94-155">`GetMAPIPath`を`GetComponentPath`渡します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="7bf94-156">`GetComponentPath`システムディレクトリから MAPI スタブライブラリ Mapi32 を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="7bf94-157">`GetComponentPath`その後、Mapi32 が**FGetComponentPath**をエクスポートすると仮定して、Mapi32 から**FGetComponentPath**関数のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="7bf94-158">Mapi32 のアドレスを取得\*\*\*\* できない場合は、 `GetComponentPath` Mapistub からアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="7bf94-159">`GetComponentPath`その後、 **FGetComponentPath**を呼び出して、MAPI の既定のバージョンのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="7bf94-160">`GetMAPIPath`次に、mapi 関数への[リンク](how-to-link-to-mapi-functions.md)に説明されているように、このパスを呼び出し元に返します。その後、mapi と明示的なリンクを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="7bf94-161">英語および英語以外のロケール用に MAPI のローカライズコピーをサポート`GetMAPIPath`するには、 **msiapplicationlcid**および**msiofficeelcid**サブキーの値を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="7bf94-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="7bf94-162">`GetMAPIPath`その後、 **FGetComponentPath**を呼び出し、最初に**msiapplicationlcid**を**szqualifier**として指定してから、 **msiofficeelcid**を**szqualifier**として指定します。</span><span class="sxs-lookup"><span data-stu-id="7bf94-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="7bf94-163">英語以外の言語をサポートするメールクライアントのレジストリキーの詳細については、「 [Setting Up the MSI keys for the MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf94-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="7bf94-164">mfcmapi が mapi を使用`GetMAPIPath`するためのパスを受信しない場合は、システムディレクトリから mapi スタブライブラリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="7bf94-165">mapi [dll への mapi 呼び出しの明示的なマッピング](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)で説明されている**MSMapiApps**レジストリ値は、mapi スタブライブラリが使用されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf94-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="7bf94-166">特定の MAPI の実装をロードしたり、既定の実装を読み込んだアプリケーションでは、 **MSMapiApps**レジストリキーを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7bf94-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7bf94-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bf94-167">See also</span></span>

- [<span data-ttu-id="7bf94-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="7bf94-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="7bf94-169">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="7bf94-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="7bf94-170">MAPI 関数へのリンク</span><span class="sxs-lookup"><span data-stu-id="7bf94-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="7bf94-171">Mapi32 スタブのレジストリ設定</span><span class="sxs-lookup"><span data-stu-id="7bf94-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="7bf94-172">MAPI DLL の MSI キーを設定する</span><span class="sxs-lookup"><span data-stu-id="7bf94-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="7bf94-173">mapi 呼び出しを mapi dll に明示的にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7bf94-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

