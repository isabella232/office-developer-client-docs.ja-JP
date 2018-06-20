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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800020"
---
# <a name="errornotification"></a><span data-ttu-id="39219-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39219-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="39219-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39219-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39219-105">重大なエラーに関連する情報をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="39219-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="39219-106">これが原因でエラーの通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="39219-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39219-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="39219-107">Header file:</span></span>  <br/> |<span data-ttu-id="39219-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39219-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="39219-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="39219-109">Members</span></span>

 <span data-ttu-id="39219-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="39219-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="39219-111">**LpEntryID**で示されるエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="39219-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="39219-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="39219-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="39219-113">エラーが発生するオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="39219-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="39219-114">**scode**</span><span class="sxs-lookup"><span data-stu-id="39219-114">**scode**</span></span>
  
> <span data-ttu-id="39219-115">重大なエラーのエラー値です。</span><span class="sxs-lookup"><span data-stu-id="39219-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="39219-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="39219-116">**ulFlags**</span></span>
  
> <span data-ttu-id="39219-117">**LpMAPIError**が指す構造体の**lpszError**メンバーが指す文字列の書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="39219-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="39219-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="39219-118">The following flag can be set:</span></span>
    
<span data-ttu-id="39219-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39219-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="39219-120">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="39219-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="39219-121">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="39219-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="39219-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="39219-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="39219-123">エラーを説明する[MAPIERROR](mapierror.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="39219-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39219-124">備考</span><span class="sxs-lookup"><span data-stu-id="39219-124">Remarks</span></span>

<span data-ttu-id="39219-125">**ERROR_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="39219-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="39219-126">**通知**の構造体のメンバー**情報**には、 **ERROR_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、 _fnevCriticalError_に設定されています。</span><span class="sxs-lookup"><span data-stu-id="39219-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="39219-127">**CbEntryID**メンバーと**lpEntryID**メンバーの値は NULL であることができます。</span><span class="sxs-lookup"><span data-stu-id="39219-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="39219-128">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="39219-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="39219-129">**トピック**</span><span class="sxs-lookup"><span data-stu-id="39219-129">**Topic**</span></span>|<span data-ttu-id="39219-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="39219-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39219-131">MAPI でのイベントの通知</span><span class="sxs-lookup"><span data-stu-id="39219-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="39219-132">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="39219-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="39219-133">通知の処理</span><span class="sxs-lookup"><span data-stu-id="39219-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="39219-134">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="39219-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="39219-135">イベント通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="39219-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="39219-136">サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="39219-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39219-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="39219-137">See also</span></span>



[<span data-ttu-id="39219-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="39219-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="39219-139">�ʒm</span><span class="sxs-lookup"><span data-stu-id="39219-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="39219-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="39219-140">MAPI Structures</span></span>](mapi-structures.md)

