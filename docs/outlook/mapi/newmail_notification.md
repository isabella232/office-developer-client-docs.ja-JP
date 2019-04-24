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
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326244"
---
# <a name="newmailnotification"></a><span data-ttu-id="16739-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16739-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="16739-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16739-105">新しいメッセージの到着に関連する情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="16739-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16739-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="16739-106">Header file:</span></span>  <br/> |<span data-ttu-id="16739-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16739-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="16739-108">Members</span><span class="sxs-lookup"><span data-stu-id="16739-108">Members</span></span>

 <span data-ttu-id="16739-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="16739-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="16739-110">**lな tryid**メンバーによって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="16739-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="16739-111">**lて tryid**</span><span class="sxs-lookup"><span data-stu-id="16739-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="16739-112">新しく到着したメッセージのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16739-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="16739-113">**cbparentid**</span><span class="sxs-lookup"><span data-stu-id="16739-113">**cbParentID**</span></span>
  
> <span data-ttu-id="16739-114">**lpparentid**メンバーによって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="16739-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="16739-115">**lpparentid**</span><span class="sxs-lookup"><span data-stu-id="16739-115">**lpParentID**</span></span>
  
> <span data-ttu-id="16739-116">新しく到着したメッセージの受信フォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16739-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="16739-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="16739-117">**ulFlags**</span></span>
  
> <span data-ttu-id="16739-118">メッセージに含まれる文字列プロパティの形式を記述するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="16739-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="16739-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="16739-119">The following flag can be set:</span></span>
    
<span data-ttu-id="16739-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16739-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="16739-121">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="16739-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="16739-122">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="16739-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="16739-123">**lpszmessageclass**</span><span class="sxs-lookup"><span data-stu-id="16739-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="16739-124">新しく到着したメッセージのメッセージクラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="16739-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="16739-125">**ulmessageflags**</span><span class="sxs-lookup"><span data-stu-id="16739-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="16739-126">新しく到着したメッセージの現在の状態を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="16739-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="16739-127">**ulmessageflags**メンバーは、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="16739-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16739-128">解説</span><span class="sxs-lookup"><span data-stu-id="16739-128">Remarks</span></span>

<span data-ttu-id="16739-129">**NEWMAIL_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="16739-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="16739-130">**通知**構造の**info**メンバーに**NEWMAIL_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは fnevNewMail に設定され_ます。_</span><span class="sxs-lookup"><span data-stu-id="16739-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="16739-131">MAPI では、通知シンクの通知イベントに関する情報を保持する**通知**構造のメンバとしてのみ**NEWMAIL_NOTIFICATION**構造が使用されます。</span><span class="sxs-lookup"><span data-stu-id="16739-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="16739-132">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="16739-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="16739-133">**トピック**</span><span class="sxs-lookup"><span data-stu-id="16739-133">**Topic**</span></span>|<span data-ttu-id="16739-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="16739-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16739-135">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="16739-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="16739-136">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="16739-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="16739-137">通知の処理</span><span class="sxs-lookup"><span data-stu-id="16739-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="16739-138">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="16739-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="16739-139">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="16739-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="16739-140">サービスプロバイダーが[imapisupport](imapisupportiunknown.md)メソッドを使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="16739-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16739-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="16739-141">See also</span></span>



[<span data-ttu-id="16739-142">�ʒm</span><span class="sxs-lookup"><span data-stu-id="16739-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="16739-143">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="16739-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="16739-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="16739-144">MAPI Structures</span></span>](mapi-structures.md)

