---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーがフレンドかどうかを指定します。
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412563"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="25b05-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="25b05-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="25b05-104">指定したユーザーがフレンドかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="25b05-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="25b05-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25b05-105">Parameters</span></span>

<span data-ttu-id="25b05-106">_UserIds_</span><span class="sxs-lookup"><span data-stu-id="25b05-106">_userIds_</span></span>
  
> <span data-ttu-id="25b05-107">[in]ソーシャル ネットワーク上の一連のユーザーに対応するユーザー ID 値の配列を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="25b05-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="25b05-108">_結果_</span><span class="sxs-lookup"><span data-stu-id="25b05-108">_results_</span></span>
  
> <span data-ttu-id="25b05-109">[out]userIds 配列の対応する人物がフレンドであるかどうかを示すブール型  _(Boolean)_ の値の配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="25b05-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="25b05-110">注釈</span><span class="sxs-lookup"><span data-stu-id="25b05-110">Remarks</span></span>

<span data-ttu-id="25b05-111">_userIds_ パラメーターの入力配列で表される各ユーザーについて、このメソッドは、results パラメーターの出力配列に対応する要素を _設定_ します。</span><span class="sxs-lookup"><span data-stu-id="25b05-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="25b05-112">**true** は、そのユーザーが友人であり **、false は** 、そのユーザーが友人ではないと示します。</span><span class="sxs-lookup"><span data-stu-id="25b05-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25b05-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="25b05-113">See also</span></span>

- [<span data-ttu-id="25b05-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="25b05-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

