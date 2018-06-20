---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーを友人かどうかを判断します。
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804345"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="beaff-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="beaff-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="beaff-104">指定したユーザーを友人かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="beaff-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="beaff-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="beaff-105">Parameters</span></span>

<span data-ttu-id="beaff-106">_ユーザー Id_</span><span class="sxs-lookup"><span data-stu-id="beaff-106">_userIds_</span></span>
  
> <span data-ttu-id="beaff-107">[in]ソーシャル ネットワーク上のユーザーのセットに対応するユーザー ID の値の配列を指定する構造体です。</span><span class="sxs-lookup"><span data-stu-id="beaff-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="beaff-108">_結果_</span><span class="sxs-lookup"><span data-stu-id="beaff-108">_results_</span></span>
  
> <span data-ttu-id="beaff-109">[out]_ユーザー Id_の配列で対応する人が友人であるかどうかを示すブール型の値の配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="beaff-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="beaff-110">備考</span><span class="sxs-lookup"><span data-stu-id="beaff-110">Remarks</span></span>

<span data-ttu-id="beaff-111">人ごとに、_ユーザー Id_のパラメーターの入力配列で表されるは、このメソッドは、_結果_のパラメーターの出力配列の対応する要素を設定します。</span><span class="sxs-lookup"><span data-stu-id="beaff-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="beaff-112">**true**は、人、友人は、 **false の場合、人が友人ではないこと**を示します。</span><span class="sxs-lookup"><span data-stu-id="beaff-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="beaff-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="beaff-113">See also</span></span>

- [<span data-ttu-id="beaff-114">ISocialProfile: ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="beaff-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

