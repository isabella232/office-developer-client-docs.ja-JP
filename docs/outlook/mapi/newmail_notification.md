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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801656"
---
# <a name="newmailnotification"></a><span data-ttu-id="ab6f2-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ab6f2-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="ab6f2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab6f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab6f2-105">新しいメッセージの到着に関連する情報をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab6f2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ab6f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab6f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab6f2-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="ab6f2-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="ab6f2-108">Members</span></span>

 <span data-ttu-id="ab6f2-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="ab6f2-110">**LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="ab6f2-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="ab6f2-112">新しく到着したメッセージのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="ab6f2-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-113">**cbParentID**</span></span>
  
> <span data-ttu-id="ab6f2-114">**LpParentID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="ab6f2-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-115">**lpParentID**</span></span>
  
> <span data-ttu-id="ab6f2-116">新しく到着したメッセージの受信フォルダーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="ab6f2-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-117">**ulFlags**</span></span>
  
> <span data-ttu-id="ab6f2-118">メッセージに含まれている文字列のプロパティの形式を記述するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="ab6f2-119">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-119">The following flag can be set:</span></span>
    
<span data-ttu-id="ab6f2-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab6f2-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ab6f2-121">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ab6f2-122">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ab6f2-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="ab6f2-124">新しく到着したメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="ab6f2-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="ab6f2-126">新しく到着したメッセージの現在の状態を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="ab6f2-127">**UlMessageFlags**メンバーは、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab6f2-128">備考</span><span class="sxs-lookup"><span data-stu-id="ab6f2-128">Remarks</span></span>

<span data-ttu-id="ab6f2-129">**NEWMAIL_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="ab6f2-130">**通知**の構造体の**ulEventType**メンバー設定されている**通知**の構造体のメンバー**情報**には、 **NEWMAIL_NOTIFICATION**構造体が含まれている、 _fnevNewMail です_。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="ab6f2-131">MAPI では、アドバイズ シンクに通知イベントに関する情報を保持する、**通知**の構造体のメンバーとしてだけ**NEWMAIL_NOTIFICATION**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="ab6f2-132">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="ab6f2-133">**トピック**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-133">**Topic**</span></span>|<span data-ttu-id="ab6f2-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="ab6f2-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab6f2-135">MAPI でのイベントの通知</span><span class="sxs-lookup"><span data-stu-id="ab6f2-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="ab6f2-136">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="ab6f2-137">通知の処理</span><span class="sxs-lookup"><span data-stu-id="ab6f2-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="ab6f2-138">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="ab6f2-139">イベント通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="ab6f2-140">サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab6f2-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab6f2-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab6f2-141">See also</span></span>



[<span data-ttu-id="ab6f2-142">�ʒm</span><span class="sxs-lookup"><span data-stu-id="ab6f2-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ab6f2-143">PidTagMessageFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ab6f2-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="ab6f2-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ab6f2-144">MAPI Structures</span></span>](mapi-structures.md)

