---
title: Android アプリケーションからの Office との統合
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office for Android は、サード パーティのアプリケーションとの統合を可能にする、拡張可能なソリューションを提供します。Android アプリケーションから Office にユーザーを渡すことにより、そのアプリケーションから Office と統合できます。
ms.openlocfilehash: 2fd60c7e86d3390bc5343f3e09fb2235f97e0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799230"
---
# <a name="integrate-with-office-from-android-applications"></a><span data-ttu-id="4094f-104">Android アプリケーションからの Office との統合</span><span class="sxs-lookup"><span data-stu-id="4094f-104">Integrate with Office from Android applications</span></span>

<span data-ttu-id="4094f-p102">Office for Android は、サード パーティのアプリケーションとの統合を可能にする、拡張可能なソリューションを提供します。Android アプリケーションから Office にユーザーを渡すことにより、そのアプリケーションから Office と統合できます。</span><span class="sxs-lookup"><span data-stu-id="4094f-p102">Office for Android provides an extensible solution that enables integration with third-party applications. You can integrate with Office from your Android application by passing users from your application to Office.</span></span>
  
<span data-ttu-id="4094f-p103">Android デバイスで Office を実行しているユーザーが、SharePoint または OneDrive に保管されたファイルを、任意のアプリケーションから開いて編集できるようにすることができます。そのためには、プロトコル ハンドラーを通してファイルを Office に渡し、Office が理解できる方法で Office を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4094f-p103">You can enable users who are running Office on an Android device to open and edit files stored in SharePoint or OneDrive from any application. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="4094f-109">ユーザーは、ファイルの編集が終わったら、デバイスの戻るキーを選択して、元のストレージ アプリケーションに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="4094f-109">When a user is done editing a file, they can choose the back key on the device to return to the original storage application.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="4094f-110">Office がインストールされていることの確認</span><span class="sxs-lookup"><span data-stu-id="4094f-110">Verify that Office has been installed</span></span>

<span data-ttu-id="4094f-p104">特定の Office アプリケーションがインストールされていることを、まず参照元のアプリケーションが確認します。文書の表示と編集用に以下の Office アプリケーションを Android デバイスにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="4094f-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on Android devices for document viewing and editing:</span></span> 
  
- <span data-ttu-id="4094f-113">Excel</span><span class="sxs-lookup"><span data-stu-id="4094f-113">Excel</span></span>
    
- <span data-ttu-id="4094f-114">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4094f-114">PowerPoint</span></span>
    
- <span data-ttu-id="4094f-115">Word</span><span class="sxs-lookup"><span data-stu-id="4094f-115">Word</span></span>
    
<span data-ttu-id="4094f-p105">特定の Office アプリケーションがインストールされているかどうかを判別するには、Android PackageManager を使用します。この処理で使用できる Office アプリケーションのパッケージ名を以下の表に一覧で示します。</span><span class="sxs-lookup"><span data-stu-id="4094f-p105">Use Android PackageManager to determine whether a particular Office application is installed on the device. The following table lists the package names for the Office applications that you can use in this process.</span></span>
  
|<span data-ttu-id="4094f-118">**アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="4094f-118">**Application**</span></span>|<span data-ttu-id="4094f-119">**パッケージ名**</span><span class="sxs-lookup"><span data-stu-id="4094f-119">**Package name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4094f-120">Excel</span><span class="sxs-lookup"><span data-stu-id="4094f-120">Excel</span></span>  <br/> |<span data-ttu-id="4094f-121">com.microsoft.office.excel</span><span class="sxs-lookup"><span data-stu-id="4094f-121">com.microsoft.office.excel</span></span>  <br/> |
|<span data-ttu-id="4094f-122">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4094f-122">PowerPoint</span></span>  <br/> |<span data-ttu-id="4094f-123">com.microsoft.office.powerpoint</span><span class="sxs-lookup"><span data-stu-id="4094f-123">com.microsoft.office.powerpoint</span></span>  <br/> |
|<span data-ttu-id="4094f-124">Word</span><span class="sxs-lookup"><span data-stu-id="4094f-124">Word</span></span>  <br/> |<span data-ttu-id="4094f-125">com.microsoft.office.word</span><span class="sxs-lookup"><span data-stu-id="4094f-125">com.microsoft.office.word</span></span>  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="4094f-126">Office をインストールするようユーザーにプロンプトを出す</span><span class="sxs-lookup"><span data-stu-id="4094f-126">Prompt the user to install Office</span></span>

<span data-ttu-id="4094f-p106">特定の Office アプリケーションがインストールされていない場合、アプリケーションをインストールするようユーザーにプロンプトを出すことができます。以下の表に、Office アプリケーションの使用可能なインストール場所の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="4094f-p106">If a particular Office application is not installed, you can prompt the user to install the application. The following table lists the available install locations for Office applications.</span></span>
  
