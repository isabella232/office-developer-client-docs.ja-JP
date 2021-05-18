---
title: Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f86ad294e894b4faea10d033a069638221f1bd78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285173"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a><span data-ttu-id="c60ec-102">Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する</span><span class="sxs-lookup"><span data-stu-id="c60ec-102">Using a trusted Application object provided by Office Developer Tools for Visual Studio</span></span>

<span data-ttu-id="c60ec-103">Office Developer Tools for Visual Studio を使用して管理対象アドインを開発する場合は、常に、Visual Studio が提供する [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="c60ec-103">If you are developing a managed add-in by using Office Developer Tools for Visual Studio, always use the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that is provided by Visual Studio.</span></span> 

<span data-ttu-id="c60ec-104">Outlook の新しいインスタンスを自動化することを目的としていない場合は、Outlook の新しいインスタンスを作成するために New または new キーワードを使用しないでください。その理由は、この **Application** オブジェクトのインスタンスが、Outlook のオブジェクト モデル ガードの観点からは信頼されていないためです。</span><span class="sxs-lookup"><span data-stu-id="c60ec-104">Unless you intend to automate a new instance of Outlook, do not use the New or new keyword to create a new instance of Outlook, as this instance of the **Application** object is not trusted from the perspective of the Outlook Object Model Guard.</span></span> 

<span data-ttu-id="c60ec-105">アドインで **Application** オブジェクトの信頼されていないインスタンスを使用すると、クライアントが実行している Outlook のバージョンによっては、そのアドインが既定でオブジェクト モデルのいくつかのメンバーで Outlook のオブジェクト モデル ガードを呼び出すようになります。</span><span class="sxs-lookup"><span data-stu-id="c60ec-105">If your add-in uses an untrusted instance of the **Application** object, depending on the version of Outlook that the client is running, the add-in by default will invoke Outlook's Object Model Guard on a number of members of the object model.</span></span> 

<span data-ttu-id="c60ec-106">オブジェクト モデル ガードの動作に関する詳細については、「[Outlook 2007 でのコード セキュリティの変更点](https://msdn.microsoft.com/library/bb226709\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c60ec-106">For more information about the behavior of the Object Model Guard, see [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span></span> <span data-ttu-id="c60ec-107">「Outlook 2007 でのコード セキュリティの変更点」の記事では既定で信頼されている COM アドインについて記述されていても、このデザインは Outlook 2007 以降の Outlook バージョンに適用されるものであり、信頼は同じ方法で管理対象アドインにも適用される点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="c60ec-107">Note that even though the "Code Security Changes in Outlook 2007" article refers to COM add-ins that are trusted by default, this design applies to versions of Outlook since Outlook 2007, and the trust applies to managed add-ins the same way.</span></span> <span data-ttu-id="c60ec-108">アドインが管理対象かどうかにかかわらず、信頼は、そのアドインが信頼された **Application** オブジェクトを使用するという前提に基づきます。</span><span class="sxs-lookup"><span data-stu-id="c60ec-108">Regardless of whether the add-in is managed or not, the trust is based on the assumption that the add-in uses a trusted **Application** object.</span></span>

