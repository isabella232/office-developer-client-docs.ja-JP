---
title: よく使うプロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424554"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="66c29-103">よく使うプロパティの保存</span><span class="sxs-lookup"><span data-stu-id="66c29-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="66c29-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66c29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66c29-105">取得に時間とリソースを要し、頻繁にアクセスするデータを格納することで、パフォーマンスを向上させます。</span><span class="sxs-lookup"><span data-stu-id="66c29-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="66c29-106">余分なメモリを使用すると、取得を繰り返す方が良いオプションになる場合があります。</span><span class="sxs-lookup"><span data-stu-id="66c29-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="66c29-107">このデータを格納するためのキャッシュを作成する場合は、注意と注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="66c29-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="66c29-108">キャッシュの設計が不十分な場合、パフォーマンスに悪影響を及ぼす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="66c29-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="66c29-109">たとえば、ほとんどの対人間メッセージ (IPM) クライアントは、一般的なセッション中に何度もフォルダーの IPM サブツリーを表示および開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="66c29-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="66c29-110">これらの各フォルダーのエントリ識別子を格納することで、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="66c29-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

