---
title: よく使用されるプロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a5fa4510f0bcad69bc17b8ac19433f66ec763fba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803793"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="735f5-103">よく使用されるプロパティの保存</span><span class="sxs-lookup"><span data-stu-id="735f5-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="735f5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="735f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="735f5-105">時間とリソースを取得して、頻繁にアクセスされるデータを格納することによってパフォーマンスを向上します。</span><span class="sxs-lookup"><span data-stu-id="735f5-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="735f5-106">余分なメモリを使用する場合があります検索を繰り返すための優れた選択肢です。</span><span class="sxs-lookup"><span data-stu-id="735f5-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="735f5-107">このデータを格納するキャッシュを作成するときの注意とお手入れを使用します。</span><span class="sxs-lookup"><span data-stu-id="735f5-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="735f5-108">設計が不十分なキャッシュのパフォーマンスに影響悪影響を及ぼすことに留意してください。</span><span class="sxs-lookup"><span data-stu-id="735f5-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="735f5-109">たとえば、最も個人間メッセージ (IPM) クライアントを表示し、通常のセッション中に何度も IPM サブツリーのフォルダーを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="735f5-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="735f5-110">これらのフォルダーのそれぞれのエントリの識別子を格納することによってパフォーマンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="735f5-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

