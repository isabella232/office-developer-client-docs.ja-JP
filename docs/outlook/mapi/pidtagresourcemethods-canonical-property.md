---
title: PidTagResourceMethods 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330143"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="9c2d9-103">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9c2d9-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="9c2d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c2d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c2d9-105">状態オブジェクトでサポートされている**imapistatus**インターフェイスのメソッドを示すフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c2d9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9c2d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c2d9-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="9c2d9-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="9c2d9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9c2d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c2d9-109">0x3e02</span><span class="sxs-lookup"><span data-stu-id="9c2d9-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="9c2d9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9c2d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c2d9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9c2d9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9c2d9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9c2d9-112">Area:</span></span>  <br/> |<span data-ttu-id="9c2d9-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="9c2d9-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c2d9-114">解説</span><span class="sxs-lookup"><span data-stu-id="9c2d9-114">Remarks</span></span>

<span data-ttu-id="9c2d9-115">このプロパティは、ステータスオブジェクトの**imapistatus**の実装のどのメソッドがサポートされているかを示します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="9c2d9-116">Status オブジェクトは、サポートされていないメソッドから MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="9c2d9-117">クライアントは、ステータスオブジェクトの**PR_RESOURCE_METHODS**プロパティを使用して、サポートされていないメソッドを呼び出すことを回避します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="9c2d9-118">特定のメソッドに対応するフラグが設定されている場合、メソッドが存在し、呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="9c2d9-119">このフラグがオフの場合は、メソッドを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="9c2d9-120">MAPI によって実装される状態オブジェクトは、次の方法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="9c2d9-121">**Status オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="9c2d9-121">**Status object**</span></span>|<span data-ttu-id="9c2d9-122">**サポートされているメソッド**</span><span class="sxs-lookup"><span data-stu-id="9c2d9-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c2d9-123">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="9c2d9-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="9c2d9-124">**validatestate**のみ</span><span class="sxs-lookup"><span data-stu-id="9c2d9-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="9c2d9-125">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="9c2d9-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="9c2d9-126">**validatestate**のみ</span><span class="sxs-lookup"><span data-stu-id="9c2d9-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="9c2d9-127">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="9c2d9-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="9c2d9-128">**validatestate**および**flushqueues**</span><span class="sxs-lookup"><span data-stu-id="9c2d9-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="9c2d9-129">**PR_RESOURCE_METHODS**では、次のフラグのうち1つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="9c2d9-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="9c2d9-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="9c2d9-131">[imapistatus:: ChangePassword](imapistatus-changepassword.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="9c2d9-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="9c2d9-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="9c2d9-133">[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="9c2d9-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9c2d9-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="9c2d9-135">[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="9c2d9-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="9c2d9-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="9c2d9-137">[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="9c2d9-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9c2d9-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9c2d9-139">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9c2d9-139">Header files</span></span>

<span data-ttu-id="9c2d9-140">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c2d9-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c2d9-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c2d9-142">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9c2d9-142">Mapitags.h</span></span>
  
> <span data-ttu-id="9c2d9-143">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c2d9-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c2d9-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c2d9-144">See also</span></span>



[<span data-ttu-id="9c2d9-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9c2d9-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c2d9-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9c2d9-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c2d9-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9c2d9-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c2d9-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9c2d9-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

