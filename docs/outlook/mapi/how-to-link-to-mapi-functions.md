---
title: MAPI 機能へのリンク
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346885"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="033e2-103">MAPI 機能へのリンク</span><span class="sxs-lookup"><span data-stu-id="033e2-103">Link to MAPI functions</span></span>

<span data-ttu-id="033e2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="033e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="033e2-105">リンクには、暗黙的なリンク、明示的なリンク、MAPI スタブ ライブラリを使用した新しいハイブリッド モデルの 3 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="033e2-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="033e2-106">暗黙的なリンク</span><span class="sxs-lookup"><span data-stu-id="033e2-106">Implicit linking</span></span>

<span data-ttu-id="033e2-107">従来、メッセージング アプリケーションで MAPI 関数を呼び出す場合は、常に Mapi32.lib ライブラリへのリンクが必要でした。</span><span class="sxs-lookup"><span data-stu-id="033e2-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="033e2-108">これには、MAPI スタブ ライブラリ Windows Mapi32.dll に MAPI 呼び出しをルーティングし、実行時に既定の MAPI クライアント実装に呼び出しを転送しました。</span><span class="sxs-lookup"><span data-stu-id="033e2-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="033e2-109">この呼び出しプロセスは暗黙的リンクと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="033e2-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="033e2-110">次の図の左側は、MAPI 関数呼び出しプロセスで使用される暗黙的なリンクの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="033e2-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="033e2-111">このプロセスは MAPI アプリケーションによって開始され、MAPI ライブラリ (Mapi32.lib) と Windows MAPI スタブ (Mapi32.dll) が関係し、MAPI スタブ (Msmapi32.dll) の Outlook MAPI クライアント実装によって完了します。</span><span class="sxs-lookup"><span data-stu-id="033e2-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="033e2-112">**暗黙的リンクと明示的リンクの比較。**</span><span class="sxs-lookup"><span data-stu-id="033e2-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="033e2-113">![暗黙的リンクと明示的リンクの比較](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "暗黙的リンクと明示的リンクの比較")</span><span class="sxs-lookup"><span data-stu-id="033e2-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="033e2-114">明示的なリンク</span><span class="sxs-lookup"><span data-stu-id="033e2-114">Explicit linking</span></span>

<span data-ttu-id="033e2-115">既定の MAPI クライアントは、Windows インストーラー (MSI) を使用してオンデマンド インストールをサポートしていますので、MAPI ライブラリと Windows MAPI スタブを使用する代わりに、Outlook MAPI スタブでメッセージング アプリケーションを直接開発できます。</span><span class="sxs-lookup"><span data-stu-id="033e2-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="033e2-116">前の図の右側に、MAPI 関数呼び出しプロセスの例を示します。まず、MAPI アプリケーションで Outlook MAPI スタブのパスと DLL 名を検索し (次のセクションの手順 2)、Outlook MAPI スタブに関数呼び出しを行います (次のセクションの手順 3)。</span><span class="sxs-lookup"><span data-stu-id="033e2-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="033e2-117">次の手順は、明示的なリンクを使用して MAPI 関数を呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="033e2-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="033e2-118">明示的なリンクに関するこの情報は、次のセクションで説明する MAPIStubLibrary.lib の導入により、ニーズに余計な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="033e2-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="033e2-119">暗黙的なモデルと同様に、新しいライブラリは、すべてを管理し、アプリケーションの MAPI を直接読み込Outlook明示的なリンク ロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="033e2-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="033e2-120">明示的なリンクの詳細については、「Linking Explicitly」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="033e2-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="033e2-121">MAPI ライブラリと MAPI スタブを使用せずに MAPI API 要素Windowsするには</span><span class="sxs-lookup"><span data-stu-id="033e2-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="033e2-122">プログラム ファイルで、使用している MAPI API 要素ごとに関数ポインターのグローバル リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="033e2-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="033e2-123">次の例は、この手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="033e2-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="033e2-124">既定の MAPI クライアントの MAPI DLL にリンクする MAPI 関数を初期化する関数を作成します (たとえば、Microsoft の MAPI クライアントMsmapi32.dllなどOutlook。</span><span class="sxs-lookup"><span data-stu-id="033e2-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="033e2-125">この関数では、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="033e2-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="033e2-126">適切mapi32.dllディレクトリからデータを読み込む。</span><span class="sxs-lookup"><span data-stu-id="033e2-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="033e2-127">x64 または x86 ネイティブ</span><span class="sxs-lookup"><span data-stu-id="033e2-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="033e2-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="033e2-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="033e2-129">woW モードでの x86</span><span class="sxs-lookup"><span data-stu-id="033e2-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="033e2-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="033e2-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="033e2-131">MAPI サブシステムを実装するパスと DLL 名を取得するには [、FGetComponentPath](fgetcomponentpath.md) 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="033e2-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="033e2-132">詳細については、「読み込 [む MAPI の特定のバージョンを選択する」を参照してください](how-to-choose-a-specific-version-of-mapi-to-load.md)。</span><span class="sxs-lookup"><span data-stu-id="033e2-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="033e2-133">LoadLibrary 関数を呼び出して DLL を読み込む。</span><span class="sxs-lookup"><span data-stu-id="033e2-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="033e2-134">GetProcAddress 関数を呼び出して MAPI 関数ポインター配列を初期化します。</span><span class="sxs-lookup"><span data-stu-id="033e2-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="033e2-135">次の例は、前の手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="033e2-135">The following example shows the previous steps:</span></span>
        
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

