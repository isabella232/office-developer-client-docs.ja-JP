---
title: iOS アプリケーションからの Office との統合
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office for iOS は、サード パーティ アプリケーションとの統合を可能にする拡張可能なソリューションを提供します。この記事では、アプリケーションから Office にユーザーを渡し、その後アプリケーションに戻すことによって、iOS アプリケーションから Office と統合する方法について説明します。
ms.openlocfilehash: 66106c51706a9ab1cd0e36b51340e65ccb807902
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595329"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="8b941-104">iOS アプリケーションからの Office との統合</span><span class="sxs-lookup"><span data-stu-id="8b941-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="8b941-p102">Office for iOS は、サード パーティ アプリケーションとの統合を可能にする拡張可能なソリューションを提供します。この記事では、アプリケーションから Office にユーザーを渡し、その後アプリケーションに戻すことによって、iOS アプリケーションから Office と統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8b941-p102">Office for iOS provides an extensible solution that enables integration with third-party applications. This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="8b941-p103">iOS デバイス上で Office を実行しているユーザーが、SharePoint または OneDrive に保存されているファイルを、任意のアプリケーションから開いて編集し、編集が完了したらすばやく元のアプリケーションに戻れるようにできます。そうするには、プロトコル ハンドラーを介してファイルを Office に渡し、Office で認識されるよう Office が確実に呼び出されるようにします。</span><span class="sxs-lookup"><span data-stu-id="8b941-p103">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="8b941-109">Office アプリケーションの起動時に特定の情報を渡しておけば、ユーザーが編集を完了した際、Office アプリケーションの [戻る] 矢印を使ってドキュメントを閉じて元のストレージ アプリケーションに戻るようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8b941-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="8b941-110">Office がインストールされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="8b941-110">Verify that Office has been installed</span></span>

<span data-ttu-id="8b941-p104">参照元のアプリケーションは、最初に特定の Office アプリケーションがインストールされていることを確認する必要があります。次の Office アプリケーションは、ドキュメントを表示および編集するために iOS デバイスにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="8b941-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="8b941-113">Excel</span><span class="sxs-lookup"><span data-stu-id="8b941-113">Excel</span></span>
    
- <span data-ttu-id="8b941-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="8b941-114">OneNote</span></span>
    
- <span data-ttu-id="8b941-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8b941-115">PowerPoint</span></span>
    
- <span data-ttu-id="8b941-116">Word</span><span class="sxs-lookup"><span data-stu-id="8b941-116">Word</span></span>
    
