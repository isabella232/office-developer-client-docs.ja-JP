---
title: 状態オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336338"
---
# <a name="status-object-implementation"></a><span data-ttu-id="21f87-103">状態オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="21f87-103">Status object implementation</span></span>

<span data-ttu-id="21f87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21f87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21f87-105">すべてのサービス プロバイダーは、状態オブジェクトを実装し、そこからセッション状態テーブルにプロパティを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-105">All service providers must implement a status object and furnish properties from it to the session status table.</span></span> <span data-ttu-id="21f87-106">制御するリソースの数に応じて、状態テーブルに 1 つ以上の行を含めできます。</span><span class="sxs-lookup"><span data-stu-id="21f87-106">You can include one or more rows in the status table, depending on the number of resources that you control.</span></span> <span data-ttu-id="21f87-107">たとえば、トランスポート プロバイダーは、管理する各メッセージ キューの状態テーブルに行を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-107">A transport provider, for example, should create a row in the status table for each message queue it manages.</span></span> <span data-ttu-id="21f87-108">変更が発生した場合は、適切な状態テーブル行を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-108">When changes occur, the appropriate status table row must be updated.</span></span> <span data-ttu-id="21f87-109">Status オブジェクトは、状態テーブルに含まれる情報と、テーブルに含まれていない追加情報へのアクセスを提供するために実装されます。</span><span class="sxs-lookup"><span data-stu-id="21f87-109">Status objects are implemented to provide access both to the information included in the status table and to additional information not included in the table.</span></span>
  
### <a name="to-implement-a-status-object"></a><span data-ttu-id="21f87-110">状態オブジェクトを実装するには</span><span class="sxs-lookup"><span data-stu-id="21f87-110">To implement a status object</span></span>

