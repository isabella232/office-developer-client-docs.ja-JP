---
title: マネージ Outlook アドインの開発でのベスト プラクティス
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 474a43c17360979b4b25ccb55c0ed48b2c9d2ef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359081"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="5911d-102">マネージ Outlook アドインの開発でのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="5911d-102">Best practices in developing managed Outlook add-ins</span></span>

<span data-ttu-id="5911d-p101">Outlook の相互運用機能アセンブリを使用すると Outlook と相互運用できるマネージ ソリューションを作成できますが、Outlook は .NET Framework より前から存在しており、Visual Basic for Applications (VBA) や Visual Basic などのアンマネージ言語でのプログラミングをサポートするように設計されています。ここでは、Outlook 用のマネージ アドインを開発するときに注意する必要のある最重要事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="5911d-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="5911d-105">オブジェクトを系統的に解放する</span><span class="sxs-lookup"><span data-stu-id="5911d-105">Systematically releasing objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="5911d-106">異なるアプリケーション ドメインを使用してクラッシュを回避する</span><span class="sxs-lookup"><span data-stu-id="5911d-106">Using a separate application domain to avoid crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="5911d-107">Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する</span><span class="sxs-lookup"><span data-stu-id="5911d-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="5911d-108">イベント ハンドラーで変数の範囲を適切に設定する</span><span class="sxs-lookup"><span data-stu-id="5911d-108">Scoping variables appropriately in event handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="5911d-109">マネージ Outlook アドインでサポートされないテクノロジを回避する</span><span class="sxs-lookup"><span data-stu-id="5911d-109">Avoiding unsupported technologies in managed Outlook add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="5911d-110">複数のバージョンの Outlook を使用する場合の遅延バインディングの使用</span><span class="sxs-lookup"><span data-stu-id="5911d-110">Using late binding if depending on multiple versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

