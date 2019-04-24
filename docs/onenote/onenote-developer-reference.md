---
title: OneNote 開発者用リファレンス
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: このリファレンスには、OneNote 2013 デスクトップ クライアント アプリケーション用のソリューションを開発するときに役立つ概念情報とプログラム関連のリファレンスが含まれています。
localization_priority: Priority
ms.openlocfilehash: d2b401a768e62c4b9712b1590bfaf499c2b022ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317053"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="5914d-103">OneNote 開発者用リファレンス</span><span class="sxs-lookup"><span data-stu-id="5914d-103">OneNote developer reference</span></span>

<span data-ttu-id="5914d-104">このリファレンスには、OneNote 2013 デスクトップ クライアント アプリケーション用のソリューションを開発するときに役立つ概念情報とプログラム関連のリファレンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5914d-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="5914d-105">OneNote 2013 アプリケーション プログラミング インターフェイス (API) に対する追加および変更の内容がすべて含まれています。また、OneNote のいくつかのタスクを実行する方法を示す C# のコード サンプルも提供されています。</span><span class="sxs-lookup"><span data-stu-id="5914d-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="5914d-106">OneNote 2013 API を使用すると、ユーザーはプログラムで OneNote のコンテンツにアクセスして編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5914d-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="5914d-107">さらに、ユーザーが OneNote ウィンドウのビューに変更を加えることもできます。</span><span class="sxs-lookup"><span data-stu-id="5914d-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="5914d-108">このドキュメントには次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5914d-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="5914d-109">[ウィンドウ インターフェイス](window-interfaces-onenote.md): **Window** インターフェイスと **Windows** インターフェイスについて説明しています。このインターフェイスを使用すると、ユーザーは OneNote のウィンドウのセットを列挙して、特定のウィンドウのプロパティを変更できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5914d-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="5914d-110">[クイック ファイリング ダイアログ ボックス インターフェイス](quick-filing-dialog-box-interfaces-onenote.md): OneNote 2013 の **[クイック ファイリング]** ダイアログ ボックスをプログラムでカスタマイズする際に使用できるインターフェイスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5914d-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="5914d-111">[アプリケーション インターフェイス](application-interface-onenote.md): OneNote 2013 の情報とコンテンツの取得、操作、および更新に役立つメソッド、プロパティ、およびイベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5914d-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="5914d-112">[列挙体](enumerations-onenote-developer-reference.md): OneNote 2013 オブジェクト モデルの列挙体について説明します。</span><span class="sxs-lookup"><span data-stu-id="5914d-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="5914d-113">[エラー コード](error-codes-onenote.md): OneNote 2013 オブジェクト モデルのエラー コードのリストを示します。</span><span class="sxs-lookup"><span data-stu-id="5914d-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="5914d-p102">このドキュメントに記載する API は、未接続のシナリオにおける OneNote Win32 デスクトップ クライアント ソリューションのみを対象としています。接続のシナリオの場合は、推奨する OneNote サービス API を使用してください。詳細については、[dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="5914d-p102">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios. For connected scenarios, use the recommended OneNote service APIs. To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5914d-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="5914d-117">See also</span></span>

- [<span data-ttu-id="5914d-118">OneNote (開発者向け)</span><span class="sxs-lookup"><span data-stu-id="5914d-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="5914d-119">[GitHub のサンプル](https://github.com/OneNoteDev/) (OneNote サービス API)</span><span class="sxs-lookup"><span data-stu-id="5914d-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="5914d-120">マイクロソフト製品のアクセシビリティ機能</span><span class="sxs-lookup"><span data-stu-id="5914d-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="5914d-121">ドキュメントの表記規則</span><span class="sxs-lookup"><span data-stu-id="5914d-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="5914d-122">OneNote 開発者用リファレンスの著作権情報</span><span class="sxs-lookup"><span data-stu-id="5914d-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

