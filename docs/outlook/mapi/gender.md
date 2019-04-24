---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342582"
---
# <a name="gender"></a><span data-ttu-id="2f60d-103">Gender</span><span class="sxs-lookup"><span data-stu-id="2f60d-103">Gender</span></span>

  
  
<span data-ttu-id="2f60d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f60d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f60d-105">メッセージングユーザーの性別に対して使用可能な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f60d-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2f60d-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2f60d-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="2f60d-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="2f60d-107">Members</span></span>

 <span data-ttu-id="2f60d-108">_gendermin_</span><span class="sxs-lookup"><span data-stu-id="2f60d-108">_genderMin_</span></span>
  
> <span data-ttu-id="2f60d-109">性別に対してサポートされている、さまざまな値の最小数。</span><span class="sxs-lookup"><span data-stu-id="2f60d-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="2f60d-110">_genderunspecified_</span><span class="sxs-lookup"><span data-stu-id="2f60d-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="2f60d-111">メッセージユーザーに性別が指定されていません。</span><span class="sxs-lookup"><span data-stu-id="2f60d-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="2f60d-112">_genderfemale_</span><span class="sxs-lookup"><span data-stu-id="2f60d-112">_genderFemale_</span></span>
  
> <span data-ttu-id="2f60d-113">メッセージングユーザーが女性である。</span><span class="sxs-lookup"><span data-stu-id="2f60d-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="2f60d-114">_gendermale_</span><span class="sxs-lookup"><span data-stu-id="2f60d-114">_genderMale_</span></span>
  
> <span data-ttu-id="2f60d-115">メッセージングユーザーが男性である。</span><span class="sxs-lookup"><span data-stu-id="2f60d-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="2f60d-116">_gendercount_</span><span class="sxs-lookup"><span data-stu-id="2f60d-116">_genderCount_</span></span>
  
> <span data-ttu-id="2f60d-117">性別に対してサポートされているさまざまな値の数。</span><span class="sxs-lookup"><span data-stu-id="2f60d-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="2f60d-118">_gendermax_</span><span class="sxs-lookup"><span data-stu-id="2f60d-118">_genderMax_</span></span>
  
> <span data-ttu-id="2f60d-119">性別に対してサポートされているさまざまな値の最大数。</span><span class="sxs-lookup"><span data-stu-id="2f60d-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f60d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f60d-120">See also</span></span>



[<span data-ttu-id="2f60d-121">PidTagGender 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f60d-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

