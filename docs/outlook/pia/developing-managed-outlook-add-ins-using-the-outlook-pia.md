---
title: Outlook PIA を使用してマネージ Outlook アドインを開発する
TOCTitle: Developing managed Outlook add-ins using the Outlook PIA
ms:assetid: a779f49e-656b-4726-b0c6-37c4a6f9abd1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646706(v=office.15)
ms:contentKeyID: 55119781
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 765d6304957642fc84411aca1af695e10666e130
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721200"
---
# <a name="developing-managed-outlook-add-ins-using-the-outlook-pia"></a><span data-ttu-id="eeeb8-102">Outlook PIA を使用してマネージ Outlook アドインを開発する</span><span class="sxs-lookup"><span data-stu-id="eeeb8-102">Developing managed Outlook add-ins using the Outlook PIA</span></span>

<span data-ttu-id="eeeb8-103">ここでは、Outlook プライマリ相互運用機能アセンブリ (PIA) を使用したカスタム イベント処理、およびマネージ Outlook アドインを作成するときに発生しやすい誤りを避けるために理解しておく必要のあるいくつかの事柄について説明します。PIA を使用して Office 用のマネージ アプリケーションを作成する方法の基本については、「[Visual Studio Tools for Office](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eeeb8-103">The topics in this section describe custom event handling using the Outlook Primary Interop Assembly (PIA) and list a few areas that you should be aware of to avoid common pitfalls when writing managed Outlook add-ins. For more basic information about writing managed applications for Office using PIA, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eeeb8-104">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="eeeb8-104">In this section</span></span>

|<span data-ttu-id="eeeb8-105">トピック</span><span class="sxs-lookup"><span data-stu-id="eeeb8-105">Topic</span></span>|<span data-ttu-id="eeeb8-106">説明</span><span class="sxs-lookup"><span data-stu-id="eeeb8-106">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="eeeb8-107">カスタム イベント ハンドラーに接続する</span><span class="sxs-lookup"><span data-stu-id="eeeb8-107">Connecting to custom event handlers</span></span>](connecting-to-custom-event-handlers.md) |<span data-ttu-id="eeeb8-108">コールバック メソッドを定義し、それをカスタム イベント ハンドラーとして Outlook オブジェクトに接続する処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="eeeb8-108">Describes the process of defining a callback method and connecting it as a custom event handler for an Outlook object.</span></span>|
|[<span data-ttu-id="eeeb8-109">マネージ Outlook アドインの開発でのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="eeeb8-109">Best practices in developing managed Outlook add-ins</span></span>](best-practices-in-developing-managed-outlook-add-ins.md) |<span data-ttu-id="eeeb8-110">マネージ Outlook アドインを開発するときの一般的な問題を避けるために推奨される方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eeeb8-110">Recommends practices to avoid some common problems in developing managed Outlook add-ins.</span></span>

## <a name="see-also"></a><span data-ttu-id="eeeb8-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="eeeb8-111">See also</span></span>

- [<span data-ttu-id="eeeb8-112">Outlook PIA を使用するためのセットアップ</span><span class="sxs-lookup"><span data-stu-id="eeeb8-112">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="eeeb8-113">Outlook PIA のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="eeeb8-113">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="eeeb8-114">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="eeeb8-114">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

