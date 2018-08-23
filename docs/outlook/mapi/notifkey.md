---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c480c420753b2da6c57b3961589d5c2e2e8022a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801675"
---
# <a name="notifkey"></a><span data-ttu-id="6463e-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="6463e-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="6463e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6463e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6463e-105">アドバイズ シンク、アドバイズ ソースと MAPI との間の接続を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="6463e-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6463e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6463e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6463e-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="6463e-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="6463e-108">Members</span><span class="sxs-lookup"><span data-stu-id="6463e-108">Members</span></span>

 <span data-ttu-id="6463e-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="6463e-109">**cb**</span></span>
  
> <span data-ttu-id="6463e-110">**Ab**メンバーのバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="6463e-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="6463e-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="6463e-111">**ab**</span></span>
  
> <span data-ttu-id="6463e-112">通知キーを記述するバイトの配列です。</span><span class="sxs-lookup"><span data-stu-id="6463e-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6463e-113">注釈</span><span class="sxs-lookup"><span data-stu-id="6463e-113">Remarks</span></span>

<span data-ttu-id="6463e-114">[IMAPISupport](imapisupportiunknown.md)の[購読](imapisupport-subscribe.md)と[通知](imapisupport-notify.md)方法は、適切なアドバイスのソースに関する適切なアドバイズ シンクに通知を生成するのに**NOTIFKEY**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="6463e-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="6463e-115">サービスのプロバイダーは、**そのメソッド**が呼び出され、通知の登録と通知のそれ以降の送信を処理するために**購読**を呼び出すときに通知キーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6463e-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="6463e-116">アドバイズ ソースのエントリ id は、通知のキーまたは定数などの他の識別項目を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6463e-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="6463e-117">などのメッセージ ストア プロバイダーでは、その通知キーとしてフォルダーのパスを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6463e-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="6463e-118">通知キーは、複数のプロセス間で動作するはずです。</span><span class="sxs-lookup"><span data-stu-id="6463e-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="6463e-119">通知キーのスコープ要件では、長期のエントリ id のようになります。</span><span class="sxs-lookup"><span data-stu-id="6463e-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="6463e-120">ただし、エントリの識別子とは異なり通知キーをバイナリ比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6463e-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="6463e-121">通常、通知のキーには、オブジェクトに固有の他のプロバイダー固有情報の後にサービス ・ プロバイダーによって定義された**GUID**の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6463e-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="6463e-122">管理する**NOTIFKEY**構造体の使用の詳細については、通知を生成するオブジェクトとアドバイズ シンクの接続には、[イベント通知をサポートしている](supporting-event-notification.md)が参照してください。</span><span class="sxs-lookup"><span data-stu-id="6463e-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6463e-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="6463e-123">See also</span></span>



[<span data-ttu-id="6463e-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="6463e-124">MAPI Structures</span></span>](mapi-structures.md)

