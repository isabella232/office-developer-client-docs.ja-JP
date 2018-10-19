---
title: Outlook PIA のアーキテクチャ
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 759e01b7ea032f53e3afeeaccaff687afc3735b3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406149"
---
# <a name="architecture-of-the-outlook-pia"></a><span data-ttu-id="181cb-102">Outlook PIA のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="181cb-102">Architecture of the Outlook PIA</span></span>

<span data-ttu-id="181cb-p101">Outlook のプライマリ相互運用機能アセンブリ (PIA) は、マネージ コードにおける Outlook オブジェクト モデル対応開発を網羅するサポートを提供します。ただし、オブジェクト ブラウザーで PIA を初めて見たときには、PIA に多くの追加インターフェイスが含まれることと、オブジェクトのすべてのメソッド、プロパティ、およびイベント メンバーが同じオブジェクト インターフェイスで公開されているのではないということに、驚くかもしれません。このセクションの各トピックでは、コードでオブジェクト メンバーにアクセスする方法についてのガイドラインと、オブジェクト、メソッド、プロパティ、およびイベントについての情報を探す場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="181cb-p101">The Outlook Primary Interop Assembly (PIA) fully supports developing against the Outlook object model in managed code. However, when you look at the PIA in an object browser for the first time, you may be surprised by the many extra interfaces that the PIA contains, and the fact that not all method, property, and event members of an object are exposed by the same object interface. The topics in this section describe guidelines for how to access object members in code, and where to look for help for objects, methods, properties, and events.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="181cb-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="181cb-106">In this section</span></span>

|<span data-ttu-id="181cb-107">トピック</span><span class="sxs-lookup"><span data-stu-id="181cb-107">Topic</span></span>|<span data-ttu-id="181cb-108">説明</span><span class="sxs-lookup"><span data-stu-id="181cb-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="181cb-109">Outlook PIA とオブジェクト モデルの関係</span><span class="sxs-lookup"><span data-stu-id="181cb-109">Relating the Outlook PIA with the Object Model</span></span>](relating-the-outlook-pia-with-the-object-model.md) |<span data-ttu-id="181cb-110">COM ベースの Outlook オブジェクト モデルのオブジェクトおよびメンバーと、PIA のマネージ インターフェイスおよびクラスの対応について説明します。</span><span class="sxs-lookup"><span data-stu-id="181cb-110">Describes how objects and members in the COM-based Outlook object model are mapped to corresponding managed interfaces and classes in the PIA.</span></span>|
|[<span data-ttu-id="181cb-111">Outlook PIA でのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="181cb-111">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md) |<span data-ttu-id="181cb-112">COM オブジェクトにマップされる一般的な .NET インターフェイス、クラス、およびデリゲートについて、および PIA のオブジェクトにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="181cb-112">Describes the typical .NET interfaces, classes, and delegates that are mapped to a COM object, and describes how to access an object in the PIA.</span></span>|
|[<span data-ttu-id="181cb-113">Outlook PIA でのメソッドとプロパティ</span><span class="sxs-lookup"><span data-stu-id="181cb-113">Methods and Properties in the Outlook PIA</span></span>](methods-and-properties-in-the-outlook-pia.md) |<span data-ttu-id="181cb-114">PIA を使用してマネージ コード内のオブジェクトのメソッドとプロパティにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="181cb-114">Describes how to access methods and properties of an object in managed code by using the PIA.</span></span>|
|[<span data-ttu-id="181cb-115">Outlook PIA でのイベント</span><span class="sxs-lookup"><span data-stu-id="181cb-115">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md) |<span data-ttu-id="181cb-116">PIA のイベント関連のインターフェイス、デリゲート、およびシンク ヘルパー クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="181cb-116">Describes event-related interfaces, delegates, and sink helper classes in the PIA.</span></span>|

## <a name="see-also"></a><span data-ttu-id="181cb-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="181cb-117">See also</span></span>

- [<span data-ttu-id="181cb-118">Outlook PIA を使用するためのセットアップ</span><span class="sxs-lookup"><span data-stu-id="181cb-118">Setting Up to Use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="181cb-119">Outlook PIA を使用してマネージ Outlook アドインを開発する</span><span class="sxs-lookup"><span data-stu-id="181cb-119">Developing Managed Outlook Add-ins Using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="181cb-120">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="181cb-120">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

