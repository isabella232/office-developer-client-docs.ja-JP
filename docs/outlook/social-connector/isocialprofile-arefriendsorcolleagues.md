---
title: iこの alprofilearefriendsor仕事仲間
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーがフレンドであるかどうかを判断します。
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331669"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="8d1f9-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="8d1f9-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="8d1f9-104">指定したユーザーがフレンドであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="8d1f9-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="8d1f9-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d1f9-105">Parameters</span></span>

<span data-ttu-id="8d1f9-106">_UserIds_</span><span class="sxs-lookup"><span data-stu-id="8d1f9-106">_userIds_</span></span>
  
> <span data-ttu-id="8d1f9-107">順番ソーシャルネットワーク上の一連のユーザーに対応するユーザー ID 値の配列を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="8d1f9-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="8d1f9-108">_出力_</span><span class="sxs-lookup"><span data-stu-id="8d1f9-108">_results_</span></span>
  
> <span data-ttu-id="8d1f9-109">読み上げブール値の配列を指定する構造体へのポインター。これは、 _userIds_配列内の対応する人物がフレンドであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8d1f9-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8d1f9-110">解説</span><span class="sxs-lookup"><span data-stu-id="8d1f9-110">Remarks</span></span>

<span data-ttu-id="8d1f9-111">_userIds_パラメーターの入力配列に表示される各ユーザーについて、このメソッドは、 _results_パラメーターの出力配列の対応する要素を設定します。</span><span class="sxs-lookup"><span data-stu-id="8d1f9-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="8d1f9-112">**true**は、ユーザーがフレンドであることを示し、 **false**は、その人物がフレンドではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8d1f9-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d1f9-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d1f9-113">See also</span></span>

- [<span data-ttu-id="8d1f9-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="8d1f9-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

