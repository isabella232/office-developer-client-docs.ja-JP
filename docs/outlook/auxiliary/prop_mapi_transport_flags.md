---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: 必要な同期タスクOutlook、アカウントがサポートしていないユーザー インターフェイス (UI) 要素を無効にするために使用するトランスポート設定を表します。
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404527"
---
# <a name="prop_mapi_transport_flags"></a><span data-ttu-id="0cdb1-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0cdb1-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="0cdb1-104">必要な同期タスクOutlook、アカウントがサポートしていないユーザー インターフェイス (UI) 要素を無効にするために使用するトランスポート設定を表します。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0cdb1-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0cdb1-105">Quick info</span></span>

<span data-ttu-id="0cdb1-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cdb1-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="0cdb1-107">Identifier:</span></span>  <br/> |<span data-ttu-id="0cdb1-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="0cdb1-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="0cdb1-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="0cdb1-109">Property type:</span></span>  <br/> |<span data-ttu-id="0cdb1-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0cdb1-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0cdb1-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="0cdb1-111">Property tag:</span></span>  <br/> |<span data-ttu-id="0cdb1-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="0cdb1-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="0cdb1-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="0cdb1-113">Access:</span></span>  <br/> |<span data-ttu-id="0cdb1-114">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="0cdb1-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cdb1-115">注釈</span><span class="sxs-lookup"><span data-stu-id="0cdb1-115">Remarks</span></span>

<span data-ttu-id="0cdb1-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="0cdb1-117">アカウントが **MAPIACCT_SEND_ONLY** のみ送信できますが、メッセージを受信できない場合は、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="0cdb1-118">この場合、Outlook種類のアカウント (たとえば、送信/受信の UI) に適用されない UI が **無効にされます**。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0cdb1-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0cdb1-119">See also</span></span>

- [<span data-ttu-id="0cdb1-120">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="0cdb1-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="0cdb1-121">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="0cdb1-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

