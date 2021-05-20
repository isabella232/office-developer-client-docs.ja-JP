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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436336"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="8954c-103">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8954c-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="8954c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8954c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8954c-105">status オブジェクトでサポートされている **IMAPIStatus** インターフェイスのメソッドを示すフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="8954c-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8954c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8954c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8954c-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="8954c-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="8954c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8954c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8954c-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="8954c-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="8954c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8954c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8954c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8954c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8954c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8954c-112">Area:</span></span>  <br/> |<span data-ttu-id="8954c-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="8954c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8954c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8954c-114">Remarks</span></span>

<span data-ttu-id="8954c-115">このプロパティは、ステータス オブジェクトの **IMAPIStatus** の実装でサポートされているメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="8954c-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="8954c-116">Status オブジェクトは、サポートされていないメソッドMAPI_E_NO_SUPPORTを返します。</span><span class="sxs-lookup"><span data-stu-id="8954c-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="8954c-117">クライアントは、サポートされていないメソッドを **呼びPR_RESOURCE_METHODS** を避けるために、status オブジェクトのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8954c-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="8954c-118">特定のメソッドに対応するフラグが設定されている場合は、メソッドが存在し、呼び出し可能です。</span><span class="sxs-lookup"><span data-stu-id="8954c-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="8954c-119">このフラグがクリアされている場合は、メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8954c-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="8954c-120">MAPI によって実装された状態オブジェクトは、次のメソッドをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8954c-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="8954c-121">**Status オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="8954c-121">**Status object**</span></span>|<span data-ttu-id="8954c-122">**サポートされているメソッド**</span><span class="sxs-lookup"><span data-stu-id="8954c-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8954c-123">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="8954c-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="8954c-124">**ValidateState** のみ</span><span class="sxs-lookup"><span data-stu-id="8954c-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="8954c-125">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="8954c-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="8954c-126">**ValidateState** のみ</span><span class="sxs-lookup"><span data-stu-id="8954c-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="8954c-127">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="8954c-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="8954c-128">**ValidateState** と **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="8954c-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="8954c-129">次のフラグの 1 つ以上は、次の **PR_RESOURCE_METHODS。**</span><span class="sxs-lookup"><span data-stu-id="8954c-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="8954c-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="8954c-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="8954c-131">[IMAPIStatus::ChangePassword](imapistatus-changepassword.md)メソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8954c-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="8954c-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="8954c-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="8954c-133">[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8954c-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="8954c-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8954c-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="8954c-135">[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8954c-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="8954c-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="8954c-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="8954c-137">[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8954c-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="8954c-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8954c-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8954c-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8954c-139">Header files</span></span>

<span data-ttu-id="8954c-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8954c-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="8954c-141">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8954c-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="8954c-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8954c-142">Mapitags.h</span></span>
  
> <span data-ttu-id="8954c-143">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8954c-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8954c-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="8954c-144">See also</span></span>



[<span data-ttu-id="8954c-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8954c-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8954c-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8954c-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8954c-147">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8954c-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8954c-148">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8954c-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

