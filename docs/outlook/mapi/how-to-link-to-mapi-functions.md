---
title: MAPI の関数へのリンクします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400146"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="26555-103">MAPI の関数へのリンクします。</span><span class="sxs-lookup"><span data-stu-id="26555-103">Link to MAPI functions</span></span>

<span data-ttu-id="26555-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26555-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26555-105">リンクの 3 つの方法があります: 暗黙的なリンク、明示的なリンク、および MAPI スタブ ライブラリを使用して新しいハイブリッド モデルです。</span><span class="sxs-lookup"><span data-stu-id="26555-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="26555-106">暗黙的なリンク</span><span class="sxs-lookup"><span data-stu-id="26555-106">Implicit linking</span></span>

<span data-ttu-id="26555-107">従来、メッセージング アプリケーションでは常に MAPI の関数を呼び出すと関与 Mapi32.lib ライブラリへのリンクです。</span><span class="sxs-lookup"><span data-stu-id="26555-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="26555-108">これには、Mapi32.dll で、実行時に既定の MAPI クライアント実装への呼び出しを転送し、Windows の MAPI スタブ ライブラリにルーティングの MAPI 呼び出しが含まれています。</span><span class="sxs-lookup"><span data-stu-id="26555-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="26555-109">この呼び出しプロセスは、暗黙的なリンクと呼びます。</span><span class="sxs-lookup"><span data-stu-id="26555-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="26555-110">次の図の左側には、MAPI の関数の呼び出しプロセスで使用されている暗黙的なリンクの例を示します。</span><span class="sxs-lookup"><span data-stu-id="26555-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="26555-111">プロセスは、MAPI アプリケーションによって開始されますと MAPI ライブラリ (Mapi32.lib) と Windows の MAPI スタブ (Mapi32.dll) し、MAPI スタブ (Msmapi32.dll) の Outlook MAPI クライアントの実装が完了しました。</span><span class="sxs-lookup"><span data-stu-id="26555-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="26555-112">**暗黙的および明示的なリンクの比較を行います。**</span><span class="sxs-lookup"><span data-stu-id="26555-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="26555-113">![暗黙的および明示的なリンクの比較](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "暗黙的および明示的なリンクの比較")</span><span class="sxs-lookup"><span data-stu-id="26555-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="26555-114">明示的なリンク</span><span class="sxs-lookup"><span data-stu-id="26555-114">Explicit linking</span></span>

