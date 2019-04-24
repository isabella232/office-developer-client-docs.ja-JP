---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348854"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="12221-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12221-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="12221-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12221-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12221-105">プロファイルの管理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="12221-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12221-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="12221-106">Header file:</span></span>  <br/> |<span data-ttu-id="12221-107">mapix</span><span class="sxs-lookup"><span data-stu-id="12221-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="12221-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="12221-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="12221-109">プロファイル管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="12221-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="12221-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="12221-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="12221-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="12221-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="12221-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="12221-112">Called by:</span></span>  <br/> |<span data-ttu-id="12221-113">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="12221-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="12221-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="12221-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="12221-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="12221-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="12221-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="12221-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="12221-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="12221-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="12221-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="12221-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="12221-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="12221-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="12221-120">プロファイル管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="12221-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="12221-121">getprofiletable</span><span class="sxs-lookup"><span data-stu-id="12221-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="12221-122">利用可能なすべてのプロファイルについての情報を含むテーブルである、プロファイルテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="12221-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="12221-123">createprofile</span><span class="sxs-lookup"><span data-stu-id="12221-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="12221-124">新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="12221-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="12221-125">deleteprofile</span><span class="sxs-lookup"><span data-stu-id="12221-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="12221-126">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="12221-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="12221-127">changeprofilepassword</span><span class="sxs-lookup"><span data-stu-id="12221-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="12221-128">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="12221-128">Deprecated.</span></span> <span data-ttu-id="12221-129">プロファイルのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="12221-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="12221-130">copyprofile</span><span class="sxs-lookup"><span data-stu-id="12221-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="12221-131">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="12221-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="12221-132">renameprofile</span><span class="sxs-lookup"><span data-stu-id="12221-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="12221-133">プロファイルに新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="12221-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="12221-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12221-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="12221-135">クライアントの既定のプロファイルを設定またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="12221-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="12221-136">adminservices</span><span class="sxs-lookup"><span data-stu-id="12221-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="12221-137">プロファイル内のメッセージサービスに変更を加えるためのメッセージサービス管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="12221-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12221-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="12221-138">See also</span></span>



[<span data-ttu-id="12221-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="12221-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