1. <span data-ttu-id="21f87-111">ログオン オブジェクト **の OpenStatusEntry** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="21f87-111">Implement the **OpenStatusEntry** method of your logon object.</span></span> <span data-ttu-id="21f87-112">クライアントが status オブジェクトを開く場合は [、IMAPISession::OpenEntry を呼び出します](imapisession-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="21f87-112">When clients want to open your status object, they call [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="21f87-113">MAPI は、プロバイダーの **OpenStatusEntry** メソッドを呼び出して開いている要求を満たし、プロバイダーが状態オブジェクトを開き **、IMAPIStatus** 実装へのポインターをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="21f87-113">MAPI fulfills the open request by calling your provider's **OpenStatusEntry** method, causing your provider to open its status object and return to the client a pointer to its **IMAPIStatus** implementation.</span></span> <span data-ttu-id="21f87-114">**OpenStatusEntry 実装で**、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="21f87-114">In your **OpenStatusEntry** implementation, complete the following steps:</span></span> 
    
   1. <span data-ttu-id="21f87-115">ログオン オブジェクトがまだ状態オブジェクトを作成していない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="21f87-115">Perform the following tasks if your logon object has not yet created a status object:</span></span>
    
      1. <span data-ttu-id="21f87-116">サポート オブジェクトの [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、プロバイダーのプロファイル セクションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="21f87-116">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your provider's profile section.</span></span> 
          
      2. <span data-ttu-id="21f87-117">新しい状態オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="21f87-117">Create a new status object.</span></span>
          
      3. <span data-ttu-id="21f87-118">プロバイダーの状態オブジェクトにプロファイル セクションへの参照を格納し、プロファイル セクションの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) メソッドを呼び出して、参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="21f87-118">Store a reference to the profile section in your provider's status object and call the profile section's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count.</span></span> 
          
      4. <span data-ttu-id="21f87-119">プロバイダーの状態オブジェクトにログオン オブジェクトへの参照を格納し、ログオン オブジェクトの **IUnknown::AddRef** メソッドを呼び出して参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="21f87-119">Store a reference to the logon object in your provider's status object and call the logon object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
          
      5. <span data-ttu-id="21f87-120">プロバイダーのログオン オブジェクトに status オブジェクトへの参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="21f87-120">Store a reference to the status object in your provider's logon object.</span></span>
    
   2. <span data-ttu-id="21f87-121">status オブジェクトの **IUnknown::AddRef** メソッドを呼び出して、ログオン オブジェクトの参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="21f87-121">Call the status object's **IUnknown::AddRef** method to increment its reference count in the logon object.</span></span> 
    
   3. <span data-ttu-id="21f87-122">status オブジェクトのプロパティ ([PidTagObjectType](pidtagobjecttype-canonical-property.md) **)** プロパティを PR_OBJECT_TYPE に設定MAPI_STATUS。</span><span class="sxs-lookup"><span data-stu-id="21f87-122">Set the status object's **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property to MAPI_STATUS.</span></span>
    
   4. <span data-ttu-id="21f87-123">_lppMAPIStatus 出力_ パラメーターを status オブジェクトをポイントして返す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="21f87-123">Set the  _lppMAPIStatus_ output parameter to point to the status object, and return.</span></span> 
    
   5. <span data-ttu-id="21f87-124">_ulFlags 入力パラメーターを_ 確認します。</span><span class="sxs-lookup"><span data-stu-id="21f87-124">Check the  _ulFlags_ input parameter.</span></span> <span data-ttu-id="21f87-125">このオブジェクトが MAPI_MODIFYに設定され、プロバイダーが status オブジェクトへの読み取り/書き込みアクセスをサポートしている場合は、書き込み可能なオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="21f87-125">If it is set to MAPI_MODIFY and your provider supports read/write access to its status object, return a writeable object.</span></span> <span data-ttu-id="21f87-126">ただし、プロバイダーが status オブジェクトへの読み取り/書き込みアクセスをサポートしていない場合は、失敗しない。</span><span class="sxs-lookup"><span data-stu-id="21f87-126">However, if your provider does not support read/write access to its status object, do not fail.</span></span> <span data-ttu-id="21f87-127">読み取り専用の状態オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="21f87-127">Return a status object that is read-only.</span></span> <span data-ttu-id="21f87-128">読み取り/書き込み状態オブジェクトを受け取る必要があるクライアントは、変更を行う前に、読み取り/書き込みアクセス許可が付与されたことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-128">Clients that expect to receive read/write status objects should verify that read/write permission has been granted before attempting to make any changes.</span></span> 
    
2. <span data-ttu-id="21f87-129">必要なすべての状態オブジェクトと状態テーブルのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="21f87-129">Set all of the required status object and status table properties.</span></span> <span data-ttu-id="21f87-130">状態テーブルの行に含めるプロパティは、MAPI によって計算されるプロパティを除き、status オブジェクトで使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-130">The properties that you include in your status table row should be available through your status object, except for the properties calculated by MAPI.</span></span> <span data-ttu-id="21f87-131">必要なプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="21f87-131">The required properties are as follows:</span></span>
    
   - <span data-ttu-id="21f87-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="21f87-133">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-133">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="21f87-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   - <span data-ttu-id="21f87-135">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-135">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>
    
   - <span data-ttu-id="21f87-136">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-136">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>
    
   - <span data-ttu-id="21f87-137">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-137">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>
    
   - <span data-ttu-id="21f87-138">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21f87-138">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>
    
3. <span data-ttu-id="21f87-139">プロバイダーに [適した IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="21f87-139">Implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) methods that are appropriate for your provider.</span></span> <span data-ttu-id="21f87-140">プロバイダーによっては、IMAPIStatus で 4 つのメソッドのすべてが実装 **されている必要はなさそう**。</span><span class="sxs-lookup"><span data-stu-id="21f87-140">Depending on your provider, you do not need to implement all of the four methods in **IMAPIStatus**.</span></span> <span data-ttu-id="21f87-141">すべてのプロバイダーは [、IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスと [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドのメソッドの読み取り専用バージョンを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-141">Every provider should implement a read-only version of the methods of the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 

   <span data-ttu-id="21f87-142">トランスポート プロバイダーは [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)も実装する必要があります。すべてのプロバイダーは [IMAPIStatus::SettingsDialog をサポートする必要があります](imapistatus-settingsdialog.md)。</span><span class="sxs-lookup"><span data-stu-id="21f87-142">Transport providers should also implement [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md), and all providers should support [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md).</span></span> <span data-ttu-id="21f87-143">ただし [、IMAPIStatus::ChangePassword のサポートは](imapistatus-changepassword.md) オプションです。</span><span class="sxs-lookup"><span data-stu-id="21f87-143">However, support for [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) is optional.</span></span> <span data-ttu-id="21f87-144">パスワードが必要で、ユーザーがパスワードを変更できるサービス プロバイダーだけが、このメソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-144">Only service providers that require passwords and want to allow users to change them programmatically need to implement this method.</span></span> <span data-ttu-id="21f87-145">サポートするメソッドごとに、対応するビットを **PR_RESOURCE_METHODSします。**</span><span class="sxs-lookup"><span data-stu-id="21f87-145">For every method that you support, set the corresponding bit in the **PR_RESOURCE_METHODS** property.</span></span> <span data-ttu-id="21f87-146">たとえば **、ValidateState** と **SettingsDialog** のみをサポートしている場合は **、次PR_RESOURCE_METHODS** 設定します。</span><span class="sxs-lookup"><span data-stu-id="21f87-146">For example, if you support **ValidateState** and **SettingsDialog** only, set **PR_RESOURCE_METHODS** to the following:</span></span> 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   <span data-ttu-id="21f87-147">クライアントは、status オブジェクトを呼び **出す前PR_RESOURCE_METHODS** の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f87-147">Clients should check the value of **PR_RESOURCE_METHODS** before attempting to call your status object.</span></span> <span data-ttu-id="21f87-148">サポートされていないメソッドの呼び出しを処理するには、サポートされていないメソッドを返MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="21f87-148">Handle calls to any of your unsupported methods by returning MAPI_E_NO_SUPPORT.</span></span> 
    
4. <span data-ttu-id="21f87-149">ログオン [中に IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) を呼び出して、行または行を状態テーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="21f87-149">Call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) during logon to add your row or rows to the status table.</span></span> <span data-ttu-id="21f87-150">行の列情報と  _ulFlags_ パラメーターの 0 を含むプロパティ値配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="21f87-150">Pass a property value array that contains the column information for the row and 0 for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="21f87-151">セッションの後でプロバイダーの状態が変更され、列情報を更新する必要がある場合は、STATUSROW_UPDATE フラグを設定して **ModifyStatusRow** を再度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21f87-151">If at some point later in the session your provider's status changes and it becomes necessary to update the column information, call **ModifyStatusRow** again with the STATUSROW_UPDATE flag set.</span></span> 
    
<span data-ttu-id="21f87-152">状態オブジェクトの詳細については、「MAPI Status [Objects」を参照してください](mapi-status-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="21f87-152">For more information about status objects, see [MAPI Status Objects](mapi-status-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21f87-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="21f87-153">See also</span></span>

- [<span data-ttu-id="21f87-154">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="21f87-154">MAPI Service Providers</span></span>](mapi-service-providers.md)

