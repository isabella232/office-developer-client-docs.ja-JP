---
title: ロードするのには MAPI の特定のバージョンを選択します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800213"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="931ec-103">ロードするのには MAPI の特定のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="931ec-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="931ec-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="931ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="931ec-105">MAPI の実装を明示的にリンクする場合、ロードする実装を慎重に選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="931ec-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="931ec-106">MAPI の実装を明示的にリンクする 2 つの方法もあります。</span><span class="sxs-lookup"><span data-stu-id="931ec-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="931ec-107">MAPI スタブ ライブラリをロードし、カスタム DLL をロードし、MAPI をディスパッチする呼び出しを行って、レジストリで指定できます。</span><span class="sxs-lookup"><span data-stu-id="931ec-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="931ec-108">既定のメール クライアントで使用されている MAPI のバージョンを検索するのには、MAPI クライアントの検索アルゴリズムを実装し、それをロードできます。</span><span class="sxs-lookup"><span data-stu-id="931ec-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="931ec-109">MAPI の実装を使用するようにアプリケーションに指示する[Mapi32.dll スタブのレジストリ設定](http://msdn.microsoft.com/ja-jp/library/ms531218%28EXCHG.10%29.aspx)を変更することができます、ため、アプリケーションをテストしている MAPI の実装を使用するを指示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="931ec-109">Because you can change the [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/ja-jp/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="931ec-110">明示的なリンクの両方の方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="931ec-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="931ec-111">レジストリからの読み取り</span><span class="sxs-lookup"><span data-stu-id="931ec-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="931ec-112">MAPI 実装に関する情報をレジストリから読み取れません</span><span class="sxs-lookup"><span data-stu-id="931ec-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="931ec-113">メール クライアントのカスタム DLL を指定するレジストリ キーが下にある、`HKLM\Software\Clients\Mail`メール クライアントのキーです。</span><span class="sxs-lookup"><span data-stu-id="931ec-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="931ec-114">次の表では、これらのキーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="931ec-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="931ec-115">**キー**</span><span class="sxs-lookup"><span data-stu-id="931ec-115">**Key**</span></span>|<span data-ttu-id="931ec-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="931ec-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="931ec-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="931ec-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="931ec-118">Windows インストーラー PublishComponent カテゴリ ID (GUID) シンプル MAPI、または MAPI をエクスポートする DLL を識別するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="931ec-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="931ec-119">場合はセットでは、このキーは、 **DLLPath**または**DLLPathEx**キーよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="931ec-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="931ec-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="931ec-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="931ec-121">アプリケーションのロケール識別子 (LCID) です。</span><span class="sxs-lookup"><span data-stu-id="931ec-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="931ec-122">最初の文字列から下位のキーを識別する値`HKLM\Software`し、後続の文字列の値がこのキーの下のロケール情報が含まれているレジストリ値を識別します。</span><span class="sxs-lookup"><span data-stu-id="931ec-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="931ec-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="931ec-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="931ec-124">Microsoft Office の Lcid です。</span><span class="sxs-lookup"><span data-stu-id="931ec-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="931ec-125">最初の文字列から下位のキーを識別する値`HKLM\Software`し、後続の文字列の値がこのキーの下にあるレジストリの値を識別します。</span><span class="sxs-lookup"><span data-stu-id="931ec-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="931ec-126">これらのキーから情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="931ec-127">[FGetComponentPath](fgetcomponentpath.md)関数に前の手順から取得した値を渡します。</span><span class="sxs-lookup"><span data-stu-id="931ec-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="931ec-128">Mapistub.dll MAPI スタブ ライブラリによってエクスポートされる関数は、 **FGetComponentPath**です。</span><span class="sxs-lookup"><span data-stu-id="931ec-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="931ec-129">カスタム MAPI のバージョンのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="931ec-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="931ec-130">既定としてマークされている MAPI の実装をロードするには</span><span class="sxs-lookup"><span data-stu-id="931ec-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="931ec-131">読み取り、`HKLM\Software\Clients\Mail::(default)`のレジストリ値です。</span><span class="sxs-lookup"><span data-stu-id="931ec-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="931ec-132">前述したように、指定されたクライアントの情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="931ec-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="931ec-133">既定のメール クライアントが MAPI の拡張を実装可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="931ec-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="931ec-134">例</span><span class="sxs-lookup"><span data-stu-id="931ec-134">Example</span></span>

<span data-ttu-id="931ec-135">下にレジストリ キーを参照して Outlook に実装された、MAPI を読み込み、 `HKLM\Software\Clients\Mail\Microsoft Outlook` **FGetComponentPath**に渡すとします。</span><span class="sxs-lookup"><span data-stu-id="931ec-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="931ec-136">**FGetComponentPath**では、Outlook の MAPI 実装へのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="931ec-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="931ec-137">**MSIComponentID**、 **MSIApplicationLCID**、および**MSIOfficeLCID**キーが設定されていない場合は、 **DLLPathEx**レジストリ値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="931ec-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="931ec-138">キーが設定されている場合**FGetComponentPath**は、mapi クライアントの実装のパスを示します。</span><span class="sxs-lookup"><span data-stu-id="931ec-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="931ec-139">MAPI クライアントの検索アルゴリズムを実装します。</span><span class="sxs-lookup"><span data-stu-id="931ec-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="931ec-140">MFCMAPI から MAPI のカスタム実装のパスを検索に使用される 4 つの機能を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="931ec-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="931ec-141">**関数**</span><span class="sxs-lookup"><span data-stu-id="931ec-141">**Function**</span></span>|<span data-ttu-id="931ec-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="931ec-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="931ec-143">MAPI ライブラリのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="931ec-144">MAPI メールのレジストリ キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="931ec-145">Windows インストーラーの識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="931ec-146">[FGetComponentPath](fgetcomponentpath.md)を使用してコンポーネントのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="931ec-147">MFCMAPI では、MAPI の別の実装を使用する場合、既定では、MAPI の既定の実装が読み込まれる、ために割り当てる必要が明示的にそのようにします。</span><span class="sxs-lookup"><span data-stu-id="931ec-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="931ec-148">これは、 **MAPI の Session\Load**ルーチンを使用してによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="931ec-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="931ec-149">これらの関数のしくみ</span><span class="sxs-lookup"><span data-stu-id="931ec-149">How these functions work</span></span>

1. <span data-ttu-id="931ec-150">MFCMAPI 呼び出し`GetMAPIPath`、既定の MAPI 実装をロードするのには、クライアント パラメーターの受け渡しが NULL です。</span><span class="sxs-lookup"><span data-stu-id="931ec-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="931ec-151">`GetMAPIPath`呼び出し`GetMapiMsiIds` **MSIComponentID**、 **MSIApplicationLCID**、および**MSIOfficeLCID**の値を読み取る。</span><span class="sxs-lookup"><span data-stu-id="931ec-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="931ec-152">`GetMapiMsiIds`呼び出し`GetMailKey`を既定のメール クライアントのレジストリ キーを開きます。</span><span class="sxs-lookup"><span data-stu-id="931ec-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="931ec-153">`GetMapiMsiIds`によって返されるレジストリ ハンドルを使用して`GetMailKey` **MSIComponentID**、 **MSIApplicationLCID**、および**MSIOfficeLCID**の値を検索します。</span><span class="sxs-lookup"><span data-stu-id="931ec-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="931ec-154">**MSIComponentID**、 **MSIApplicationLCID**、 **MSIOfficeLCID**の値が返されます`GetMAPIPath`。</span><span class="sxs-lookup"><span data-stu-id="931ec-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="931ec-155">`GetMAPIPath`渡されたに`GetComponentPath`。</span><span class="sxs-lookup"><span data-stu-id="931ec-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="931ec-156">`GetComponentPath`システム ディレクトリから、Mapi32.dll、MAPI スタブ ライブラリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="931ec-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="931ec-157">`GetComponentPath`Mapi32.dll、Mapi32.dll が**FGetComponentPath**をエクスポートすると仮定してから、 **FGetComponentPath**関数のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="931ec-158">Mapi32.dll が失敗した場合から**FGetComponentPath**のアドレスを取得する場合`GetComponentPath`Mapistub.dll からアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="931ec-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="931ec-159">`GetComponentPath`**FGetComponentPath**MAPI の既定のバージョンのパスを取得するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="931ec-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="931ec-160">`GetMAPIPath`呼び出し元、MAPI をロードし、明示的にリンクしている[MAPI の関数へのリンク](how-to-link-to-mapi-functions.md)で説明したようにこのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="931ec-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="931ec-161">英語と英語以外のロケールのローカライズされたコピー MAPI をサポートするために`GetMAPIPath` **MSIApplicationLCID**と**MSIOfficeLCID**のサブキーの値を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="931ec-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="931ec-162">`GetMAPIPath`**FGetComponentPath**を最初として、 **szQualifier**、 **MSIApplicationLCID**を指定して、再び**szQualifier**として**MSIOfficeLCID**を指定するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="931ec-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="931ec-163">英語以外の言語をサポートするメール クライアントのレジストリ キーの詳細については、[設定の [MSI のキーの MAPI DLL](http://msdn.microsoft.com/ja-jp/library/ee909494%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="931ec-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](http://msdn.microsoft.com/ja-jp/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="931ec-164">MFCMAPI が MAPI を使用するためのパスを受信していないかどうか`GetMAPIPath`、システム ディレクトリから MAPI スタブ ライブラリが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="931ec-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="931ec-165">[MAPI 呼び出しを明示的に MAPI Dll へのマッピング](http://msdn.microsoft.com/ja-jp/library/ee909490%28VS.85%29.aspx)で説明されている**MSMapiApps**レジストリ値は、MAPI スタブ ライブラリを使用する場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="931ec-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](http://msdn.microsoft.com/ja-jp/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="931ec-166">MAPI の特定の実装をロードまたは既定の実装をロードするアプリケーションは、 **MSMapiApps**レジストリ キーを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="931ec-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="931ec-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="931ec-167">See also</span></span>

- [<span data-ttu-id="931ec-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="931ec-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="931ec-169">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="931ec-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="931ec-170">MAPI の関数へのリンク</span><span class="sxs-lookup"><span data-stu-id="931ec-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="931ec-171">Mapi32.dll スタブのレジストリ設定</span><span class="sxs-lookup"><span data-stu-id="931ec-171">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/ja-jp/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="931ec-172">MAPI DLL の MSI のキーの設定</span><span class="sxs-lookup"><span data-stu-id="931ec-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](http://msdn.microsoft.com/ja-jp/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="931ec-173">MAPI MAPI Dll への呼び出しを明示的にマッピング</span><span class="sxs-lookup"><span data-stu-id="931ec-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](http://msdn.microsoft.com/ja-jp/library/ee909490%28VS.85%29.aspx)

