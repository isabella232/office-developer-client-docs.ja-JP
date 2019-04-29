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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434117"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="b40b7-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b40b7-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="b40b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b40b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b40b7-105">プロファイルの管理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b40b7-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b40b7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b40b7-106">Header file:</span></span>  <br/> |<span data-ttu-id="b40b7-107">mapix</span><span class="sxs-lookup"><span data-stu-id="b40b7-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b40b7-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="b40b7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b40b7-109">プロファイル管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b40b7-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="b40b7-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="b40b7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b40b7-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b40b7-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b40b7-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b40b7-112">Called by:</span></span>  <br/> |<span data-ttu-id="b40b7-113">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b40b7-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="b40b7-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="b40b7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b40b7-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="b40b7-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="b40b7-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="b40b7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b40b7-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="b40b7-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b40b7-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="b40b7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b40b7-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b40b7-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="b40b7-120">プロファイル管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="b40b7-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-121">getprofiletable</span><span class="sxs-lookup"><span data-stu-id="b40b7-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="b40b7-122">利用可能なすべてのプロファイルについての情報を含むテーブルである、プロファイルテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b40b7-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-123">createprofile</span><span class="sxs-lookup"><span data-stu-id="b40b7-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="b40b7-124">新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b40b7-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-125">deleteprofile</span><span class="sxs-lookup"><span data-stu-id="b40b7-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="b40b7-126">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="b40b7-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-127">changeprofilepassword</span><span class="sxs-lookup"><span data-stu-id="b40b7-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="b40b7-128">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="b40b7-128">Deprecated.</span></span> <span data-ttu-id="b40b7-129">プロファイルのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="b40b7-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-130">copyprofile</span><span class="sxs-lookup"><span data-stu-id="b40b7-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="b40b7-131">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="b40b7-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-132">renameprofile</span><span class="sxs-lookup"><span data-stu-id="b40b7-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="b40b7-133">プロファイルに新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b40b7-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40b7-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="b40b7-135">クライアントの既定のプロファイルを設定またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="b40b7-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="b40b7-136">adminservices</span><span class="sxs-lookup"><span data-stu-id="b40b7-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="b40b7-137">プロファイル内のメッセージサービスに変更を加えるためのメッセージサービス管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b40b7-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b40b7-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="b40b7-138">See also</span></span>



[<span data-ttu-id="b40b7-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="b40b7-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

