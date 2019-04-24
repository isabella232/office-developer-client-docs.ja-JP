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
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335736"
---
# <a name="errornotification"></a><span data-ttu-id="b1dbb-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1dbb-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="b1dbb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1dbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1dbb-105">重大なエラーに関連する情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="b1dbb-106">これにより、エラー通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1dbb-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b1dbb-107">Header file:</span></span>  <br/> |<span data-ttu-id="b1dbb-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1dbb-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="b1dbb-109">Members</span><span class="sxs-lookup"><span data-stu-id="b1dbb-109">Members</span></span>

 <span data-ttu-id="b1dbb-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="b1dbb-111">**lな tryid**で示されるエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="b1dbb-112">**lて tryid**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="b1dbb-113">エラーを発生させるオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="b1dbb-114">**scode as scode**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-114">**scode**</span></span>
  
> <span data-ttu-id="b1dbb-115">重大なエラーのエラー値。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="b1dbb-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-116">**ulFlags**</span></span>
  
> <span data-ttu-id="b1dbb-117">**lpMAPIError**によって参照されている構造体で、 **lpszerror**メンバーが指すテキストの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="b1dbb-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-118">The following flag can be set:</span></span>
    
<span data-ttu-id="b1dbb-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1dbb-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1dbb-120">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b1dbb-121">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b1dbb-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="b1dbb-123">エラーを説明する[MAPIERROR](mapierror.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b1dbb-124">解説</span><span class="sxs-lookup"><span data-stu-id="b1dbb-124">Remarks</span></span>

<span data-ttu-id="b1dbb-125">**ERROR_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b1dbb-126">**通知**構造の**info**メンバーに**ERROR_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは_fnevCriticalError_に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="b1dbb-127">**cbEntryID**メンバーの値と**l tryid**メンバーは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="b1dbb-128">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b1dbb-129">**トピック**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-129">**Topic**</span></span>|<span data-ttu-id="b1dbb-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1dbb-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1dbb-131">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="b1dbb-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b1dbb-132">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b1dbb-133">通知の処理</span><span class="sxs-lookup"><span data-stu-id="b1dbb-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b1dbb-134">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b1dbb-135">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="b1dbb-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b1dbb-136">サービスプロバイダーが**imapisupport**メソッドを使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="b1dbb-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1dbb-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1dbb-137">See also</span></span>



[<span data-ttu-id="b1dbb-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b1dbb-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b1dbb-139">�ʒm</span><span class="sxs-lookup"><span data-stu-id="b1dbb-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="b1dbb-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b1dbb-140">MAPI Structures</span></span>](mapi-structures.md)

