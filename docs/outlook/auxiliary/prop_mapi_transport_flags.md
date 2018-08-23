---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Outlook を使用して必要な同期タスクを決定し、アカウントをサポートしないユーザー インターフェイス (UI) 要素を無効にするトランスポートの設定を表します。
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799569"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="a9395-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a9395-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="a9395-104">Outlook を使用して必要な同期タスクを決定し、アカウントをサポートしないユーザー インターフェイス (UI) 要素を無効にするトランスポートの設定を表します。</span><span class="sxs-lookup"><span data-stu-id="a9395-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9395-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a9395-105">Quick info</span></span>

<span data-ttu-id="a9395-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9395-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9395-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="a9395-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a9395-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="a9395-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="a9395-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="a9395-109">Property type:</span></span>  <br/> |<span data-ttu-id="a9395-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9395-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a9395-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="a9395-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a9395-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="a9395-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="a9395-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="a9395-113">Access:</span></span>  <br/> |<span data-ttu-id="a9395-114">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="a9395-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9395-115">注釈</span><span class="sxs-lookup"><span data-stu-id="a9395-115">Remarks</span></span>

<span data-ttu-id="a9395-116">取得または[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9395-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="a9395-117">アカウントは、メッセージの送信だけが、メッセージを受信できない場合は、 **MAPIACCT_SEND_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="a9395-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="a9395-118">この例では、Outlook には、この種類のアカウント (**送信/受信**するための UI など) には適用されない UI が無効になります。</span><span class="sxs-lookup"><span data-stu-id="a9395-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9395-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9395-119">See also</span></span>

- [<span data-ttu-id="a9395-120">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="a9395-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="a9395-121">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="a9395-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