|<span data-ttu-id="4094f-129">**アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="4094f-129">**Application**</span></span>|<span data-ttu-id="4094f-130">**Google Play ストア**</span><span class="sxs-lookup"><span data-stu-id="4094f-130">**Google Play Store**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4094f-131">Excel</span><span class="sxs-lookup"><span data-stu-id="4094f-131">Excel</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|<span data-ttu-id="4094f-132">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4094f-132">PowerPoint</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|<span data-ttu-id="4094f-133">Word</span><span class="sxs-lookup"><span data-stu-id="4094f-133">Word</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="4094f-134">Office を呼び出す</span><span class="sxs-lookup"><span data-stu-id="4094f-134">Invoke Office</span></span>

<span data-ttu-id="4094f-135">Office アプリケーションがインストールされている場合、参照元のアプリケーションは次の情報を渡すことで Office を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4094f-135">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span>
  
- <span data-ttu-id="4094f-136">Office プロトコル</span><span class="sxs-lookup"><span data-stu-id="4094f-136">Office protocol</span></span>
    
- <span data-ttu-id="4094f-137">オープン モード</span><span class="sxs-lookup"><span data-stu-id="4094f-137">Open mode</span></span>
    
- <span data-ttu-id="4094f-138">URL</span><span class="sxs-lookup"><span data-stu-id="4094f-138">URL</span></span>
    
<span data-ttu-id="4094f-139">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="4094f-139">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>`
  
<span data-ttu-id="4094f-140">Word ファイルを編集用に呼び出す要求の例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="4094f-140">The following example shows a request to invoke a Word file for editing.</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a><span data-ttu-id="4094f-141">Office プロトコル</span><span class="sxs-lookup"><span data-stu-id="4094f-141">Office protocols</span></span>

<span data-ttu-id="4094f-142">次の表に、各 Office アプリケーションのプロトコルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4094f-142">The following table lists the protocols for each Office application.</span></span>
  
|<span data-ttu-id="4094f-143">**アプリケーション**</span><span class="sxs-lookup"><span data-stu-id="4094f-143">**Application**</span></span>|<span data-ttu-id="4094f-144">**プロトコル**</span><span class="sxs-lookup"><span data-stu-id="4094f-144">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4094f-145">Excel</span><span class="sxs-lookup"><span data-stu-id="4094f-145">Excel</span></span>  <br/> |<span data-ttu-id="4094f-146">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="4094f-146">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="4094f-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4094f-147">PowerPoint</span></span>  <br/> |<span data-ttu-id="4094f-148">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="4094f-148">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="4094f-149">Word</span><span class="sxs-lookup"><span data-stu-id="4094f-149">Word</span></span>  <br/> |<span data-ttu-id="4094f-150">ms-word:</span><span class="sxs-lookup"><span data-stu-id="4094f-150">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="4094f-151">オープン モード</span><span class="sxs-lookup"><span data-stu-id="4094f-151">Open mode</span></span>

<span data-ttu-id="4094f-p107">Office アプリケーションは、ファイルを表示 (ofv) モードまたは編集 (ofe) モードで直接開くことができます。既定は編集モードです。</span><span class="sxs-lookup"><span data-stu-id="4094f-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span>
  
<span data-ttu-id="4094f-154">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="4094f-154">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="4094f-155">URL</span><span class="sxs-lookup"><span data-stu-id="4094f-155">URL</span></span>

<span data-ttu-id="4094f-156">URL は 3 つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="4094f-156">The URL includes three parts:</span></span>
  
- <span data-ttu-id="4094f-157">編集用 (ofe) にファイルを開くための宣言</span><span class="sxs-lookup"><span data-stu-id="4094f-157">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="4094f-158">URL 記述子 (|u|)</span><span class="sxs-lookup"><span data-stu-id="4094f-158">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="4094f-159">URL</span><span class="sxs-lookup"><span data-stu-id="4094f-159">The URL</span></span>
    
<span data-ttu-id="4094f-p108">URL は、エンコードされる必要があり、ファイルへの直接リンク (リダイレクトではない) でなければなりません。URL が Office で扱うことのできない形式か、または単純にダウンロードに失敗した場合、Office は、呼び出し元のアプリケーションにユーザーを戻すことができません。</span><span class="sxs-lookup"><span data-stu-id="4094f-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span>
  
<span data-ttu-id="4094f-162">スキーマ形式:</span><span class="sxs-lookup"><span data-stu-id="4094f-162">Schema format:</span></span>
  
 `|u|<document URL>`
  
## <a name="see-also"></a><span data-ttu-id="4094f-163">関連項目</span><span class="sxs-lookup"><span data-stu-id="4094f-163">See also</span></span>
<span data-ttu-id="4094f-164"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="4094f-164"></span></span>

- [<span data-ttu-id="4094f-165">Office との統合</span><span class="sxs-lookup"><span data-stu-id="4094f-165">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="4094f-166">PackageManager</span><span class="sxs-lookup"><span data-stu-id="4094f-166">PackageManager</span></span>](http://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [<span data-ttu-id="4094f-167">GetPackageManager()</span><span class="sxs-lookup"><span data-stu-id="4094f-167">GetPackageManager()</span></span>](http://developer.android.com/reference/android/content/Context.html)
    

