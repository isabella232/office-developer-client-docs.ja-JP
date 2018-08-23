---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: POP アカウントのサーバーにメッセージのコピーを残すかを指定します。
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799570"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="a8180-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="a8180-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="a8180-104">POP アカウントのサーバーにメッセージのコピーを残すかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a8180-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8180-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a8180-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8180-106">識別子:</span><span class="sxs-lookup"><span data-stu-id="a8180-106">Identifier:</span></span>  <br/> |<span data-ttu-id="a8180-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="a8180-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="a8180-108">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="a8180-108">Property type:</span></span>  <br/> |<span data-ttu-id="a8180-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="a8180-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="a8180-110">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="a8180-110">Property tag:</span></span>  <br/> |<span data-ttu-id="a8180-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="a8180-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="a8180-112">アクセス:</span><span class="sxs-lookup"><span data-stu-id="a8180-112">Access:</span></span>  <br/> |<span data-ttu-id="a8180-113">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a8180-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8180-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a8180-114">Remarks</span></span>

<span data-ttu-id="a8180-115">次の表は、可能な値を一覧します。</span><span class="sxs-lookup"><span data-stu-id="a8180-115">The following table lists the possible values.</span></span> <span data-ttu-id="a8180-116">定数の詳細については[定数 (アカウント管理 API)](constants-account-management-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8180-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="a8180-117">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a8180-117">**Possible values**</span></span>|<span data-ttu-id="a8180-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8180-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8180-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="a8180-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="a8180-120">デバイスにメッセージをダウンロードした後、POP サーバーにメッセージのコピーを残します。</span><span class="sxs-lookup"><span data-stu-id="a8180-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="a8180-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="a8180-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="a8180-122">デバイスにダウンロードした後、POP サーバーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="a8180-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="a8180-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="a8180-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="a8180-124">ユーザーが削除済みアイテム フォルダーからメッセージを削除した後にのみ、POP サーバーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="a8180-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="a8180-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span><span class="sxs-lookup"><span data-stu-id="a8180-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="a8180-126">POP サーバーから、メッセージを削除するまでの日数を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8180-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="a8180-127">**SET_REMOVE_AFTER_DAYS**(_日_)</span><span class="sxs-lookup"><span data-stu-id="a8180-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="a8180-128">POP サーバーから、メッセージを削除するまでの日数を設定します。</span><span class="sxs-lookup"><span data-stu-id="a8180-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8180-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8180-129">See also</span></span>

- [<span data-ttu-id="a8180-130">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="a8180-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="a8180-131">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="a8180-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

