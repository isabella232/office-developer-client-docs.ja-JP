---
title: Office for Android による Android Storage Access Framework のサポート
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office for Android は Android Storage Access Framework と統合され、他のドキュメント プロバイダーが保存したファイルを Office で開けるようにします。
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799271"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="c7606-103">Office for Android による Android Storage Access Framework のサポート</span><span class="sxs-lookup"><span data-stu-id="c7606-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="c7606-104">Office for Android は Android Storage Access Framework と統合され、他のドキュメント プロバイダーが保存したファイルを Office で開けるようにします。</span><span class="sxs-lookup"><span data-stu-id="c7606-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="c7606-p101">Android 4.4 (API レベル 19) に Storage Access Framework (SAF) が導入されました。SAF を使用することにより、ユーザーはすべての推奨されるドキュメント ストレージ プロバイダー間でドキュメント、イメージ、および他のファイルを参照し、開くことができます。標準の UI によって、ユーザーはアプリおよびプロバイダーの間で一貫した方法で、ファイルの参照およびアクセスができます。</span><span class="sxs-lookup"><span data-stu-id="c7606-p101">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF). The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers. A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="c7606-108">ドキュメント プロバイダーを実装する</span><span class="sxs-lookup"><span data-stu-id="c7606-108">Implement a document provider</span></span>

<span data-ttu-id="c7606-p102">ドキュメントのストレージ サービスを提供するアプリを開発している場合、[カスタム ドキュメント プロバイダーを記述する](https://developer.android.com/guide/topics/providers/document-provider.html)ことによって、SAF を通じてファイルを利用できるようにします。その後、Office アプリは [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) および [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) インテントを呼び出して、ドキュメント プロバイダーによって返されたファイルを受信できます。インテントには、条件をさらに絞り込むためのフィルターが含まれる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c7606-p102">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html). Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider. Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="c7606-112">コンシューマーによる無料の編集の有効化</span><span class="sxs-lookup"><span data-stu-id="c7606-112">Enable free consumer edits</span></span>

<span data-ttu-id="c7606-p103">ユーザーは、無料の Microsoft アカウントを使用して Office アプリにサインインし、コンシューマー対象のストレージ サービスに保存されているドキュメントを作成または編集できます。次の表は、Storage Access Framework を通してアクセスされるドキュメントに対するコンシューマーによる無料の編集を有効にするために、プロバイダーがカーソルの一部として提供する必要のある必須プロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="c7606-p103">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service. The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="c7606-115">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="c7606-115">**Property**</span></span>|<span data-ttu-id="c7606-116">**インデックス**</span><span class="sxs-lookup"><span data-stu-id="c7606-116">**Index**</span></span>|<span data-ttu-id="c7606-117">**値**</span><span class="sxs-lookup"><span data-stu-id="c7606-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7606-118">ドキュメントの種類</span><span class="sxs-lookup"><span data-stu-id="c7606-118">Document Type</span></span>  <br/> |<span data-ttu-id="c7606-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="c7606-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="c7606-120">\<consumer\></span><span class="sxs-lookup"><span data-stu-id="c7606-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="c7606-121">サービスのフレンドリ名</span><span class="sxs-lookup"><span data-stu-id="c7606-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="c7606-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="c7606-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="c7606-p104">Office アプリ内の最近使用した一覧にあるドキュメントを特定するのに使用される、サービスのわかりやすい任意の名前。サービスのフレンドり名が表示される前に "使用条件契約" プロパティを指定する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c7606-p104">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps. Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="c7606-125">使用条件契約</span><span class="sxs-lookup"><span data-stu-id="c7606-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="c7606-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="c7606-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="c7606-127">\<ある条項に同意します。http://go.microsoft.com/fwlink/p/?LinkId=528381\></span><span class="sxs-lookup"><span data-stu-id="c7606-127">\<I agree to the terms located at http://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7606-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7606-128">See also</span></span>
<span data-ttu-id="c7606-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c7606-129"></span></span>

- [<span data-ttu-id="c7606-130">Office との統合</span><span class="sxs-lookup"><span data-stu-id="c7606-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="c7606-131">コンテンツ プロバイダーの基本</span><span class="sxs-lookup"><span data-stu-id="c7606-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="c7606-132">コンテンツ プロバイダーの作成</span><span class="sxs-lookup"><span data-stu-id="c7606-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="c7606-133">Storage Access Framework の開発者ガイド</span><span class="sxs-lookup"><span data-stu-id="c7606-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    

