---
title: Windows ユニバーサル アプリからの Office との統合
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Windows ユニバーサル アプリ プラットフォームのサードパーティ アプリを Excel Mobile、PowerPoint Mobile、Word Mobile と統合できます。ユニバーサル アプリを Office アプリと統合する際には、Windows ファイル ピッカー コントラクト、expando プロパティ、キャッシュ ファイル更新プログラム コントラクト を使います。
ms.openlocfilehash: ad04ccc3ceb6e0f1d53e4aebc12cf9724ab8ab66
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388225"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a><span data-ttu-id="0f979-104">Windows ユニバーサル アプリからの Office との統合</span><span class="sxs-lookup"><span data-stu-id="0f979-104">Integrate with Office from Windows universal apps</span></span>

<span data-ttu-id="0f979-p102">Windows ユニバーサル アプリ プラットフォームのサードパーティ アプリを Excel Mobile、PowerPoint Mobile、Word Mobile と統合できます。ユニバーサル アプリを Office アプリと統合する際には、Windows [ファイル ピッカー コントラクト](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx)、[expando プロパティ](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx)、[キャッシュ ファイル更新プログラム コントラクト](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx) を使います。</span><span class="sxs-lookup"><span data-stu-id="0f979-p102">You can integrate your Windows universal app platform third-party apps with Excel Mobile, PowerPoint Mobile, and Word Mobile. Universal apps integrate with Office apps via Windows [file picker contracts](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx), [expando properties](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx), and [Cached File Updater contracts](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).</span></span>
  
<span data-ttu-id="0f979-p103">ユニバーサル アプリを Excel、PowerPoint、または Word Mobile と統合すると、ユーザーはそのアプリで提供されている Office ドキュメントを開くことができます。これは Office 内から閲覧するときにも、Windows を使用してそのアプリ内からファイルを開くときにも当てはまります。ユーザーがユニバーサル アプリにファイルを再び保存し、そのアプリからご使用のサービスにファイルをアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0f979-p103">When you integrate your universal app with Excel, PowerPoint, or Word Mobile, your users can open Office documents that your app provides, either when they browse from within Office or when they use Windows to open files from within your app. Users can also save the file back to your universal app, which uploads the file back to your service.</span></span>
  
<span data-ttu-id="0f979-109">この方法で開いたファイルは Office の最近使用したファイルの一覧に表示されるので、ユーザーは簡単に検索して再び開くことができます。</span><span class="sxs-lookup"><span data-stu-id="0f979-109">Files opened this way appear in the Recent list in Office, so your users can easily find and reopen them.</span></span>
  
<span data-ttu-id="0f979-110">この統合を行うには、ユニバーサル アプリが以下の条件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f979-110">This integration requires that your universal app:</span></span>
    
- <span data-ttu-id="0f979-111">Windows [ファイル ピッカー契約](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx)を実装します。</span><span class="sxs-lookup"><span data-stu-id="0f979-111">Implements the Windows [file picker contracts](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx).</span></span>
    
- <span data-ttu-id="0f979-112">ファイル ストア (クラウド ストレージにアクセスできるアプリなど) を表している。</span><span class="sxs-lookup"><span data-stu-id="0f979-112">Represents a file store (for example, an app that allows access to cloud storage).</span></span>
    
## <a name="expando-properties"></a><span data-ttu-id="0f979-113">Expando プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f979-113">Expando properties</span></span>

<span data-ttu-id="0f979-p104">Windows ユニバーサル アプリは、Expando プロパティを使用して、ファイルに関連付けられている追加情報を伝達できます。Windows でのこの操作の流れについては、「[StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx)」の「System.ExpandoProperties」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f979-p104">Windows universal apps can use Expando properties to communicate additional information that is associated with files. For information about how this works in Windows, see "System.ExpandoProperties" in [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx).</span></span>
  
