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
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588455"
---
# <a name="gender"></a><span data-ttu-id="e3ac3-103">Gender</span><span class="sxs-lookup"><span data-stu-id="e3ac3-103">Gender</span></span>

  
  
<span data-ttu-id="e3ac3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3ac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3ac3-105">メッセージング ユーザーの性別の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e3ac3-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e3ac3-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e3ac3-107">Members</span><span class="sxs-lookup"><span data-stu-id="e3ac3-107">Members</span></span>

 <span data-ttu-id="e3ac3-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="e3ac3-108">_genderMin_</span></span>
  
> <span data-ttu-id="e3ac3-109">性別のサポートされている別の値の最小数です。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="e3ac3-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="e3ac3-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="e3ac3-111">メッセージング ユーザーの性別は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="e3ac3-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="e3ac3-112">_genderFemale_</span></span>
  
> <span data-ttu-id="e3ac3-113">メッセージングのユーザーは、(メス) です。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="e3ac3-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="e3ac3-114">_genderMale_</span></span>
  
> <span data-ttu-id="e3ac3-115">メッセージングのユーザーは、(オス) です。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="e3ac3-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="e3ac3-116">_genderCount_</span></span>
  
> <span data-ttu-id="e3ac3-117">性別のサポートされている別の値の数。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="e3ac3-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="e3ac3-118">_genderMax_</span></span>
  
> <span data-ttu-id="e3ac3-119">性別のサポートされている別の値の最大数です。</span><span class="sxs-lookup"><span data-stu-id="e3ac3-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3ac3-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3ac3-120">See also</span></span>



[<span data-ttu-id="e3ac3-121">PidTagGender 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3ac3-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

