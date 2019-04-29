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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410946"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="cb79d-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="cb79d-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="cb79d-104">POP アカウントのサーバーにメッセージのコピーを残すことを指定します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb79d-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cb79d-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb79d-106">識別子:</span><span class="sxs-lookup"><span data-stu-id="cb79d-106">Identifier:</span></span>  <br/> |<span data-ttu-id="cb79d-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="cb79d-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="cb79d-108">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="cb79d-108">Property type:</span></span>  <br/> |<span data-ttu-id="cb79d-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="cb79d-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="cb79d-110">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="cb79d-110">Property tag:</span></span>  <br/> |<span data-ttu-id="cb79d-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="cb79d-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="cb79d-112">接続</span><span class="sxs-lookup"><span data-stu-id="cb79d-112">Access:</span></span>  <br/> |<span data-ttu-id="cb79d-113">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cb79d-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb79d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cb79d-114">Remarks</span></span>

<span data-ttu-id="cb79d-115">次の表に、使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-115">The following table lists the possible values.</span></span> <span data-ttu-id="cb79d-116">定数の詳細については、「 [constants (Account management API)](constants-account-management-api.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb79d-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="cb79d-117">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="cb79d-117">**Possible values**</span></span>|<span data-ttu-id="cb79d-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb79d-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb79d-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="cb79d-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="cb79d-120">メッセージをデバイスにダウンロードした後、メッセージのコピーを POP サーバーに残します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="cb79d-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="cb79d-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="cb79d-122">メッセージをデバイスにダウンロードした後、POP サーバーから削除します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="cb79d-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="cb79d-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="cb79d-124">ユーザーが [削除済みアイテム] フォルダーからメッセージを削除した後にのみ、POP サーバーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="cb79d-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span><span class="sxs-lookup"><span data-stu-id="cb79d-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="cb79d-126">メッセージが POP サーバーから削除されるまでの日数を取得します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="cb79d-127">**SET_REMOVE_AFTER_DAYS**(_日数_)</span><span class="sxs-lookup"><span data-stu-id="cb79d-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="cb79d-128">メッセージが POP サーバーから削除されるまでの日数を設定します。</span><span class="sxs-lookup"><span data-stu-id="cb79d-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb79d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb79d-129">See also</span></span>

- [<span data-ttu-id="cb79d-130">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="cb79d-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="cb79d-131">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="cb79d-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