<span data-ttu-id="0f979-p105">次の表に、ファイルを開くシナリオが有効になるように、アプリから Office に提供する必要があるプロパティを示します。この情報を提供しないと、アプリからのファイルはすべて読み取り専用として開かれます。ユーザーが編集の目的でファイルを開くことができるかどうかは、ユーザーが持つ Office ライセンスの種類と、ユーザーが開こうとしているドキュメントの種類に応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="0f979-p105">The following table describes the properties that your app has to provide to Office to enable file open scenarios. If this information is not provided, all files from your app are opened as read only. Whether users can open files for editing depends on the type of Office license they have and the type of document they're trying to open.</span></span>
  
<span data-ttu-id="0f979-119">これらのプロパティは、 **System.ExpandoProperties** プロパティ セット内で設定してください。</span><span class="sxs-lookup"><span data-stu-id="0f979-119">Set these properties in the **System.ExpandoProperties** property set.</span></span> 
  
|<span data-ttu-id="0f979-120">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="0f979-120">**Property**</span></span>|<span data-ttu-id="0f979-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f979-121">**Description**</span></span>|<span data-ttu-id="0f979-122">**型**</span><span class="sxs-lookup"><span data-stu-id="0f979-122">**Type**</span></span>|<span data-ttu-id="0f979-123">**例**</span><span class="sxs-lookup"><span data-stu-id="0f979-123">**Example**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0f979-124">**AppDisplayName**</span><span class="sxs-lookup"><span data-stu-id="0f979-124">**AppDisplayName**</span></span> <br/> |<span data-ttu-id="0f979-p106">ユーザーに対して表示するプロバイダー名。Office では、最近使用したドキュメントの一覧などの複数の場所に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f979-p106">Provider name to display to the user. Appears in multiple places in Office, such as the recent document list.</span></span>  <br/> |<span data-ttu-id="0f979-127">String</span><span class="sxs-lookup"><span data-stu-id="0f979-127">String</span></span>  <br/> |<span data-ttu-id="0f979-128">Contoso</span><span class="sxs-lookup"><span data-stu-id="0f979-128">Contoso</span></span>  <br/> |
|<span data-ttu-id="0f979-129">**MicrosoftOfficeOwnershipType**</span><span class="sxs-lookup"><span data-stu-id="0f979-129">**MicrosoftOfficeOwnershipType**</span></span> <br/> |<span data-ttu-id="0f979-p107">ライセンスの場合、ドキュメント/場所が Personal/Consumer か Work/Business かを示します。使用できる値は 1 (Personal) と 2 (Business) です。たとえば、ユーザーのファイルが Contoso Business に保存される場合は Business の値「2」を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f979-p107">For licensing, indicate whether the document/location is Personal/Consumer or Work/Business. Allowed values are 1 (personal) and 2 (business). For example, if your user's file is stored in Contoso Business, use the value "2" for business.</span></span>  <br/> |<span data-ttu-id="0f979-133">Unit32</span><span class="sxs-lookup"><span data-stu-id="0f979-133">Unit32</span></span>  <br/> | <span data-ttu-id="0f979-134">1 または 2</span><span class="sxs-lookup"><span data-stu-id="0f979-134">1 or 2</span></span>  <br/> <span data-ttu-id="0f979-135">たとえば、ユーザーのファイルが Contoso Business に保存される場合は、このファイルに Business の「2」のマークを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f979-135">For example, if your user's file is stored in Contoso Business, this file should be marked 2 for business.</span></span>  <br/> |
|<span data-ttu-id="0f979-136">**MicrosoftOfficeTermsOfUse**</span><span class="sxs-lookup"><span data-stu-id="0f979-136">**MicrosoftOfficeTermsOfUse**</span></span> <br/> |<span data-ttu-id="0f979-p108">提供した情報が利用規約どおりに正確であることを宣言する法的な文章。このテキストはユーザーに対しては表示されません。ご自分とアプリケーションのプロバイダーと Microsoft の間の同意になります。</span><span class="sxs-lookup"><span data-stu-id="0f979-p108">Legal text to declare that the information you provide is accurate per our terms of use. This text is not displayed to the user. It is an agreement between you, the application provider, and Microsoft.</span></span>  <br/> <span data-ttu-id="0f979-140">例については、以下をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f979-140">See the following for an example.</span></span>  <br/> | <span data-ttu-id="0f979-141">String</span><span class="sxs-lookup"><span data-stu-id="0f979-141">String</span></span>  <br/> | <span data-ttu-id="0f979-142">[https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) にある条項に同意します。</span><span class="sxs-lookup"><span data-stu-id="0f979-142">I agree to the terms located in [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md)</span></span> <br/> |
   
