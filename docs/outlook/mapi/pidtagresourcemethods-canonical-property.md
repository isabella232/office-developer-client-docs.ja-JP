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
ms.openlocfilehash: 2e1cff8148815c3e03b92e4d57d1c6a303943c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578165"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="59dc9-103">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="59dc9-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="59dc9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59dc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59dc9-105">**IMAPIStatus**インタ フェース内の状態のオブジェクトでサポートされているメソッドを示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59dc9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="59dc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59dc9-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="59dc9-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="59dc9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="59dc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59dc9-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="59dc9-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="59dc9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="59dc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="59dc9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="59dc9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="59dc9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="59dc9-112">Area:</span></span>  <br/> |<span data-ttu-id="59dc9-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="59dc9-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59dc9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="59dc9-114">Remarks</span></span>

<span data-ttu-id="59dc9-115">このプロパティは、サポート対象の**IMAPIStatus**の実装では、状態オブジェクトのメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="59dc9-116">状態オブジェクトは、サポートされていないメソッドから MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="59dc9-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="59dc9-117">クライアントは、サポートされていないメソッドの呼び出しを避けるために、状態オブジェクトの**PR_RESOURCE_METHODS**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="59dc9-118">特定のメソッドに対応するフラグが設定されている場合、メソッドが存在し、呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="59dc9-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="59dc9-119">このフラグがオフの場合は、このメソッドは呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="59dc9-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="59dc9-120">状態オブジェクトは、MAPI のサポートで次のメソッドを実装しました。</span><span class="sxs-lookup"><span data-stu-id="59dc9-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="59dc9-121">**ステータス オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="59dc9-121">**Status object**</span></span>|<span data-ttu-id="59dc9-122">**サポートされている方法**</span><span class="sxs-lookup"><span data-stu-id="59dc9-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59dc9-123">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="59dc9-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="59dc9-124">**ValidateState**のみ</span><span class="sxs-lookup"><span data-stu-id="59dc9-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="59dc9-125">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="59dc9-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="59dc9-126">**ValidateState**のみ</span><span class="sxs-lookup"><span data-stu-id="59dc9-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="59dc9-127">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="59dc9-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="59dc9-128">**ValidateState**と**FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="59dc9-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="59dc9-129">**PR_RESOURCE_METHODS**では、次のフラグの 1 つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="59dc9-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="59dc9-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="59dc9-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="59dc9-131">[IMAPIStatus::ChangePassword](imapistatus-changepassword.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="59dc9-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="59dc9-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="59dc9-133">[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="59dc9-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="59dc9-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="59dc9-135">[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="59dc9-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="59dc9-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="59dc9-137">[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドがサポートされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="59dc9-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="59dc9-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="59dc9-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="59dc9-139">Header files</span></span>

<span data-ttu-id="59dc9-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59dc9-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="59dc9-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="59dc9-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="59dc9-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59dc9-142">Mapitags.h</span></span>
  
> <span data-ttu-id="59dc9-143">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59dc9-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59dc9-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="59dc9-144">See also</span></span>



[<span data-ttu-id="59dc9-145">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="59dc9-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59dc9-146">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="59dc9-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59dc9-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="59dc9-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59dc9-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="59dc9-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

