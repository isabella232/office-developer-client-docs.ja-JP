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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426269"
---
# <a name="status_object_notification"></a><span data-ttu-id="8ae99-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8ae99-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8ae99-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ae99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ae99-105">変更の影響を受けた状態オブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8ae99-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ae99-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8ae99-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ae99-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ae99-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="8ae99-108">Members</span><span class="sxs-lookup"><span data-stu-id="8ae99-108">Members</span></span>

 <span data-ttu-id="8ae99-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="8ae99-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="8ae99-110">**lpEntryID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="8ae99-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="8ae99-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="8ae99-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="8ae99-112">変更された状態オブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8ae99-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="8ae99-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8ae99-113">**cValues**</span></span>
  
> <span data-ttu-id="8ae99-114">[lpPropVals](spropvalue.md)メンバーが指す配列内の **SPropValue 構造体の** 数。</span><span class="sxs-lookup"><span data-stu-id="8ae99-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="8ae99-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="8ae99-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="8ae99-116">変更された状態オブジェクトの **プロパティを記述する SPropValue** 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8ae99-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8ae99-117">注釈</span><span class="sxs-lookup"><span data-stu-id="8ae99-117">Remarks</span></span>

<span data-ttu-id="8ae99-118">このSTATUS_OBJECT_NOTIFICATIONは、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md)つです。 </span><span class="sxs-lookup"><span data-stu-id="8ae99-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8ae99-119">この **STATUS_OBJECT_NOTIFICATION** は  _、fnevStatusObjectModified_ 型のイベントの状態オブジェクト通知に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ae99-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="8ae99-120">Status オブジェクト通知は、内部 MAPI 通知です。クライアントとサービス プロバイダーは、クライアントとサービス プロバイダーに登録できません。また、サービス プロバイダーはクライアントを生成できません。</span><span class="sxs-lookup"><span data-stu-id="8ae99-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="8ae99-121">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ae99-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8ae99-122">**トピック**</span><span class="sxs-lookup"><span data-stu-id="8ae99-122">**Topic**</span></span>|<span data-ttu-id="8ae99-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="8ae99-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ae99-124">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="8ae99-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8ae99-125">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="8ae99-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8ae99-126">通知の処理</span><span class="sxs-lookup"><span data-stu-id="8ae99-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8ae99-127">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ae99-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8ae99-128">サポート イベント通知</span><span class="sxs-lookup"><span data-stu-id="8ae99-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8ae99-129">サービス プロバイダーが **IMAPISupport** メソッドを使用して通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ae99-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ae99-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ae99-130">See also</span></span>



[<span data-ttu-id="8ae99-131">�ʒm</span><span class="sxs-lookup"><span data-stu-id="8ae99-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="8ae99-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8ae99-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8ae99-133">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8ae99-133">MAPI Structures</span></span>](mapi-structures.md)

