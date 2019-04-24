---
title: 頻繁に使用されるプロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283108"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="2b26f-103">頻繁に使用されるプロパティの保存</span><span class="sxs-lookup"><span data-stu-id="2b26f-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="2b26f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b26f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b26f-105">時間とリソースを取得し、頻繁にアクセスするデータを保存することによって、パフォーマンスを向上させます。</span><span class="sxs-lookup"><span data-stu-id="2b26f-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="2b26f-106">その他のメモリを使用すると、繰り返し取得するより良いオプションになることがあります。</span><span class="sxs-lookup"><span data-stu-id="2b26f-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="2b26f-107">このデータを格納するためのキャッシュを作成するときは、注意して使用してください。</span><span class="sxs-lookup"><span data-stu-id="2b26f-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="2b26f-108">適切に設計されていないキャッシュは、パフォーマンスに悪影響を及ぼす可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2b26f-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="2b26f-109">たとえば、ほとんどの個人間メッセージ (ipm) クライアントは、一般的なセッションの間に、フォルダーの ipm サブツリーを表示して開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b26f-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="2b26f-110">これらの各フォルダーのエントリ識別子を格納することによって、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="2b26f-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

