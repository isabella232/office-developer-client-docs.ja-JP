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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429629"
---
# <a name="notifkey"></a><span data-ttu-id="9ab9b-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="9ab9b-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="9ab9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ab9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ab9b-105">アドバイス シンク、アドバイス ソース、MAPI の間の接続を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ab9b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9ab9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ab9b-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="9ab9b-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="9ab9b-108">Members</span><span class="sxs-lookup"><span data-stu-id="9ab9b-108">Members</span></span>

 <span data-ttu-id="9ab9b-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="9ab9b-109">**cb**</span></span>
  
> <span data-ttu-id="9ab9b-110">ab メンバーのバイト **数** 。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="9ab9b-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="9ab9b-111">**ab**</span></span>
  
> <span data-ttu-id="9ab9b-112">通知キーを記述するバイトの配列。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ab9b-113">注釈</span><span class="sxs-lookup"><span data-stu-id="9ab9b-113">Remarks</span></span>

<span data-ttu-id="9ab9b-114">[IMAPISupport](imapisupportiunknown.md)の Subscribe メソッドと [Notify](imapisupport-notify.md)メソッドは **、NOTIFKEY** 構造体を使用して、適切なアドバイス ソースに関する適切なアアドバイス シンクへの通知を生成します。 [](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="9ab9b-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="9ab9b-115">サービス プロバイダーは **、Advise** メソッドが呼び出され、通知登録とその後の通知の送信を処理するために **Subscribe** を呼び出す場合に通知キーを生成します。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="9ab9b-116">通知キーには、アドバイス ソースのエントリ識別子を指定するか、定数などの他の識別アイテムを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="9ab9b-117">たとえば、メッセージ ストア プロバイダーは、フォルダーのパスを通知キーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="9ab9b-118">通知キーは、複数のプロセスで機能する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="9ab9b-119">通知キーのスコープ要件は、長期的なエントリ識別子の要件と似ている。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="9ab9b-120">ただし、エントリ識別子とは異なり、通知キーはバイナリと同等である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="9ab9b-121">通常、通知キーには、サービス プロバイダーによって定義された **GUID** 値と、そのオブジェクトに固有の他のプロバイダー固有の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="9ab9b-122">**NOTIFKEY** 構造体を使用して、通知を生成するアアドバイス シンクとオブジェクト間の接続を管理する方法については、「サポート イベント通知」[を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="9ab9b-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ab9b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ab9b-123">See also</span></span>



[<span data-ttu-id="9ab9b-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9ab9b-124">MAPI Structures</span></span>](mapi-structures.md)

