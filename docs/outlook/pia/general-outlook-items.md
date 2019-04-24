---
title: Outlook アイテム全般
TOCTitle: General Outlook items
ms:assetid: e7d57811-17b6-4689-b2fc-8eddddcbb6ba
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292516(v=office.15)
ms:contentKeyID: 55119843
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4133baf2a1b8c84ab887896e4c563fe0f8ece533
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269959"
---
# <a name="general-outlook-items"></a><span data-ttu-id="18b0a-102">Outlook アイテム全般</span><span class="sxs-lookup"><span data-stu-id="18b0a-102">General Outlook items</span></span>

<span data-ttu-id="18b0a-103">このセクションでは、Microsoft Outlook のアイテム全般に適用されるサンプル コードを示します。</span><span class="sxs-lookup"><span data-stu-id="18b0a-103">This section provides sample code that applies to items in Microsoft Outlook in general.</span></span>

<span data-ttu-id="18b0a-104">このセクションには、Microsoft Outlook のほとんどのアイテムに適用されるサンプル コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="18b0a-104">This section includes sample code that is applicable to most Outlook items.</span></span> <span data-ttu-id="18b0a-105">[\_AppointmentItem](https://msdn.microsoft.com/library/bb623692\(v=office.15\))、[\_ContactItem](https://msdn.microsoft.com/library/bb643903\(v=office.15\))、[\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) の各オブジェクトを個別に取り扱うセクションで、他の例を参照できます。</span><span class="sxs-lookup"><span data-stu-id="18b0a-105">Further examples are available under sections specific for the [\_AppointmentItem](https://msdn.microsoft.com/library/bb623692\(v=office.15\)), [\_ContactItem](https://msdn.microsoft.com/library/bb643903\(v=office.15\)), and [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18b0a-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="18b0a-106">In this section</span></span>

|<span data-ttu-id="18b0a-107">トピック</span><span class="sxs-lookup"><span data-stu-id="18b0a-107">Topic</span></span>|<span data-ttu-id="18b0a-108">説明</span><span class="sxs-lookup"><span data-stu-id="18b0a-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="18b0a-109">ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする</span><span class="sxs-lookup"><span data-stu-id="18b0a-109">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) |<span data-ttu-id="18b0a-110">Outlook アイテム オブジェクトの共通するプロパティおよびメソッドにアクセスする OutlookItem ヘルパー クラスを実装して、これらのメンバーにアクセスする前に、特定のアイテム オブジェクトをテストおよびキャストするためのオーバーヘッドを節約します。</span><span class="sxs-lookup"><span data-stu-id="18b0a-110">Implements an OutlookItem helper class that accesses common properties and methods of Outlook item objects, saving the overhead of testing for and casting to a specific item object before accessing these members.</span></span> <span data-ttu-id="18b0a-111">「関連項目」セクションに記載されている他の方法のトピックでも、このヘルパー クラスを利用しています。</span><span class="sxs-lookup"><span data-stu-id="18b0a-111">Several other how-to topics listed in the See also section take advantage of this helper class.</span></span>|
|[<span data-ttu-id="18b0a-112">アクティブ エクスプローラーで選択した項目を表示する</span><span class="sxs-lookup"><span data-stu-id="18b0a-112">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)  |<span data-ttu-id="18b0a-113">OutlookItem ヘルパー クラスを利用して、アクティブなエクスプローラー ウィンドウで選択したすべてのアイテムを簡単に表示します。</span><span class="sxs-lookup"><span data-stu-id="18b0a-113">Uses the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>|

## <a name="see-also"></a><span data-ttu-id="18b0a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="18b0a-114">See also</span></span>

- [<span data-ttu-id="18b0a-115">iCalendar ファイルを開いて内容を表示する</span><span class="sxs-lookup"><span data-stu-id="18b0a-115">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)
- [<span data-ttu-id="18b0a-116">分類項目をアイテムに割り当てる</span><span class="sxs-lookup"><span data-stu-id="18b0a-116">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)
- [<span data-ttu-id="18b0a-117">インスペクターのラッパーを実装し、インスペクターごとにアイテム レベルのイベントを追跡する</span><span class="sxs-lookup"><span data-stu-id="18b0a-117">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)
- [<span data-ttu-id="18b0a-118">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="18b0a-118">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)


