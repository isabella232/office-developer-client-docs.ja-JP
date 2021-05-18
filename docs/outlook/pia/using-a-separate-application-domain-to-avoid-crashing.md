---
title: 異なるアプリケーション ドメインを使用してクラッシュを回避する
TOCTitle: Using a separate application domain to avoid crashing
ms:assetid: 7fc6d1e5-7032-47a9-826f-6b5d3b43fef9
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb623114(v=office.15)
ms:contentKeyID: 55119786
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2490c15da9c993a1a26b50adeb38207457f8286
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285148"
---
# <a name="using-a-separate-application-domain-to-avoid-crashing"></a><span data-ttu-id="09d38-102">異なるアプリケーション ドメインを使用してクラッシュを回避する</span><span class="sxs-lookup"><span data-stu-id="09d38-102">Using a separate application domain to avoid crashing</span></span>

<span data-ttu-id="09d38-p101">**IDTExtensibility2** インターフェイスを実装するマネージ アドインは、すべて同じ既定のアプリケーション ドメインに読み込まれます。アプリケーション ドメイン内のアドインがクラッシュすると、同じアプリケーション ドメイン内の他のアドインも動作しなくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="09d38-p101">Managed add-ins that implement the **IDTExtensibility2** interface are loaded into the same default application domain. When an add-in in the application domain crashes, it can cause other add-ins in the same application domain to fail as well.</span></span>

<span data-ttu-id="09d38-p102">この問題を回避するには、アドイン用の shim を作成し、アドインを専用のアプリケーション ドメインに読み込むことができます。shim は、C++ で作成されたアンマネージ ダイナミック リンク ライブラリです。shim を使用するときは、アドインの代わりに shim を登録します。Outlook が shim を読み込むと、shim が対応するアドインを読み込みます。アドインごとに個別に shim を作成して登録する必要があります。マネージ アドイン用の shim の作成方法については、「[Isolating Office Extensions with the COM Shim Wizard ](https://go.microsoft.com/fwlink/?linkid=89109)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09d38-p102">To work around this problem, you can create a shim for the add-in, so that the add-in can be loaded in its own application domain. A shim is an unmanaged dynamic link library written in C++. When you use a shim, you register the shim instead of the add-in. Outlook loads the shim, and the shim loads the add-in for which it was built. You must build and register a separate shim for each add-in. For more information about developing shims for managed add-ins, see [Isolating Office Extensions with the COM Shim Wizard](https://go.microsoft.com/fwlink/?linkid=89109).</span></span>

<span data-ttu-id="09d38-111">その他の方法で別のアプリケーション ドメインにアドインを読み込むには、Visual Studio 2010 以降のリリースの Office Developer Tools for Visual Studio で Office 開発ツールを使用してアドインを開発します。</span><span class="sxs-lookup"><span data-stu-id="09d38-111">Another alternative to load your add-in into a separate application domain is to develop your add-in using Office development tools in Visual Studio 2010, or a later release of Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="09d38-112">これに該当するバージョンの Office Developer Tools for Visual Studio で開発したアドインは、IDTExtensibility2 インターフェイスを実装しないで、**IStartup** インターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="09d38-112">Add-ins developed by these versions of Office Developer Tools for Visual Studio do not implement the IDTExtensibility2 interface but use the **IStartup** interface.</span></span> <span data-ttu-id="09d38-113">こうしたアドインは、Visual Studio が提供するローダー AddinLoader.dll を使用します。このローダーは、汎用の shim のように動作します。</span><span class="sxs-lookup"><span data-stu-id="09d38-113">They use a loader provided by Visual Studio, AddinLoader.dll, which acts like a generic shim.</span></span> <span data-ttu-id="09d38-114">Outlook は、Visual Studio で作成されたアドインについてレジストリを調べます。</span><span class="sxs-lookup"><span data-stu-id="09d38-114">Outlook looks in the registry for add-ins created with Visual Studio.</span></span> 

<span data-ttu-id="09d38-115">そうしたアドインを Outlook が検出すると、Outlook は AddinLoader.dll を開始します。これにより、Visual Studio Tools for Office ランタイムが開始され、アプリケーション マニフェストが Visual Studio Tools for Office ランタイムに中継されます。</span><span class="sxs-lookup"><span data-stu-id="09d38-115">If Outlook finds such add-ins, Outlook starts AddinLoader.dll, which then starts the Visual Studio Tools for Office Runtime and relays the application manifest to the Visual Studio Tools for Office Runtime.</span></span> <span data-ttu-id="09d38-116">その後、Visual Studio Tools for Office ランタイムは、該当するアドインを個別のアプリケーション ドメインに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="09d38-116">The Visual Studio Tools for Office Runtime then loads each such add-in in a separate application domain.</span></span> <span data-ttu-id="09d38-117">Visual Studio がアドインを読み込む方法の詳細については、「[VSTO アドインのアーキテクチャ](https://msdn.microsoft.com/library/bb386298\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09d38-117">For more information about how Visual Studio loads an add-in, see [Architecture of Application-Level Add-Ins](https://msdn.microsoft.com/library/bb386298\(v=office.15\)).</span></span>

