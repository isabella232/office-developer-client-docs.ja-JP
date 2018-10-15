---
title: Outlook プライマリ相互運用機能アセンブリ リファレンス
TOCTitle: '@NoTitle'
ms:assetid: 54bdde85-8dc9-4498-a1ac-f72eaf8f0cd3
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb652780(v=office.15)
ms:contentKeyID: 55119771
ms.date: 09/15/2015
mtps_version: v=office.15
f1_keywords:
- Outlook 2010, programming
- Outlook 2010, object model
- Outlook 2010, PIA
- Outlook code samples
- Outlook 2010, primary interop assembly
- primary interop assembly [Outlook 2010]
- PIA [Outlook 2010]
- reference [Outlook 2010], primary interop assembly
ms.openlocfilehash: cd62ea6537216a8d597b225c18472b2517842aa4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407290"
---
# <a name="outlook-primary-interop-assembly-reference"></a><span data-ttu-id="37d65-102">Outlook プライマリ相互運用機能アセンブリ リファレンス</span><span class="sxs-lookup"><span data-stu-id="37d65-102">Outlook Primary Interop Assembly reference</span></span>

<span data-ttu-id="37d65-103">Outlook 2013 プライマリ相互運用機能アセンブリ (PIA) リファレンスは、Outlook 2013 のマネージ アプリケーションを開発する際のヘルプを提供します。</span><span class="sxs-lookup"><span data-stu-id="37d65-103">The Outlook 2013 Primary Interop Assembly (PIA) reference provides help for developing managed applications for Outlook 2013.</span></span> <span data-ttu-id="37d65-104">「[Outlook 2013 開発者用リファレンス](https://docs.microsoft.com/office/vba/api/overview/outlook)」を COM 環境からマネージ環境に拡張したものであり、主に PIA の使用方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="37d65-104">The wd15short Primary Interop Assembly (PIA) Reference provides help for developing managed applications for wordnv2. It extends the [Word 2013 Developer Reference](https://docs.microsoft.com/office/vba/api/overview/outlook) from the COM environment to the managed environment and focuses on how to use the PIA.</span></span> <span data-ttu-id="37d65-105">Outlook 2013 のオブジェクト モデルに対するすべての追加内容と変更内容が記載されています。また、Outlook の一般的なタスクを実行する方法が、C\# と Visual Basic による多数のコード例で示されています。</span><span class="sxs-lookup"><span data-stu-id="37d65-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C\# and Visual Basic to show how to perform common tasks in Outlook.</span></span>

<span data-ttu-id="37d65-106">Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。</span><span class="sxs-lookup"><span data-stu-id="37d65-106">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span>

## <a name="purpose-of-the-outlook-pia-reference"></a><span data-ttu-id="37d65-107">Outlook PIA リファレンスの目的</span><span class="sxs-lookup"><span data-stu-id="37d65-107">Purpose of the Outlook PIA Reference</span></span>

<span data-ttu-id="37d65-p102">Outlook 用アドインの作成を最近開始したばかりのユーザーの場合、Outlook 2013 開発者用リファレンスに記載されている概要を最初にご覧ください。プログラミング環境、特定のメソッドへのアクセス方法、イベントへの接続方法は COM とマネージ開発では異なりますが、Outlook オブジェクト モデルの機能は COM とマネージ開発の両方で同じように動作します。このオブジェクト モデルの各種機能の使用法については Outlook 2013 開発者用リファレンスの概要を参照すると理解できます。</span><span class="sxs-lookup"><span data-stu-id="37d65-p102">If you are just beginning to write add-ins for Outlook, you should first refer to the conceptual content in the Outlook 2013 Developer Reference. Even though the programming environment and accessing certain methods and connecting to events are different in COM and in managed development, features in the Outlook object model behave the same way in both COM and managed development. You can refer to the conceptual content in the Outlook 2013 Developer Reference to understand how to use the different features of the object model.</span></span>

<span data-ttu-id="37d65-111">Outlook オブジェクト モデルの基本を理解していて、マネージ Outlook アドイン開発に向けた学習を進める場合は、「[Outlook PIA を使用するためのセットアップ](setting-up-to-use-the-outlook-pia.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d65-111">If you have a basic understanding of the Outlook object model and are learning to develop managed Outlook add-ins, see [Setting up to use the Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span></span> 

<span data-ttu-id="37d65-112">マネージ Office ソリューションの開発に Office Developer Tools for Visual Studio 2013 を使用する方法の詳細については、「[Visual Studio での Office 開発](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d65-112">For information about developing managed Office solutions by using Office Developer Tools for Visual Studio 2013, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span> 

<span data-ttu-id="37d65-113">いくつかの基本的な Outlook タスクを Visual Basic と C\# の両方でプログラムする方法の詳細については、「[Outlook ソリューション](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d65-113">For information about how to program some basic Outlook tasks in both Visual Basic and C\#, see [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span></span> 

<span data-ttu-id="37d65-114">さらに高度なコード例については、このリファレンスの「[操作方法 (Outlook 2013 PIA リファレンス)](how-do-i-outlook-2013-pia-reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d65-114">For more advanced code examples, see [How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md) in this reference.</span></span>

<span data-ttu-id="37d65-115">Outlook オブジェクト モデルについて詳しく理解していて、マネージ アプリケーションを作成したことがあるときに、初めて Outlook PIA を使用する場合は、「[Outlook PIA のインストールと参照](installing-and-referencing-the-outlook-pia.md)」と「[Outlook PIA のアーキテクチャ](architecture-of-the-outlook-pia.md)」から開始してください。</span><span class="sxs-lookup"><span data-stu-id="37d65-115">If you are already familiar with the Outlook object model, you have some experience writing managed applications, and you are using the Outlook PIA for the first time, start with [Installing and Referencing the Outlook PIA](installing-and-referencing-the-outlook-pia.md) and [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md).</span></span>

## <a name="accessing-the-outlook-pia-reference-in-design-time"></a><span data-ttu-id="37d65-116">設計時に Outlook PIA リファレンスにアクセスする</span><span class="sxs-lookup"><span data-stu-id="37d65-116">Accessing the Outlook PIA Reference in Design Time</span></span>

<span data-ttu-id="37d65-117">Office Developer Tools for Visual Studio 2013 を使用していてインターネットに接続している場合、Visual Studio 統合開発環境 (IDE) で F1 を押すと状況依存のヘルプにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="37d65-117">If you use vsto15short and you are connected to the Internet, you can access context-sensitive Help when you press F1 in the Visual Studio integrated development environment (IDE). This Help content is the Outlook 2013 PIA Reference posted on MSDN.</span></span> <span data-ttu-id="37d65-118">このヘルプ コンテンツは、Outlook 2013 PIA リファレンスです。</span><span class="sxs-lookup"><span data-stu-id="37d65-118">This Help content is the Outlook 2013 PIA reference.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37d65-119">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="37d65-119">In this section</span></span>

- [<span data-ttu-id="37d65-120">Outlook PIA リファレンスの新機能</span><span class="sxs-lookup"><span data-stu-id="37d65-120">What's New in the Outlook PIA Reference</span></span>](what-s-new-in-the-outlook-pia-reference.md)
- [<span data-ttu-id="37d65-121">Outlook PIA を使用するためのセットアップ</span><span class="sxs-lookup"><span data-stu-id="37d65-121">Setting Up to Use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="37d65-122">Outlook PIA のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="37d65-122">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="37d65-123">Outlook PIA を使用してマネージ Outlook アドインを開発する</span><span class="sxs-lookup"><span data-stu-id="37d65-123">Developing Managed Outlook Add-ins Using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="37d65-124">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="37d65-124">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
- [<span data-ttu-id="37d65-125">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="37d65-125">Class library</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?view=outlook-pia)

## <a name="see-also"></a><span data-ttu-id="37d65-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="37d65-126">See also</span></span>

- [<span data-ttu-id="37d65-127">Outlook デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="37d65-127">Outlook developer center</span></span>](../outlook-home.md)
- [<span data-ttu-id="37d65-128">COM と .NET の相互運用性</span><span class="sxs-lookup"><span data-stu-id="37d65-128">COM and .NET Interoperability</span></span>](https://www.apress.com/us/book/9781590590119)
- [<span data-ttu-id="37d65-129">Visual Studio での Office および SharePoint 開発</span><span class="sxs-lookup"><span data-stu-id="37d65-129">Office Development in Visual Studio</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)
- [<span data-ttu-id="37d65-130">マイクロソフト製品のアクセシビリティ機能</span><span class="sxs-lookup"><span data-stu-id="37d65-130">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/en-us/accessibility/)

