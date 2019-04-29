---
title: iOS ドキュメント ピッカーのための Office for iOS のサポート
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: ドキュメント プロバイダー拡張機能を使用して Office for iOS を iOS ドキュメント ピッカーと統合することにより、別のドキュメント プロバイダーによって保存されたファイルを Office で開けるようになります。
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410666"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="79a18-103">iOS ドキュメント ピッカーのための Office for iOS のサポート</span><span class="sxs-lookup"><span data-stu-id="79a18-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="79a18-104">ドキュメント プロバイダー拡張機能を使用して Office for iOS を iOS ドキュメント ピッカーと統合することにより、別のドキュメント プロバイダーによって保存されたファイルを Office で開けるようになります。</span><span class="sxs-lookup"><span data-stu-id="79a18-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="79a18-p101">iOS 8.0 以降の Apple iOS のバージョンには、[アプリ拡張サポート](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)が含まれています。これらの拡張機能を使用して、アプリケーションの機能をユーザーのデバイス上の他のアプリまたはコンテキストに拡張できます。Office for iOS を iOS ドキュメント ピッカーと統合するには、[ドキュメント プロバイダー拡張機能](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)を使用します。</span><span class="sxs-lookup"><span data-stu-id="79a18-p101">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device. To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="79a18-108">ドキュメント プロバイダー拡張機能は次の 4 つの操作をサポートします。</span><span class="sxs-lookup"><span data-stu-id="79a18-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="79a18-109">インポート</span><span class="sxs-lookup"><span data-stu-id="79a18-109">Import</span></span>
    
- <span data-ttu-id="79a18-110">エクスポート</span><span class="sxs-lookup"><span data-stu-id="79a18-110">Export</span></span>
    
- <span data-ttu-id="79a18-111">開く</span><span class="sxs-lookup"><span data-stu-id="79a18-111">Open</span></span>
    
- <span data-ttu-id="79a18-112">移動</span><span class="sxs-lookup"><span data-stu-id="79a18-112">Move</span></span>
    
<span data-ttu-id="79a18-p102">Office for iOS は、開く操作と統合されます。ドキュメント プロバイダー拡張機能を作成すると、ユーザーはファイルのコピーを作成することなく、ドキュメント ピッカーを使用して Office で直接ドキュメントを開いたり編集したりできます。</span><span class="sxs-lookup"><span data-stu-id="79a18-p102">Office for iOS integrates with the open operation. When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="79a18-115">アプリの拡張機能とドキュメント ピッカーの詳細</span><span class="sxs-lookup"><span data-stu-id="79a18-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="79a18-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="79a18-116"></span></span>

- [<span data-ttu-id="79a18-117">アプリの拡張機能</span><span class="sxs-lookup"><span data-stu-id="79a18-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="79a18-118">ドキュメント ピッカーのプログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="79a18-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="79a18-119">ドキュメント プロバイダー プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="79a18-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

