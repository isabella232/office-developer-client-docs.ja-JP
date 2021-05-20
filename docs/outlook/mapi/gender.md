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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428649"
---
# <a name="gender"></a><span data-ttu-id="15903-103">Gender</span><span class="sxs-lookup"><span data-stu-id="15903-103">Gender</span></span>

  
  
<span data-ttu-id="15903-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15903-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15903-105">メッセージング ユーザーの性別に使用できる値を指定します。</span><span class="sxs-lookup"><span data-stu-id="15903-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="15903-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="15903-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="15903-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="15903-107">Members</span></span>

 <span data-ttu-id="15903-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="15903-108">_genderMin_</span></span>
  
> <span data-ttu-id="15903-109">性別でサポートされる異なる値の最小数。</span><span class="sxs-lookup"><span data-stu-id="15903-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="15903-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="15903-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="15903-111">メッセージング ユーザーの性別は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="15903-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="15903-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="15903-112">_genderFemale_</span></span>
  
> <span data-ttu-id="15903-113">メッセージング ユーザーは女性です。</span><span class="sxs-lookup"><span data-stu-id="15903-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="15903-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="15903-114">_genderMale_</span></span>
  
> <span data-ttu-id="15903-115">メッセージング ユーザーは男性です。</span><span class="sxs-lookup"><span data-stu-id="15903-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="15903-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="15903-116">_genderCount_</span></span>
  
> <span data-ttu-id="15903-117">性別でサポートされるさまざまな値の数。</span><span class="sxs-lookup"><span data-stu-id="15903-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="15903-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="15903-118">_genderMax_</span></span>
  
> <span data-ttu-id="15903-119">性別でサポートされるさまざまな値の最大数。</span><span class="sxs-lookup"><span data-stu-id="15903-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15903-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="15903-120">See also</span></span>



[<span data-ttu-id="15903-121">PidTagGender 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="15903-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

