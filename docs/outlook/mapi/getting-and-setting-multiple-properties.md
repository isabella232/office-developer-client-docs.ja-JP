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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299378"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="26089-103">複数プロパティの取得と設定</span><span class="sxs-lookup"><span data-stu-id="26089-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="26089-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26089-105">最も少ない数の呼び出しで可能な限り多くのプロパティを取得および設定することにより、リモートアクティビティは curtailed で、各プロパティに関連するオーバーヘッドが減少します。</span><span class="sxs-lookup"><span data-stu-id="26089-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="26089-106">サービスプロバイダーは、取得または変更のためにリモートプロシージャコールを行う前にプロパティの収集を試行しますが、開始するために複数のプロパティを要求することによって、この作業を最適化することができます。</span><span class="sxs-lookup"><span data-stu-id="26089-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="26089-107">たとえば、特定のプロパティセットに属する名前付きプロパティを持つ、今後の受信者について説明するルーティングリストを使用している場合は、すべての受信者を2つの呼び出しで処理します。</span><span class="sxs-lookup"><span data-stu-id="26089-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="26089-108">1つの呼び出しを[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)に使用して、すべての受信者プロパティの識別子を取得し、その他の[imapiprop:: GetProps](imapiprop-getprops.md)の呼び出しを使用してすべての値を取得します。</span><span class="sxs-lookup"><span data-stu-id="26089-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="26089-109">別の方法として、 **getidsfromnames**を呼び出して、各受信者の**GetProps**の呼び出しを行う方が、効率が悪くなります。</span><span class="sxs-lookup"><span data-stu-id="26089-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

