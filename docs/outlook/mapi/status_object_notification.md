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
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336443"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="3a2a4-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3a2a4-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="3a2a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a2a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a2a4-105">変更によって影響を受けた状態オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a2a4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3a2a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a2a4-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a2a4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="3a2a4-108">Members</span><span class="sxs-lookup"><span data-stu-id="3a2a4-108">Members</span></span>

 <span data-ttu-id="3a2a4-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="3a2a4-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="3a2a4-110">**lな tryid**メンバーによって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="3a2a4-111">**lて tryid**</span><span class="sxs-lookup"><span data-stu-id="3a2a4-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="3a2a4-112">変更された状態オブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="3a2a4-113">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="3a2a4-113">**cValues**</span></span>
  
> <span data-ttu-id="3a2a4-114">**lppropvals**メンバーによって参照されている、配列内の[spropvalue](spropvalue.md)構造体の数。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="3a2a4-115">**lppropvals**</span><span class="sxs-lookup"><span data-stu-id="3a2a4-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="3a2a4-116">変更されたステータスオブジェクトのプロパティを記述する**spropvalue**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a2a4-117">解説</span><span class="sxs-lookup"><span data-stu-id="3a2a4-117">Remarks</span></span>

<span data-ttu-id="3a2a4-118">**STATUS_OBJECT_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="3a2a4-119">**STATUS_OBJECT_NOTIFICATION**構造体は、 _fnevStatusObjectModified_型のイベントに対するステータスオブジェクト通知に含まれています。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="3a2a4-120">状態オブジェクト通知は MAPI の内部通知です。クライアントおよびサービスプロバイダーはそれを登録できず、サービスプロバイダーはそれを生成できません。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="3a2a4-121">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="3a2a4-122">**トピック**</span><span class="sxs-lookup"><span data-stu-id="3a2a4-122">**Topic**</span></span>|<span data-ttu-id="3a2a4-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="3a2a4-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a2a4-124">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="3a2a4-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="3a2a4-125">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="3a2a4-126">通知の処理</span><span class="sxs-lookup"><span data-stu-id="3a2a4-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="3a2a4-127">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="3a2a4-128">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="3a2a4-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="3a2a4-129">サービスプロバイダーが**imapisupport**メソッドを使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="3a2a4-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a2a4-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a2a4-130">See also</span></span>



[<span data-ttu-id="3a2a4-131">�ʒm</span><span class="sxs-lookup"><span data-stu-id="3a2a4-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="3a2a4-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3a2a4-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3a2a4-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="3a2a4-133">MAPI Structures</span></span>](mapi-structures.md)