<span data-ttu-id="0f979-143">次のコード例は、これらのプロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0f979-143">The following code example shows how to set these properties.</span></span>
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a><span data-ttu-id="0f979-144">キャッシュ ファイル更新プログラム コントラクト</span><span class="sxs-lookup"><span data-stu-id="0f979-144">Cached File Updater contracts</span></span>

<span data-ttu-id="0f979-p109">ユニバーサル アプリがキャッシュ ファイル更新プログラム コントラクトに参加すると、別のユニバーサル アプリ (Office など) からファイルに加えられた変更が通知されます。Windows でのこの操作の流れについては、「[CachedFileUpdater Class ](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f979-p109">If your universal app participates in Cached File Updater contracts, it will be notified of changes another universal app (such as Office) makes to the file. For information about how this works in Windows, see [CachedFileUpdater class](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).</span></span>
  
<span data-ttu-id="0f979-p110">Office は **AllowOnlyReaders** オプションを使用して、ユニバーサル アプリからファイル ピッカー コントラクトを通じて提供された読み取り/書き込みファイルを開きます。したがって、Office でファイルが開かれている間は、独自のアプリなどの別のアプリで移動、削除、名前変更、書き込みを行うことはできません。 Office はファイルを自動保存しますが、CachedFileManager.DeferUpdates を設定して、Office でドキュメントが閉じられるか Windows によって Office が中断される (ユーザーが別のアプリに切り替えた時点) までアプリがアクティブにならないようにします。Office がファイルを閉じると、アプリでこれに書き込みができるようになります。</span><span class="sxs-lookup"><span data-stu-id="0f979-p110">Office uses the **AllowOnlyReaders** option to open the read-write files your universal app provides via the file picker contracts. This means the file cannot be moved, deleted, renamed, or written to by another app, including your own, while it is open in Office. Office will autosave the file, but sets CachedFileManager.DeferUpdates to prevent activating your app until Office closes the document, or Office is suspended by Windows (when the user switches to another app). When Office closes the file, your app can write to it.</span></span> 
  
<span data-ttu-id="0f979-151">ダウンロード、更新、アップロードを含む、サービスとのすべての通信をアプリで処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f979-151">Your app must handle all communication with your service, including download, refresh, and upload.</span></span>
  
<span data-ttu-id="0f979-152">次の表に、アプリと Office の間の相互作用を処理する場合に設定するパラメーターの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="0f979-152">The following tables lists the parameters to set to handle interactions between your app and Office.</span></span>
  
|<span data-ttu-id="0f979-153">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0f979-153">**Parameter**</span></span>|<span data-ttu-id="0f979-154">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f979-154">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f979-155">ReadActivationMode</span><span class="sxs-lookup"><span data-stu-id="0f979-155">ReadActivationMode</span></span>](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |<span data-ttu-id="0f979-156">ファイルを Office に送信する前にアプリで更新できるようにするには、 **BeforeAccess** を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f979-156">Set **BeforeAccess** to allow your app to update the file before it sends it to Office.</span></span>  <br/> |
|[<span data-ttu-id="0f979-157">WriteActivationMode</span><span class="sxs-lookup"><span data-stu-id="0f979-157">WriteActivationMode</span></span>](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |<span data-ttu-id="0f979-p111">ファイルを読み取り専用にするには、 **ReadOnly** を設定します。Office でのファイルの処理が終わったら CacheFileUpdater によってアプリが起動されるようにするには、 **AfterWrite** を設定します。  </span><span class="sxs-lookup"><span data-stu-id="0f979-p111">Set **ReadOnly** to make the file read only. Set **AfterWrite** to ensure that your app will be triggered by the CacheFileUpdater when Office is finished with the file.</span></span><br/><br/><span data-ttu-id="0f979-160">**注**: **AfterWrite** を設定しないと、変更をアップロードするようにアプリに通知されません。つまり、ユーザーの変更はローカルのみになります。</span><span class="sxs-lookup"><span data-stu-id="0f979-160">**NOTE**: If you do not set **AfterWrite**, your app will not be notified to upload the changes, which means that the user's changes will only be local.</span></span>           |
|[<span data-ttu-id="0f979-161">CachedFileOptions.RequireUpdateOnAccess</span><span class="sxs-lookup"><span data-stu-id="0f979-161">CachedFileOptions.RequireUpdateOnAccess</span></span>](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |<span data-ttu-id="0f979-162">最近使用したファイルの一覧からユーザーがファイルにアクセスする際に、アプリがファイルを更新できるようにするには、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f979-162">Set this property to ensure that your app can update the file when a user accesses it from the Recent list.</span></span>  <br/> |
   
## <a name="invoking-office-from-your-app"></a><span data-ttu-id="0f979-163">アプリからの Office の呼び出し</span><span class="sxs-lookup"><span data-stu-id="0f979-163">Invoking Office from your app</span></span>

<span data-ttu-id="0f979-p112">ユーザーがアプリから Office ドキュメントを開く際には、Excel Mobile、PowerPoint Mobile、Word Mobile でそのドキュメントを開くことができます。たとえば、ユーザーがアプリで \*.docx ファイルを選択すると、Word Mobile が起動して \*.docx ファイルが開き ます。どの Office アプリで開くかは、ユーザーがどのアプリをそのファイルの種類に関連付けているかに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="0f979-p112">When a user opens an Office document from your app, the document can open in Excel Mobile, PowerPoint Mobile, and Word Mobile. For example, when a user selects a \*.docx file in your app, Word Mobile launches with the \*.docx file opened. The Office app that opens is based on which app the user associated with the file type.</span></span>
  
<span data-ttu-id="0f979-p113">Office でアプリからのファイルを開くには、 **LaunchFileAsync()** を使用してファイルを起動することをお勧めします。 **LaunchUriAsync()** を使用してファイルを起動することはお勧めしません。Office ではなく、URI スキーマ用に登録されたアプリケーション (ブラウザー) が起動するからです。 **LaunchUriAsync()** に **LauncherOptions.ContentType()** オプションを指定して Office を呼び出すこともできますが、この場合は、開かれるファイルに一時ファイルのマークが付けられ、Office で読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="0f979-p113">To open a file from your app in Office, we recommend that you use **LaunchFileAsync()** to launch the file. We don't recommend that you use **LaunchUriAsync()** to launch the file because that will cause the application registered for the URI scheme to launch (the browser) instead of Office. Although **LaunchUriAsync()** with the **LauncherOptions.ContentType()** option can invoke Office, in this case the file opened is marked as temporary and is read-only in Office.</span></span> 
  
<span data-ttu-id="0f979-170">詳細については、「[Launcher クラス](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f979-170">For more information, see [Launcher class](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx).</span></span>
  
## <a name="temporary-and-read-only-files"></a><span data-ttu-id="0f979-171">一時ファイルと読み取り専用ファイル</span><span class="sxs-lookup"><span data-stu-id="0f979-171">Temporary and read-only files</span></span>

<span data-ttu-id="0f979-172">アプリ内で、一時ファイルに対して **FILE_ATTRIBUTE_TEMPORARY** 属性を設定し、読み取り専用ファイルに対して **FILE_ATTRIBUTE_READONLY** 属性を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f979-172">Set the **FILE_ATTRIBUTE_TEMPORARY** attribute on temporary files and the **FILE_ATTRIBUTE_READONLY** attribute on read-only files in your app.</span></span> 
  
<span data-ttu-id="0f979-p114">**FILE_ATTRIBUTE_TEMPORARY** 属性や **FILE_ATTRIBUTE_READONLY** 属性が設定されたファイルは、Office で読み取り専用として開かれます。また **FILE_ATTRIBUTE_TEMPORARY** は、最近使用したファイルの一覧にファイルが表示されないようにします。</span><span class="sxs-lookup"><span data-stu-id="0f979-p114">Files that have the **FILE_ATTRIBUTE_TEMPORARY** or **FILE_ATTRIBUTE_READONLY** attributes set open as read-only in Office. The **FILE_ATTRIBUTE_TEMPORARY** also prevents the file from appearing in the Recent list.</span></span> 
  
<span data-ttu-id="0f979-175">ファイル属性の詳細については、「[SetFileAttributes 関数](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f979-175">For more information about file attributes, see [SetFileAttributes function](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx).</span></span>
  
## <a name="other-best-practices"></a><span data-ttu-id="0f979-176">その他のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="0f979-176">Other best practices</span></span>

<span data-ttu-id="0f979-177">競合する編集やエラーが発生した場合などにファイルの整合性を最適化するには、以下のベスト プラクティスを適用します。</span><span class="sxs-lookup"><span data-stu-id="0f979-177">To optimize for file consistency, for example when conflicting edits or errors occur, apply the following best practices:</span></span>
  
- <span data-ttu-id="0f979-178">保存が競合しないようにします。</span><span class="sxs-lookup"><span data-stu-id="0f979-178">Prevent save conflicts.</span></span>
    
  - <span data-ttu-id="0f979-p115">サーバーの競合が発生した場合は、アップロードを一時停止して分岐しないようにします (分岐は、Office で開いている書き込みファイルがなくなった場合にのみ発生します)。通常、Office でアプリからのファイルを開くと、Office が閉じるか Windows によって中断される場合のみアプリがアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="0f979-p115">Pause uploads when server conflicts occur to avoid forking (only fork when Office no longer has a write file open). Typically, if a file from your app is open in Office, your app is activated only when Office closes or is suspended by Windows.</span></span>
    
  - <span data-ttu-id="0f979-181">競合の処理に UI が必要な場合は、トースト通知を実装します。</span><span class="sxs-lookup"><span data-stu-id="0f979-181">If you need UI to handle conflicts, implement toast notifications.</span></span> <span data-ttu-id="0f979-182">Office が中断されている場合、完全な UI は使用できません。</span><span class="sxs-lookup"><span data-stu-id="0f979-182">Full UI is not available when Office is suspended.</span></span>
    
- <span data-ttu-id="0f979-183">エラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="0f979-183">Handle errors.</span></span>
    
  - <span data-ttu-id="0f979-184">ロックが解除されると、ユーザーに競合が通知され、アプリ内でそれを解決するためのパスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0f979-184">When a lock is released, notify users of the conflict and provide a path to resolve it within your app.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f979-185">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f979-185">See also</span></span>

- [<span data-ttu-id="0f979-186">Office との統合</span><span class="sxs-lookup"><span data-stu-id="0f979-186">Integrate with Office</span></span>](integrate-with-office.md)   
- [<span data-ttu-id="0f979-187">Win32 同期クライアントからの Office との統合</span><span class="sxs-lookup"><span data-stu-id="0f979-187">Integrate with Office from Win32 sync clients</span></span>](integrate-with-office-from-win32-sync-clients.md)
    

