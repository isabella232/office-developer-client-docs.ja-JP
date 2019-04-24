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
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280048"
---
# <a name="notifkey"></a><span data-ttu-id="9c7e2-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="9c7e2-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="9c7e2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c7e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c7e2-105">アドバイズシンク、アドバイズ元、および MAPI 間の接続を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c7e2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9c7e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c7e2-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="9c7e2-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="9c7e2-108">Members</span><span class="sxs-lookup"><span data-stu-id="9c7e2-108">Members</span></span>

 <span data-ttu-id="9c7e2-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="9c7e2-109">**cb**</span></span>
  
> <span data-ttu-id="9c7e2-110">**ab**メンバーのバイト数。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="9c7e2-111">**l**</span><span class="sxs-lookup"><span data-stu-id="9c7e2-111">**ab**</span></span>
  
> <span data-ttu-id="9c7e2-112">通知キーを記述するバイトの配列。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c7e2-113">解説</span><span class="sxs-lookup"><span data-stu-id="9c7e2-113">Remarks</span></span>

<span data-ttu-id="9c7e2-114">[imapisupport](imapisupportiunknown.md)の[Subscribe](imapisupport-subscribe.md)メソッドおよび[Notify](imapisupport-notify.md)メソッドは、 **NOTIFKEY**構造体を使用して、適切なアドバイズソースに関する適切なアドバイズシンクに対する通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="9c7e2-115">サービスプロバイダーは、**アドバイズ**メソッドが呼び出され、通知の登録とその後の通知の送信を処理するために、 **Subscribe**を呼び出すことを希望している場合に通知キーを生成します。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="9c7e2-116">通知キーは、アドバイズ元のエントリ識別子にすることも、定数のような他の識別項目にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="9c7e2-117">たとえば、メッセージストアプロバイダーは、その通知キーとしてフォルダーのパスを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="9c7e2-118">通知キーは、複数のプロセス間で機能します。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="9c7e2-119">通知キーのスコープ要件は、長期間のエントリ識別子の場合と似ています。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="9c7e2-120">ただし、エントリ id とは異なり、通知キーはバイナリ比較可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="9c7e2-121">通常、通知キーには、サービスプロバイダーによって定義された**GUID**値と、その後にオブジェクトに固有の他のプロバイダー固有の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="9c7e2-122">**NOTIFKEY**構造を使用して、アドバイズシンクと通知を生成するオブジェクト間の接続を管理する方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c7e2-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c7e2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c7e2-123">See also</span></span>



[<span data-ttu-id="9c7e2-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9c7e2-124">MAPI Structures</span></span>](mapi-structures.md)

