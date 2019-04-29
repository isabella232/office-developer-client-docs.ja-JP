---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: 必要な同期タスクを決定するために Outlook で使用するトランスポート設定を表し、アカウントがサポートしていないユーザーインターフェイス (UI) 要素を無効にします。
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404527"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="5cf6e-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5cf6e-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="5cf6e-104">必要な同期タスクを決定するために Outlook で使用するトランスポート設定を表し、アカウントがサポートしていないユーザーインターフェイス (UI) 要素を無効にします。</span><span class="sxs-lookup"><span data-stu-id="5cf6e-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5cf6e-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5cf6e-105">Quick info</span></span>

<span data-ttu-id="5cf6e-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cf6e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5cf6e-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="5cf6e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5cf6e-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="5cf6e-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="5cf6e-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="5cf6e-109">Property type:</span></span>  <br/> |<span data-ttu-id="5cf6e-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5cf6e-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5cf6e-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="5cf6e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="5cf6e-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="5cf6e-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="5cf6e-113">接続</span><span class="sxs-lookup"><span data-stu-id="5cf6e-113">Access:</span></span>  <br/> |<span data-ttu-id="5cf6e-114">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5cf6e-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cf6e-115">注釈</span><span class="sxs-lookup"><span data-stu-id="5cf6e-115">Remarks</span></span>

<span data-ttu-id="5cf6e-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)または[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、このプロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5cf6e-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="5cf6e-117">アカウントがメッセージを送信するだけでメッセージを受信できない場合は、 **MAPIACCT_SEND_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="5cf6e-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="5cf6e-118">この場合、Outlook では、この種類のアカウントに適用されない ui (たとえば、**送信/受信**の ui) を無効にします。</span><span class="sxs-lookup"><span data-stu-id="5cf6e-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5cf6e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="5cf6e-119">See also</span></span>

- [<span data-ttu-id="5cf6e-120">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="5cf6e-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="5cf6e-121">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="5cf6e-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

