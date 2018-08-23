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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804025"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="ca404-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ca404-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="ca404-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca404-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca404-105">変更によって影響のある状態のオブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ca404-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca404-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ca404-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca404-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca404-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="ca404-108">Members</span><span class="sxs-lookup"><span data-stu-id="ca404-108">Members</span></span>

 <span data-ttu-id="ca404-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="ca404-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="ca404-110">**LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ca404-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="ca404-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="ca404-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="ca404-112">ステータスが変更されたオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca404-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="ca404-113">**あう**</span><span class="sxs-lookup"><span data-stu-id="ca404-113">**cValues**</span></span>
  
> <span data-ttu-id="ca404-114">**LpPropVals**メンバーが指す配列内の[SPropValue](spropvalue.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="ca404-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="ca404-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="ca404-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="ca404-116">ステータスが変更されたオブジェクトのプロパティを記述する**SPropValue**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca404-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ca404-117">注釈</span><span class="sxs-lookup"><span data-stu-id="ca404-117">Remarks</span></span>

<span data-ttu-id="ca404-118">**STATUS_OBJECT_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ca404-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="ca404-119">**STATUS_OBJECT_NOTIFICATION**構造体では、イベントの種類の_fnevStatusObjectModified_の状態のオブジェクトの通知に含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca404-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="ca404-120">オブジェクトのステータスの通知は、内部の MAPI 通知です。クライアントとサービス ・ プロバイダーは、登録できませんし、サービス ・ プロバイダーが生成できません。</span><span class="sxs-lookup"><span data-stu-id="ca404-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="ca404-121">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca404-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="ca404-122">**トピック**</span><span class="sxs-lookup"><span data-stu-id="ca404-122">**Topic**</span></span>|<span data-ttu-id="ca404-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="ca404-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca404-124">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="ca404-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="ca404-125">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="ca404-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="ca404-126">通知の処理</span><span class="sxs-lookup"><span data-stu-id="ca404-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="ca404-127">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca404-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="ca404-128">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="ca404-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="ca404-129">サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca404-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca404-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca404-130">See also</span></span>



[<span data-ttu-id="ca404-131">�ʒm</span><span class="sxs-lookup"><span data-stu-id="ca404-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ca404-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ca404-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ca404-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ca404-133">MAPI Structures</span></span>](mapi-structures.md)

