---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569513"
---
# <a name="newmailnotification"></a><span data-ttu-id="c49ab-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c49ab-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c49ab-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c49ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c49ab-105">新しいメッセージの到着に関連する情報をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c49ab-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c49ab-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c49ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="c49ab-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c49ab-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="c49ab-108">Members</span><span class="sxs-lookup"><span data-stu-id="c49ab-108">Members</span></span>

 <span data-ttu-id="c49ab-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c49ab-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c49ab-110">**LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="c49ab-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c49ab-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c49ab-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c49ab-112">新しく到着したメッセージのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49ab-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="c49ab-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="c49ab-113">**cbParentID**</span></span>
  
> <span data-ttu-id="c49ab-114">**LpParentID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="c49ab-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="c49ab-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="c49ab-115">**lpParentID**</span></span>
  
> <span data-ttu-id="c49ab-116">新しく到着したメッセージの受信フォルダーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49ab-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="c49ab-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c49ab-117">**ulFlags**</span></span>
  
> <span data-ttu-id="c49ab-118">メッセージに含まれている文字列のプロパティの形式を記述するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c49ab-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="c49ab-119">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c49ab-119">The following flag can be set:</span></span>
    
<span data-ttu-id="c49ab-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c49ab-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c49ab-121">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="c49ab-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c49ab-122">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c49ab-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c49ab-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="c49ab-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="c49ab-124">新しく到着したメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49ab-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="c49ab-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="c49ab-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="c49ab-126">新しく到着したメッセージの現在の状態を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c49ab-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="c49ab-127">**UlMessageFlags**メンバーは、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="c49ab-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c49ab-128">注釈</span><span class="sxs-lookup"><span data-stu-id="c49ab-128">Remarks</span></span>

<span data-ttu-id="c49ab-129">**NEWMAIL_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="c49ab-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c49ab-130">**通知**の構造体の**ulEventType**メンバー設定されている**通知**の構造体のメンバー**情報**には、 **NEWMAIL_NOTIFICATION**構造体が含まれている、 _fnevNewMail です_。</span><span class="sxs-lookup"><span data-stu-id="c49ab-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="c49ab-131">MAPI では、アドバイズ シンクに通知イベントに関する情報を保持する、**通知**の構造体のメンバーとしてだけ**NEWMAIL_NOTIFICATION**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="c49ab-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="c49ab-132">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c49ab-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c49ab-133">**トピック**</span><span class="sxs-lookup"><span data-stu-id="c49ab-133">**Topic**</span></span>|<span data-ttu-id="c49ab-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="c49ab-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c49ab-135">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="c49ab-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c49ab-136">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="c49ab-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c49ab-137">通知の処理</span><span class="sxs-lookup"><span data-stu-id="c49ab-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c49ab-138">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c49ab-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c49ab-139">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="c49ab-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c49ab-140">サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c49ab-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c49ab-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="c49ab-141">See also</span></span>



[<span data-ttu-id="c49ab-142">�ʒm</span><span class="sxs-lookup"><span data-stu-id="c49ab-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c49ab-143">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c49ab-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="c49ab-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="c49ab-144">MAPI Structures</span></span>](mapi-structures.md)

