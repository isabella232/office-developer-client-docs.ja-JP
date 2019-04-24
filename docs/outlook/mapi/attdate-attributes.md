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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318068"
---
# <a name="attdate-attributes"></a><span data-ttu-id="593fc-103">添付日付の属性</span><span class="sxs-lookup"><span data-stu-id="593fc-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="593fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="593fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="593fc-105">日付と時刻に関連するすべての MAPI プロパティは、**日付**のプレフィックスが付いた TNEF 属性にマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="593fc-106">これらはすべて、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="593fc-107">添付ファイル属性の日付と時刻も、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="593fc-108">日付と時刻に関連するすべての MAPI プロパティは、**日付**のプレフィックスが付いた TNEF 属性にマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="593fc-109">これらはすべて、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="593fc-110">添付ファイル属性の日付と時刻も、 **DTR**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="593fc-111">**DTR**構造体は、Win32 ヘッダーファイルで定義されている**SYSTEMTIME**構造に非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="593fc-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="593fc-112">**dtr**構造は、構造体の最初のメンバから始まる**sizeof (dtr)** バイトで、TNEF ストリームにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="593fc-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="593fc-113">**DTR**構造体は TNEF で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="593fc-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

