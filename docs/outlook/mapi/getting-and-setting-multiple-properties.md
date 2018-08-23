---
title: 取得および複数のプロパティを設定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 88c3e0bdb3cc6660e35faf62c5bb63ec2f6352bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590373"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="cad95-103">取得および複数のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cad95-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="cad95-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cad95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cad95-105">取得するを最小限にできる限り多くのプロパティを設定して、活動を削減したりし、各プロパティに含まれるオーバーヘッドを削減、リモート呼び出しの数です。</span><span class="sxs-lookup"><span data-stu-id="cad95-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="cad95-106">サービス ・ プロバイダーがプロパティを取得または変更のためのリモート プロシージャ コールを行う前に収集しようとすると、複数のプロパティを最初に要求することによってこの作業を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="cad95-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="cad95-107">などの特定のプロパティ セットに属する名前付きのプロパティと、将来の受信者を記述するルーティング リストを使用する場合は、すべての 2 つの呼び出しを使用して受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="cad95-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="cad95-108">受信者のプロパティと、その他の呼び出しの[IMAPIProp::GetProps](imapiprop-getprops.md)にすべての値を取得するためにすべての識別子を取得するために[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を 1 つの呼び出しを使用します。</span><span class="sxs-lookup"><span data-stu-id="cad95-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="cad95-109">別に、各受信者について、 **GetProps**への呼び出しの後に**GetIDsFromNames**を呼び出すことは、効率が低下します。</span><span class="sxs-lookup"><span data-stu-id="cad95-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

