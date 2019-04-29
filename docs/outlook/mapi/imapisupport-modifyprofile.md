---
title: imapisupportmodifyprofile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419990"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="704e6-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="704e6-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="704e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="704e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="704e6-105">メッセージストアプロファイルセクションの変更を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="704e6-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="704e6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="704e6-106">Parameters</span></span>

 <span data-ttu-id="704e6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="704e6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="704e6-108">順番メッセージストアの種類を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="704e6-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="704e6-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="704e6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="704e6-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="704e6-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="704e6-111">メッセージストアは一時的なものであり、メッセージストアテーブルに追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="704e6-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="704e6-112">MDB_TEMPORARY が設定されている場合、 **modifyprofile**はすぐに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="704e6-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="704e6-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="704e6-113">Return value</span></span>

<span data-ttu-id="704e6-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="704e6-114">S_OK</span></span> 
  
> <span data-ttu-id="704e6-115">プロファイルセクションの変更が成功しました。</span><span class="sxs-lookup"><span data-stu-id="704e6-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="704e6-116">注釈</span><span class="sxs-lookup"><span data-stu-id="704e6-116">Remarks</span></span>

<span data-ttu-id="704e6-117">**imapisupport:: modifyprofile**メソッドは、メッセージストアプロバイダーサポートオブジェクトに対して実装されています。</span><span class="sxs-lookup"><span data-stu-id="704e6-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="704e6-118">メッセージストアプロバイダーは、「 **modifyprofile** 」を呼び出して、プロファイル情報の変更を MAPI に要求します。</span><span class="sxs-lookup"><span data-stu-id="704e6-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="704e6-119">**modifyprofile**は、呼び出し元プロバイダーに関連付けられているプロファイルセクションを、インストール済みのメッセージストアプロバイダーリソースの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="704e6-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="704e6-120">これにより、メッセージストアがメッセージストアテーブルにリストされます。これは、クライアントが[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メソッドを使用して利用でき、ダイアログボックスを表示せずに開くことができます。</span><span class="sxs-lookup"><span data-stu-id="704e6-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="704e6-121">MDB_TEMPORARY フラグが設定されている場合、MAPI は nothing を返し、メソッドはすぐに S_OK で戻ります。</span><span class="sxs-lookup"><span data-stu-id="704e6-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="704e6-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="704e6-122">See also</span></span>



[<span data-ttu-id="704e6-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="704e6-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="704e6-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="704e6-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

