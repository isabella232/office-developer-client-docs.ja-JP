---
title: attDate 属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799710"
---
# <a name="attdate-attributes"></a><span data-ttu-id="2fe22-103">attDate 属性</span><span class="sxs-lookup"><span data-stu-id="2fe22-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="2fe22-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fe22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fe22-105">日付と時刻に関連するすべての MAPI プロパティは、 **attDate**プレフィックスを持つ TNEF の属性にマップされます。</span><span class="sxs-lookup"><span data-stu-id="2fe22-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="2fe22-106">これら**DTR**の構造体としてすべてエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2fe22-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="2fe22-107">日付と時刻の添付ファイルの属性は、 **DTR**も同様の構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="2fe22-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="2fe22-108">日付と時刻に関連するすべての MAPI プロパティは、 **attDate**プレフィックスを持つ TNEF の属性にマップされます。</span><span class="sxs-lookup"><span data-stu-id="2fe22-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="2fe22-109">これら**DTR**の構造体としてすべてエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2fe22-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="2fe22-110">日付と時刻の添付ファイルの属性は、 **DTR**も同様の構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="2fe22-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="2fe22-111">**DTR**構造体は、Win32 ヘッダー ファイルで定義されている**SYSTEMTIME**構造体に非常に似ています。</span><span class="sxs-lookup"><span data-stu-id="2fe22-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="2fe22-112">**DTR**の構造は、 **sizeof(DTR)** バイトの構造体の最初のメンバーで始まる、TNEF ストリームにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="2fe22-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="2fe22-113">**DTR**の構造は、TNEF で定義されます。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="2fe22-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

