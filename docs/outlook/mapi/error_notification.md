---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2405799fa59abf58583553f8e2d3718d68411a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574973"
---
# <a name="errornotification"></a><span data-ttu-id="1513f-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1513f-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="1513f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1513f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1513f-105">重大なエラーに関連する情報をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1513f-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="1513f-106">これが原因でエラーの通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="1513f-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1513f-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1513f-107">Header file:</span></span>  <br/> |<span data-ttu-id="1513f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1513f-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a><span data-ttu-id="1513f-109">Members</span><span class="sxs-lookup"><span data-stu-id="1513f-109">Members</span></span>

 <span data-ttu-id="1513f-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="1513f-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="1513f-111">**LpEntryID**で示されるエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="1513f-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="1513f-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="1513f-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="1513f-113">エラーが発生するオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1513f-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="1513f-114">**scode**</span><span class="sxs-lookup"><span data-stu-id="1513f-114">**scode**</span></span>
  
> <span data-ttu-id="1513f-115">重大なエラーのエラー値です。</span><span class="sxs-lookup"><span data-stu-id="1513f-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="1513f-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1513f-116">**ulFlags**</span></span>
  
> <span data-ttu-id="1513f-117">**LpMAPIError**が指す構造体の**lpszError**メンバーが指す文字列の書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1513f-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="1513f-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1513f-118">The following flag can be set:</span></span>
    
<span data-ttu-id="1513f-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1513f-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1513f-120">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="1513f-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1513f-121">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="1513f-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1513f-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="1513f-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="1513f-123">エラーを説明する[MAPIERROR](mapierror.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1513f-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1513f-124">注釈</span><span class="sxs-lookup"><span data-stu-id="1513f-124">Remarks</span></span>

<span data-ttu-id="1513f-125">**ERROR_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="1513f-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="1513f-126">**通知**の構造体のメンバー**情報**には、 **ERROR_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、 _fnevCriticalError_に設定されています。</span><span class="sxs-lookup"><span data-stu-id="1513f-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="1513f-127">**CbEntryID**メンバーと**lpEntryID**メンバーの値は NULL であることができます。</span><span class="sxs-lookup"><span data-stu-id="1513f-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="1513f-128">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1513f-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="1513f-129">**トピック**</span><span class="sxs-lookup"><span data-stu-id="1513f-129">**Topic**</span></span>|<span data-ttu-id="1513f-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="1513f-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1513f-131">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="1513f-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="1513f-132">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="1513f-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="1513f-133">通知の処理</span><span class="sxs-lookup"><span data-stu-id="1513f-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="1513f-134">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1513f-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="1513f-135">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="1513f-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="1513f-136">サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1513f-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1513f-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="1513f-137">See also</span></span>



[<span data-ttu-id="1513f-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1513f-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1513f-139">�ʒm</span><span class="sxs-lookup"><span data-stu-id="1513f-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="1513f-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1513f-140">MAPI Structures</span></span>](mapi-structures.md)

