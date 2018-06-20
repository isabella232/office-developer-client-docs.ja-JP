---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804025"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="ab8ee-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ab8ee-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="ab8ee-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab8ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab8ee-105">変更によって影響のある状態のオブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab8ee-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ab8ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab8ee-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab8ee-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="ab8ee-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="ab8ee-108">Members</span></span>

 <span data-ttu-id="ab8ee-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="ab8ee-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="ab8ee-110">**LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="ab8ee-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="ab8ee-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="ab8ee-112">ステータスが変更されたオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="ab8ee-113">**あう**</span><span class="sxs-lookup"><span data-stu-id="ab8ee-113">**cValues**</span></span>
  
> <span data-ttu-id="ab8ee-114">**LpPropVals**メンバーが指す配列内の[SPropValue](spropvalue.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="ab8ee-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="ab8ee-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="ab8ee-116">ステータスが変更されたオブジェクトのプロパティを記述する**SPropValue**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ab8ee-117">備考</span><span class="sxs-lookup"><span data-stu-id="ab8ee-117">Remarks</span></span>

<span data-ttu-id="ab8ee-118">**STATUS_OBJECT_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="ab8ee-119">**STATUS_OBJECT_NOTIFICATION**構造体では、イベントの種類の_fnevStatusObjectModified_の状態のオブジェクトの通知に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="ab8ee-120">オブジェクトのステータスの通知は、内部の MAPI 通知です。クライアントとサービス ・ プロバイダーは、登録できませんし、サービス ・ プロバイダーが生成できません。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="ab8ee-121">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="ab8ee-122">**トピック**</span><span class="sxs-lookup"><span data-stu-id="ab8ee-122">**Topic**</span></span>|<span data-ttu-id="ab8ee-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="ab8ee-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab8ee-124">MAPI でのイベントの通知</span><span class="sxs-lookup"><span data-stu-id="ab8ee-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="ab8ee-125">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="ab8ee-126">通知の処理</span><span class="sxs-lookup"><span data-stu-id="ab8ee-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="ab8ee-127">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="ab8ee-128">イベント通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="ab8ee-129">サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab8ee-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab8ee-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab8ee-130">See also</span></span>



[<span data-ttu-id="ab8ee-131">�ʒm</span><span class="sxs-lookup"><span data-stu-id="ab8ee-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ab8ee-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ab8ee-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ab8ee-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ab8ee-133">MAPI Structures</span></span>](mapi-structures.md)

