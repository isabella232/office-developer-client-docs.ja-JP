---
title: attDate 属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408279"
---
# <a name="attdate-attributes"></a><span data-ttu-id="af437-103">attDate 属性</span><span class="sxs-lookup"><span data-stu-id="af437-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="af437-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af437-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af437-105">日付と時刻に関連するすべての MAPI プロパティは **、attDate** プレフィックスを持つ TNEF 属性にマップされます。</span><span class="sxs-lookup"><span data-stu-id="af437-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="af437-106">これらはすべて **DTR 構造としてエンコード** されます。</span><span class="sxs-lookup"><span data-stu-id="af437-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="af437-107">添付ファイル属性の日付と時刻は **、DTR** 構造としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="af437-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="af437-108">日付と時刻に関連するすべての MAPI プロパティは **、attDate** プレフィックスを持つ TNEF 属性にマップされます。</span><span class="sxs-lookup"><span data-stu-id="af437-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="af437-109">これらはすべて **DTR 構造としてエンコード** されます。</span><span class="sxs-lookup"><span data-stu-id="af437-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="af437-110">添付ファイル属性の日付と時刻は **、DTR** 構造としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="af437-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="af437-111">**DTR 構造は\*\*\*\*、Win32** ヘッダー ファイルで定義されている SYSTEMTIME 構造と非常に似ています。</span><span class="sxs-lookup"><span data-stu-id="af437-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="af437-112">**DTR 構造体** は、構造体の最初のメンバーで始まる **sizeof(DTR)** バイトとして TNEF ストリームにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="af437-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="af437-113">**DTR 構造** は TNEF で定義されます。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="af437-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

