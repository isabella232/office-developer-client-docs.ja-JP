---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: POP アカウントのサーバーにメッセージのコピーを残すことを指定します。
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326489"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="55c51-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="55c51-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="55c51-104">POP アカウントのサーバーにメッセージのコピーを残すことを指定します。</span><span class="sxs-lookup"><span data-stu-id="55c51-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="55c51-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="55c51-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55c51-106">識別子:</span><span class="sxs-lookup"><span data-stu-id="55c51-106">Identifier:</span></span>  <br/> |<span data-ttu-id="55c51-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="55c51-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="55c51-108">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="55c51-108">Property type:</span></span>  <br/> |<span data-ttu-id="55c51-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="55c51-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="55c51-110">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="55c51-110">Property tag:</span></span>  <br/> |<span data-ttu-id="55c51-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="55c51-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="55c51-112">接続</span><span class="sxs-lookup"><span data-stu-id="55c51-112">Access:</span></span>  <br/> |<span data-ttu-id="55c51-113">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="55c51-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c51-114">解説</span><span class="sxs-lookup"><span data-stu-id="55c51-114">Remarks</span></span>

<span data-ttu-id="55c51-115">次の表に、使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="55c51-115">The following table lists the possible values.</span></span> <span data-ttu-id="55c51-116">定数の詳細については、「 [constants (Account management API)](constants-account-management-api.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55c51-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="55c51-117">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="55c51-117">**Possible values**</span></span>|<span data-ttu-id="55c51-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="55c51-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55c51-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="55c51-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="55c51-120">メッセージをデバイスにダウンロードした後、メッセージのコピーを POP サーバーに残します。</span><span class="sxs-lookup"><span data-stu-id="55c51-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="55c51-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="55c51-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="55c51-122">メッセージをデバイスにダウンロードした後、POP サーバーから削除します。</span><span class="sxs-lookup"><span data-stu-id="55c51-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="55c51-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="55c51-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="55c51-124">ユーザーが [削除済みアイテム] フォルダーからメッセージを削除した後にのみ、POP サーバーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="55c51-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="55c51-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span><span class="sxs-lookup"><span data-stu-id="55c51-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="55c51-126">メッセージが POP サーバーから削除されるまでの日数を取得します。</span><span class="sxs-lookup"><span data-stu-id="55c51-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="55c51-127">**SET_REMOVE_AFTER_DAYS**(_日数_)</span><span class="sxs-lookup"><span data-stu-id="55c51-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="55c51-128">メッセージが POP サーバーから削除されるまでの日数を設定します。</span><span class="sxs-lookup"><span data-stu-id="55c51-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55c51-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="55c51-129">See also</span></span>

- [<span data-ttu-id="55c51-130">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="55c51-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="55c51-131">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="55c51-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

