---
title: マネージ Outlook アドインの開発でのベスト プラクティス
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87573980836d63d751302b0efcec0952331b7fc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406863"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="b6eb1-102">マネージ Outlook アドインの開発でのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="b6eb1-102">Best Practices in Developing Managed Outlook Add-Ins</span></span>

<span data-ttu-id="b6eb1-p101">Outlook の相互運用機能アセンブリを使用すると Outlook と相互運用できるマネージ ソリューションを作成できますが、Outlook は .NET Framework より前から存在しており、Visual Basic for Applications (VBA) や Visual Basic などのアンマネージ言語でのプログラミングをサポートするように設計されています。ここでは、Outlook 用のマネージ アドインを開発するときに注意する必要のある最重要事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6eb1-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="b6eb1-105">オブジェクトを系統的に解放する</span><span class="sxs-lookup"><span data-stu-id="b6eb1-105">Systematically Releasing Objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="b6eb1-106">異なるアプリケーション ドメインを使用してクラッシュを回避する</span><span class="sxs-lookup"><span data-stu-id="b6eb1-106">Using a Separate Application Domain to Avoid Crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="b6eb1-107">Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する</span><span class="sxs-lookup"><span data-stu-id="b6eb1-107">Using a Trusted Application Object Provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="b6eb1-108">イベント ハンドラーで変数の範囲を適切に設定する</span><span class="sxs-lookup"><span data-stu-id="b6eb1-108">Scoping Variables Appropriately in Event Handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="b6eb1-109">マネージ Outlook アドインでサポートされないテクノロジを回避する</span><span class="sxs-lookup"><span data-stu-id="b6eb1-109">Avoiding Unsupported Technologies in Managed Outlook Add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="b6eb1-110">複数のバージョンの Outlook を使用する場合の遅延バインディングの使用</span><span class="sxs-lookup"><span data-stu-id="b6eb1-110">Using Late Binding If Depending on Multiple Versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