<span data-ttu-id="8b941-p105">[canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) メソッドを使用して、アプリケーションがリソースを開くことができるかどうかを確認します。このメソッドは、リソースの URL をパラメーターとして認識し、その URL を受け付けるアプリケーションを使用できない場合は **No** を返します。 **canOpenURL** が **No** を返す場合は、Office をインストールするようユーザーに要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b941-p105">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource. This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available. If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="8b941-120">Office をインストールするようユーザーに求める</span><span class="sxs-lookup"><span data-stu-id="8b941-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="8b941-p106">特定の Office アプリケーションがインストールされていない場合は、[SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) オブジェクトを使用して iTunes アプリ ストアをアプリケーション内でレンダリングし、ユーザーにインストールする Office アプリケーションを示します。次の表に、ストア キット製品ビュー コントローラー内でそれぞれの Office アプリケーションを呼び出すための iTunes 識別子を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8b941-p106">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install. The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="8b941-123">**Office アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="8b941-123">**Office application**</span></span>|<span data-ttu-id="8b941-124">**iTunes 識別子**</span><span class="sxs-lookup"><span data-stu-id="8b941-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b941-125">Excel</span><span class="sxs-lookup"><span data-stu-id="8b941-125">Excel</span></span>  <br/> |[<span data-ttu-id="8b941-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="8b941-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="8b941-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="8b941-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="8b941-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="8b941-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="8b941-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8b941-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="8b941-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="8b941-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="8b941-131">Word</span><span class="sxs-lookup"><span data-stu-id="8b941-131">Word</span></span>  <br/> |[<span data-ttu-id="8b941-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="8b941-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="8b941-133">Office を呼び出す</span><span class="sxs-lookup"><span data-stu-id="8b941-133">Invoke Office</span></span>

<span data-ttu-id="8b941-134">Office アプリケーションがインストールされている場合、参照元のアプリケーションは次の情報を渡すことで Office を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8b941-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="8b941-135">Office プロトコル</span><span class="sxs-lookup"><span data-stu-id="8b941-135">Office protocol</span></span>
    
- <span data-ttu-id="8b941-136">オープン モード</span><span class="sxs-lookup"><span data-stu-id="8b941-136">Open mode</span></span>
    
- <span data-ttu-id="8b941-137">URL</span><span class="sxs-lookup"><span data-stu-id="8b941-137">URL</span></span>
    
- <span data-ttu-id="8b941-138">Passback プロトコル</span><span class="sxs-lookup"><span data-stu-id="8b941-138">Passback protocol</span></span>
    
- <span data-ttu-id="8b941-139">ドキュメントのコンテキスト</span><span class="sxs-lookup"><span data-stu-id="8b941-139">Document context</span></span>
    
<span data-ttu-id="8b941-140">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="8b941-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="8b941-141">次の例は、編集用に Word ファイルを呼び出すための要求を示します。</span><span class="sxs-lookup"><span data-stu-id="8b941-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="8b941-142">Office プロトコル</span><span class="sxs-lookup"><span data-stu-id="8b941-142">Office protocols</span></span>

<span data-ttu-id="8b941-143">次の表に、各 Office アプリケーションのプロトコルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8b941-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="8b941-144">**アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="8b941-144">**Application**</span></span>|<span data-ttu-id="8b941-145">**プロトコル**</span><span class="sxs-lookup"><span data-stu-id="8b941-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b941-146">Excel</span><span class="sxs-lookup"><span data-stu-id="8b941-146">Excel</span></span>  <br/> |<span data-ttu-id="8b941-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="8b941-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="8b941-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="8b941-148">OneNote</span></span>  <br/> |<span data-ttu-id="8b941-149">onenote:</span><span class="sxs-lookup"><span data-stu-id="8b941-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="8b941-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8b941-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="8b941-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="8b941-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="8b941-152">Word</span><span class="sxs-lookup"><span data-stu-id="8b941-152">Word</span></span>  <br/> |<span data-ttu-id="8b941-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="8b941-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="8b941-154">オープン モード</span><span class="sxs-lookup"><span data-stu-id="8b941-154">Open mode</span></span>

<span data-ttu-id="8b941-p107">Office アプリケーションは、ファイルを表示 (ofv) モードまたは編集 (ofe) モードで直接開くことができます。既定は編集モードです。</span><span class="sxs-lookup"><span data-stu-id="8b941-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span> 
  
<span data-ttu-id="8b941-157">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="8b941-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="8b941-158">URL</span><span class="sxs-lookup"><span data-stu-id="8b941-158">URL</span></span>

<span data-ttu-id="8b941-159">URL は 3 つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="8b941-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="8b941-160">編集用 (ofe) にファイルを開くための宣言</span><span class="sxs-lookup"><span data-stu-id="8b941-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="8b941-161">URL 記述子 (|u|)</span><span class="sxs-lookup"><span data-stu-id="8b941-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="8b941-162">URL</span><span class="sxs-lookup"><span data-stu-id="8b941-162">The URL</span></span>
    
<span data-ttu-id="8b941-p108">URL は、エンコードされる必要があり、ファイルへの直接リンク (リダイレクトではない) でなければなりません。URL が Office で扱うことのできない形式か、または単純にダウンロードに失敗した場合、Office は、呼び出し元のアプリケーションにユーザーを戻すことができません。</span><span class="sxs-lookup"><span data-stu-id="8b941-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="8b941-165">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="8b941-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="8b941-166">Passback プロトコル (省略可能)</span><span class="sxs-lookup"><span data-stu-id="8b941-166">Passback protocol (optional)</span></span>

<span data-ttu-id="8b941-p109">[戻る] 矢印をクリックしたときに Office がユーザーを iOS アプリケーションに戻るようにする場合、呼び出し元のアプリケーションは、Passback プロトコル (記述子 '|p|' (コロンなし) にアプリのプロトコルを続けたものを含む) を使用する必要があります。アプリケーションが Office からの応答を適切に処理できることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b941-p109">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon). You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="8b941-169">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="8b941-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="8b941-170">ドキュメントのコンテキスト (省略可能)</span><span class="sxs-lookup"><span data-stu-id="8b941-170">Document context (optional)</span></span>

<span data-ttu-id="8b941-p110">Office はドキュメントのコンテキストを使用しませんが、Office がユーザーを戻すときに、参照元のアプリケーションが必要とする可能性があります。ドキュメントのコンテキストをアプリケーションに戻す場合は、記述子 '|c|' にコンテキストを続けて文字列として使用します。Office に文字列の長さの制限はありません。オペレーティング システムによって課される制限を超えることもできます。</span><span class="sxs-lookup"><span data-stu-id="8b941-p110">Office doesn't use the document context, but the referring application might need it when Office passes a user back. If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string. Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="8b941-174">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="8b941-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="8b941-175">参照元のアプリケーションにユーザーを返す</span><span class="sxs-lookup"><span data-stu-id="8b941-175">Return users to the referring application</span></span>

<span data-ttu-id="8b941-p111">セキュリティ上の理由から、ファイルが正常に開いた場合、Office は参照元のアプリケーションにユーザーのみを返します。ユーザーが [戻る] 矢印をクリックすると、参照元のアプリケーションに対して Office は、Passback プロトコル、オープン モード、URL、アップロード保留中の状態、およびドキュメントのコンテキストで応答します。アップロード保留中の状態は、記述子 |z| を使用し、"yes" または "no" のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="8b941-p111">For security reasons, Office only returns users to the referring application if the file opened successfully. When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context. The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="8b941-179">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="8b941-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="8b941-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b941-180">See also</span></span>
<span data-ttu-id="8b941-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="8b941-181"></span></span>

- [<span data-ttu-id="8b941-182">canOpenURL メソッド</span><span class="sxs-lookup"><span data-stu-id="8b941-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="8b941-183">UIApplication クラス</span><span class="sxs-lookup"><span data-stu-id="8b941-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="8b941-184">SKProductViewController オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8b941-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

