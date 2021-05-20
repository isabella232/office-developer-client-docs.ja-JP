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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439857"
---
# <a name="newmail_notification"></a><span data-ttu-id="f6fa5-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f6fa5-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="f6fa5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6fa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6fa5-105">新しいメッセージの到着に関連する情報を説明します。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6fa5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f6fa5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f6fa5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6fa5-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f6fa5-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6fa5-108">Members</span></span>

 <span data-ttu-id="f6fa5-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="f6fa5-110">**lpEntryID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="f6fa5-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="f6fa5-112">新しく到着したメッセージのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="f6fa5-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-113">**cbParentID**</span></span>
  
> <span data-ttu-id="f6fa5-114">**lpParentID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="f6fa5-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-115">**lpParentID**</span></span>
  
> <span data-ttu-id="f6fa5-116">新しく到着したメッセージの受信フォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="f6fa5-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-117">**ulFlags**</span></span>
  
> <span data-ttu-id="f6fa5-118">メッセージに含まれる文字列プロパティの形式を記述するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="f6fa5-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-119">The following flag can be set:</span></span>
    
<span data-ttu-id="f6fa5-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f6fa5-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f6fa5-121">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f6fa5-122">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f6fa5-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="f6fa5-124">新しく到着したメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="f6fa5-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="f6fa5-126">新しく到着したメッセージの現在の状態を表すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="f6fa5-127">**ulMessageFlags** メンバーは、メッセージのプロパティ [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md) **PR_MESSAGE_FLAGSコピーです**。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6fa5-128">注釈</span><span class="sxs-lookup"><span data-stu-id="f6fa5-128">Remarks</span></span>

<span data-ttu-id="f6fa5-129">この **NEWMAIL_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md) つです。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="f6fa5-130">**NOTIFICATION** 構造体 **の info** メンバーに、NEWMAIL_NOTIFICATION構造が含まれている場合 **、NOTIFICATION** 構造体の **ulEventType** メンバーは _fnevNewMail に設定されます。_</span><span class="sxs-lookup"><span data-stu-id="f6fa5-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="f6fa5-131">MAPI は **、NEWMAIL_NOTIFICATION** 通知シンクの通知イベントに関する情報を保持する **NOTIFICATION** 構造体のメンバーとしてのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="f6fa5-132">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="f6fa5-133">**トピック**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-133">**Topic**</span></span>|<span data-ttu-id="f6fa5-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="f6fa5-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6fa5-135">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="f6fa5-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="f6fa5-136">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="f6fa5-137">通知の処理</span><span class="sxs-lookup"><span data-stu-id="f6fa5-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="f6fa5-138">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="f6fa5-139">サポート イベント通知</span><span class="sxs-lookup"><span data-stu-id="f6fa5-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="f6fa5-140">サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6fa5-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6fa5-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6fa5-141">See also</span></span>



[<span data-ttu-id="f6fa5-142">�ʒm</span><span class="sxs-lookup"><span data-stu-id="f6fa5-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f6fa5-143">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6fa5-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="f6fa5-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f6fa5-144">MAPI Structures</span></span>](mapi-structures.md)

