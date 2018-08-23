---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800154"
---
# <a name="gender"></a><span data-ttu-id="a6248-103">Gender</span><span class="sxs-lookup"><span data-stu-id="a6248-103">Gender</span></span>

  
  
<span data-ttu-id="a6248-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6248-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6248-105">メッセージング ユーザーの性別の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6248-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a6248-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a6248-106">Quick info</span></span>

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a><span data-ttu-id="a6248-107">Members</span><span class="sxs-lookup"><span data-stu-id="a6248-107">Members</span></span>

 <span data-ttu-id="a6248-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="a6248-108">_genderMin_</span></span>
  
> <span data-ttu-id="a6248-109">性別のサポートされている別の値の最小数です。</span><span class="sxs-lookup"><span data-stu-id="a6248-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="a6248-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="a6248-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="a6248-111">メッセージング ユーザーの性別は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="a6248-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="a6248-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="a6248-112">_genderFemale_</span></span>
  
> <span data-ttu-id="a6248-113">メッセージングのユーザーは、(メス) です。</span><span class="sxs-lookup"><span data-stu-id="a6248-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="a6248-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="a6248-114">_genderMale_</span></span>
  
> <span data-ttu-id="a6248-115">メッセージングのユーザーは、(オス) です。</span><span class="sxs-lookup"><span data-stu-id="a6248-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="a6248-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="a6248-116">_genderCount_</span></span>
  
> <span data-ttu-id="a6248-117">性別のサポートされている別の値の数。</span><span class="sxs-lookup"><span data-stu-id="a6248-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="a6248-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="a6248-118">_genderMax_</span></span>
  
> <span data-ttu-id="a6248-119">性別のサポートされている別の値の最大数です。</span><span class="sxs-lookup"><span data-stu-id="a6248-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6248-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6248-120">See also</span></span>



[<span data-ttu-id="a6248-121">PidTagGender 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6248-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

