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
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577416"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="3a794-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a794-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="3a794-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a794-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a794-105">プロファイルの管理をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3a794-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a794-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3a794-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a794-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="3a794-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3a794-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="3a794-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a794-109">プロファイル管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3a794-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="3a794-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3a794-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a794-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="3a794-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="3a794-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3a794-112">Called by:</span></span>  <br/> |<span data-ttu-id="3a794-113">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3a794-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="3a794-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="3a794-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a794-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="3a794-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="3a794-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="3a794-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a794-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="3a794-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a794-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3a794-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a794-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="3a794-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="3a794-120">前のプロファイルの管理オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="3a794-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="3a794-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="3a794-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="3a794-122">プロファイル テーブルのすべての利用可能なプロファイルに関する情報を格納するテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3a794-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="3a794-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="3a794-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="3a794-124">新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="3a794-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="3a794-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="3a794-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="3a794-126">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="3a794-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="3a794-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="3a794-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="3a794-128">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="3a794-128">Deprecated.</span></span> <span data-ttu-id="3a794-129">プロファイルのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="3a794-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="3a794-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="3a794-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="3a794-131">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="3a794-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="3a794-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="3a794-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="3a794-133">プロファイルに新しい名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3a794-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="3a794-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a794-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="3a794-135">設定またはクライアントの既定のプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="3a794-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="3a794-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="3a794-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="3a794-137">プロファイル内のメッセージ サービスを変更する場合、メッセージ サービスの管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3a794-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a794-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a794-138">See also</span></span>



[<span data-ttu-id="3a794-139">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3a794-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