<span data-ttu-id="26555-115">既定の MAPI クライアントは、Windows インストーラー (MSI) を使用して、オンデマンド インストールをサポートするため、MAPI ライブラリを使用するのではなく Outlook MAPI スタブと Windows の MAPI スタブに直接メッセージング ・ アプリケーションを開発できます。</span><span class="sxs-lookup"><span data-stu-id="26555-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="26555-116">前の図の右側には、(手順 2 を次のセクションで)、Outlook MAPI スタブの DLL の名前とパスを検索し、関数の呼び出しに、Outlook MAPI スタブ (は、MAPI アプリケーションを最初から、MAPI の関数の呼び出しプロセスの例を示しています。手順 3 で次のセクション)。</span><span class="sxs-lookup"><span data-stu-id="26555-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="26555-117">次の手順では、明示的なリンクを使用して MAPI の関数を呼び出す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="26555-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26555-118">明示的なリンクについては、次のセクションで説明した MAPIStubLibrary.lib の導入に伴い、お客様のニーズに不要な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="26555-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="26555-119">暗黙のモデルでは、ような新しいライブラリがすべてを管理し、Outlook に必要な明示的なリンクのロジックを実装する MAPI を直接します。</span><span class="sxs-lookup"><span data-stu-id="26555-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="26555-120">明示的リンクの詳細については、明示的にリンク参照してください。</span><span class="sxs-lookup"><span data-stu-id="26555-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="26555-121">MAPI ライブラリと Windows の MAPI スタブのない MAPI API 要素を呼び出す</span><span class="sxs-lookup"><span data-stu-id="26555-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="26555-122">プログラム ファイルで使用している MAPI API 要素ごとに関数ポインターのグローバル リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="26555-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="26555-123">次の例では、この手順を示します。</span><span class="sxs-lookup"><span data-stu-id="26555-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="26555-124">既定の MAPI クライアント (たとえば、Msmapi32.dll の Microsoft Outlook の MAPI DLL にリンクするのには MAPI の関数を初期化する関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="26555-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="26555-125">この関数では、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="26555-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="26555-126">システムの適切なディレクトリから mapi32.dll をロードします。</span><span class="sxs-lookup"><span data-stu-id="26555-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="26555-127">x64 または x86 でネイティブに</span><span class="sxs-lookup"><span data-stu-id="26555-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="26555-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="26555-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="26555-129">WoW モードでの x86</span><span class="sxs-lookup"><span data-stu-id="26555-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="26555-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="26555-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="26555-131">MAPI のサブシステムを実装する DLL の名前とパスを取得する[FGetComponentPath](fgetcomponentpath.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="26555-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="26555-132">詳細については、[特定のバージョンの MAPI 負荷の選択](how-to-choose-a-specific-version-of-mapi-to-load.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="26555-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="26555-133">LoadLibrary 関数を呼び出すことによって、DLL を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="26555-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="26555-134">GetProcAddress 関数を呼び出すことによって、MAPI の関数ポインターの配列を初期化します。</span><span class="sxs-lookup"><span data-stu-id="26555-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="26555-135">次の使用例は、上記の手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="26555-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="26555-136">最後に、MAPI API 要素への呼び出しを行う前に、手順 2 では、メッセージング アプリケーションの作成の場合にこの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="26555-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="26555-137">アプリケーションを閉じる前に、MAPI サブシステムの初期化を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26555-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="26555-138">次の使用例は、この手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="26555-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="26555-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="26555-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="26555-140">Microsoft Outlook 2010 と 64 ビットの MAPI、Microsoft Outlook 2013 年に拡張するようになりましたの登場は従来の 32 ビット API の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="26555-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="26555-141">新しいプロジェクト、MAPI スタブ ライブラリでは、CodePlex の web サイトに掲載は、32 ビットと 64 ビットの両方の MAPI アプリケーションの構築をサポートする Mapi32.lib のドロップイン交換を提供します。</span><span class="sxs-lookup"><span data-stu-id="26555-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="26555-142">MAPIStubLibrary.lib で MAPI を明示的にリンクする必要があるし、ことを構築することからを削除する Mapi32.lib、リンカーの設定では、MAPIStubLibrary.lib に置き換えることコードにさらに変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="26555-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="26555-143">Mapi32.lib で、明示的なリンクを使用する場合が必要ではありませんが、このライブラリ ファイル内に含まれている最新のエクスポートを処理するために**LoadLibrary**と**GetProcAddress**を**終わった**のコードを記述する必要もなくなります。</span><span class="sxs-lookup"><span data-stu-id="26555-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="26555-144">Mapi32.lib では使用できませんが、このライブラリにリンクしている新しい機能の一部を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="26555-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="26555-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="26555-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="26555-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="26555-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="26555-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="26555-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="26555-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="26555-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="26555-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="26555-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="26555-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="26555-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="26555-151">MAPI スタブ ライブラリを組み込むことの別の方法は、プロジェクトに直接、MapiStubLibrary.cpp、StubUtils.cpp、ソース ファイルをコピーし、Mapi32.lib へのリンケージ、および MAPI に明示的にリンクする任意のコードを削除することです。</span><span class="sxs-lookup"><span data-stu-id="26555-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="26555-152">MAPI スタブ ライブラリのファイルにアクセスし、ビルドし、統合のプロジェクトと同様にこのライブラリについての質問に次のようにタイミングと理由についての情報を使用してを参照してください[MAPI スタブ ライブラリ](https://mapistublibrary.codeplex.com/documentation)CodePlex サイトです。</span><span class="sxs-lookup"><span data-stu-id="26555-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26555-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="26555-153">See also</span></span>

- [<span data-ttu-id="26555-154">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="26555-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="26555-155">MAPI サブシステムのインストール</span><span class="sxs-lookup"><span data-stu-id="26555-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="26555-156">MAPI ヘッダー ファイルをインストールする</span><span class="sxs-lookup"><span data-stu-id="26555-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="26555-157">読み込む MAPI の特定のバージョンを選択する</span><span class="sxs-lookup"><span data-stu-id="26555-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="26555-158">使用するリンク方式の使い分け</span><span class="sxs-lookup"><span data-stu-id="26555-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="26555-159">実行可能ファイルを DLL にリンクします。</span><span class="sxs-lookup"><span data-stu-id="26555-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="26555-160">MAPI DLL の MSI のキーの設定</span><span class="sxs-lookup"><span data-stu-id="26555-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