3. <span data-ttu-id="033e2-136">最後に、MAPI API 要素を呼び出す前に、メッセージング アプリケーションの手順 2 で作成した関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="033e2-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="033e2-137">アプリケーションを閉じる前に、MAPI サブシステムの初期化を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="033e2-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="033e2-138">次の例は、この手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="033e2-138">The following example shows this step:</span></span> 
    
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

## <a name="mapistublibrarylib"></a><span data-ttu-id="033e2-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="033e2-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="033e2-140">Microsoft Outlook 2010 および 64 ビット MAPI の出現は、Microsoft Outlook 2013 に拡張され、完全実装には従来の 32 ビット API を超える必要があります。</span><span class="sxs-lookup"><span data-stu-id="033e2-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="033e2-141">CodePlex Web サイトに投稿された新しいプロジェクトである MAPI スタブ ライブラリは、32 ビット MAPI アプリケーションと 64 ビット MAPI アプリケーションの両方の構築をサポートする Mapi32.lib のドロップイン置換を提供します。</span><span class="sxs-lookup"><span data-stu-id="033e2-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="033e2-142">MAPIStubLibrary.lib を使用すると、MAPI に明示的にリンクする必要がなく、ビルドした後、リンカー設定から Mapi32.lib を削除し、MAPIStubLibrary.lib に置き換える必要があります。コードをそれ以上変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="033e2-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="033e2-143">また、明示的なリンクを使用した場合に必要になる Mapi32.lib ではなく、このライブラリ ファイルに含まれる新しいエクスポートを処理するために、LoadLibrary、GetProcAddress、**および FreeLibrary** コードを記述する必要もなくします。  </span><span class="sxs-lookup"><span data-stu-id="033e2-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="033e2-144">Mapi32.lib で使用できないこのライブラリからリンクされた新しい関数には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="033e2-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="033e2-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="033e2-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="033e2-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="033e2-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="033e2-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="033e2-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="033e2-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="033e2-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="033e2-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="033e2-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="033e2-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="033e2-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="033e2-151">MAPI スタブ ライブラリを組み込む別の方法として、ソース ファイル MapiStubLibrary.cpp と StubUtils.cpp をプロジェクトに直接コピーし、Mapi32.lib へのリンクと MAPI に明示的にリンクするコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="033e2-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="033e2-152">MAPI スタブ ライブラリ ファイルにアクセスし、プロジェクトにビルドして統合する方法の詳細、およびこのライブラリを使用する場合と使用する理由など、このライブラリに関する質問については、CodePlex サイトの [MAPI](https://mapistublibrary.codeplex.com/documentation) スタブ ライブラリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="033e2-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="033e2-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="033e2-153">See also</span></span>

- [<span data-ttu-id="033e2-154">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="033e2-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="033e2-155">MAPI サブシステムのインストール</span><span class="sxs-lookup"><span data-stu-id="033e2-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="033e2-156">MAPI ヘッダー ファイルのインストール</span><span class="sxs-lookup"><span data-stu-id="033e2-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="033e2-157">読み込む MAPI の特定のバージョンを選択する</span><span class="sxs-lookup"><span data-stu-id="033e2-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="033e2-158">使用するリンク 方法の決定</span><span class="sxs-lookup"><span data-stu-id="033e2-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="033e2-159">実行可能ファイルを DLL にリンクする</span><span class="sxs-lookup"><span data-stu-id="033e2-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="033e2-160">MAPI DLL の MSI キーのセットアップ</span><span class="sxs-lookup"><span data-stu-id="033e2-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

