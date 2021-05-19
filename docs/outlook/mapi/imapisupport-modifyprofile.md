---
title: IMAPISupportModifyProfile
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
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="8edb8-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="8edb8-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="8edb8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8edb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8edb8-105">メッセージ ストア のプロファイル セクションを永続的に変更します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8edb8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8edb8-106">Parameters</span></span>

 <span data-ttu-id="8edb8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8edb8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8edb8-108">[in]メッセージ ストアの種類を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8edb8-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="8edb8-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8edb8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8edb8-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="8edb8-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="8edb8-111">メッセージ ストアは一時的なもので、メッセージ ストア テーブルに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8edb8-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="8edb8-112">このMDB_TEMPORARY設定すると **、ModifyProfile は** 直ちにS_OK返します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8edb8-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="8edb8-113">Return value</span></span>

<span data-ttu-id="8edb8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8edb8-114">S_OK</span></span> 
  
> <span data-ttu-id="8edb8-115">プロファイル セクションの変更が成功しました。</span><span class="sxs-lookup"><span data-stu-id="8edb8-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8edb8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="8edb8-116">Remarks</span></span>

<span data-ttu-id="8edb8-117">**IMAPISupport::ModifyProfile** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="8edb8-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8edb8-118">メッセージ ストア プロバイダーは **ModifyProfile を呼び出** して、MAPI にプロファイル情報の変更を求めるプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="8edb8-119">**ModifyProfile は** 、呼び出し元プロバイダーに関連付けられているプロファイル セクションを、インストールされているメッセージ ストア プロバイダー リソースの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="8edb8-120">これにより [、IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) メソッドを使用してクライアントが使用できるメッセージ ストア テーブルにメッセージ ストアが一覧表示され、ダイアログ ボックスが表示されることなく開きます。</span><span class="sxs-lookup"><span data-stu-id="8edb8-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="8edb8-121">このフラグMDB_TEMPORARY設定されている場合、MAPI は何も実行しません。メソッドは、このフラグを使用してすぐにS_OK。</span><span class="sxs-lookup"><span data-stu-id="8edb8-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8edb8-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="8edb8-122">See also</span></span>



[<span data-ttu-id="8edb8-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="8edb8-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="8edb8-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8edb8-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

