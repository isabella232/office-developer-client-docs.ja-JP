---
title: 添付日付の属性
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
# <a name="attdate-attributes"></a><span data-ttu-id="9d349-103">添付日付の属性</span><span class="sxs-lookup"><span data-stu-id="9d349-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="9d349-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d349-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d349-105">日付と時刻に関連するすべての MAPI プロパティは、**日付**のプレフィックスが付いた TNEF 属性にマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="9d349-106">これらはすべて、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="9d349-107">添付ファイル属性の日付と時刻も、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="9d349-108">日付と時刻に関連するすべての MAPI プロパティは、**日付**のプレフィックスが付いた TNEF 属性にマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="9d349-109">これらはすべて、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="9d349-110">添付ファイル属性の日付と時刻も、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="9d349-111">**DTR**構造体は、Win32 ヘッダーファイルで定義されている**SYSTEMTIME**構造に非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="9d349-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="9d349-112">**dtr**構造は、構造体の最初のメンバから始まる**sizeof (dtr)** バイトで、TNEF ストリームにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="9d349-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="9d349-113">**DTR**構造体は TNEF で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="9d349-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

