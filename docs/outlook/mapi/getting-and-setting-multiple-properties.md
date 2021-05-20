---
title: 複数プロパティの取得と設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432262"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="d3672-103">複数プロパティの取得と設定</span><span class="sxs-lookup"><span data-stu-id="d3672-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="d3672-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3672-105">呼び出し数が少ないプロパティを可能な限り多く取得して設定すると、リモート アクティビティが抑制され、各プロパティに関連するオーバーヘッドが削減されます。</span><span class="sxs-lookup"><span data-stu-id="d3672-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="d3672-106">サービス プロバイダーは、取得または変更のリモート プロシージャ呼び出しを行う前にプロパティを収集しますが、最初に複数のプロパティを要求することで、この作業を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="d3672-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="d3672-107">たとえば、特定のプロパティ セットに属する名前付きプロパティを持つ将来の受信者を記述するルーティング リストを操作する場合は、2 回の呼び出しですべての受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="d3672-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="d3672-108">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)への 1 つの呼び出しを使用して、すべての受信者プロパティの識別子を取得し、もう一方の呼び出しで[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出してすべての値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3672-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="d3672-109">別の方法として **、GetIDsFromNames** を呼び出し、その後に各受信者の **GetProps** を呼び出す方法は、はるかに効率的です。</span><span class="sxs-lookup"><span data-stu-id="d3672-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

