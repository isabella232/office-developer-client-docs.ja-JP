---
title: (デスクトップ データベース参照のアクセス) のカーソルの種類
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95b16ba79a90765be9c6850c6aea6a000993f695
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880426"
---
# <a name="types-of-cursors"></a><span data-ttu-id="96078-102">カーソルの種類</span><span class="sxs-lookup"><span data-stu-id="96078-102">Types of Cursors</span></span>


<span data-ttu-id="96078-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="96078-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96078-p101">アプリケーションでは、通常、必要なデータ アクセス機能を提供する最も単純なカーソルを使用することをお勧めします。基本機能 (前方移動のみ、読み取り専用、静的、スクロール型、バッファーなし) よりも優れた追加的特性には、クライアントのメモリ、ネットワークの負荷、パフォーマンスなどの面で、それぞれ代償があります。多くの場合、既定のカーソル オプションを選択すると、アプリケーションで実際に必要なものよりも複雑なカーソルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="96078-p101">As a general rule, your application should use the simplest cursor that provides the required data access. Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance. In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="96078-107">選択するカーソルの種類は、アプリケーションで結果セットを使用する方法の他、いくつかのデザイン上の考慮事項 (結果セットのサイズ、使用される可能性の高いデータの割合、データ変更による影響の程度、アプリケーションのパフォーマンス要件など) によって異なります。</span><span class="sxs-lookup"><span data-stu-id="96078-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="96078-108">最も基本的な方法として、データを変更する必要があるのか、またはデータを閲覧するだけでよいのかによって、次のようにカーソルを選択します。</span><span class="sxs-lookup"><span data-stu-id="96078-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="96078-109">結果セットをスクロールして閲覧するだけでよく、データを変更する必要がない場合は、[前方のみ](forward-only-cursors.md)カーソルまたは[静的](static-cursors.md)カーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="96078-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="96078-110">結果セットのサイズが大きく、そのうち選択する必要のある行が少数の場合は、[キーセット](keyset-cursors.md) カーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="96078-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="96078-111">すべての同時ユーザーによる最近の追加、変更、および削除に結果セットを同期させる必要がある場合は、[動的](dynamic-cursors.md)カーソルを使用します。</span><span class="sxs-lookup"><span data-stu-id="96078-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="96078-112">各種類のカーソルは明確に異なっているように見えますが、これらのカーソルの種類は、特性とオプションを組み合わせた結果にすぎないため、それほど大きく異なっているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="96078-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

