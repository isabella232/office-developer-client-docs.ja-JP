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
# <a name="status-object-implementation"></a><span data-ttu-id="8c531-103">状態オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="8c531-103">Status object implementation</span></span>

<span data-ttu-id="8c531-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c531-105">すべてのサービスプロバイダーは、status オブジェクトを実装して、そのオブジェクトからのプロパティをセッション状態テーブルに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-105">All service providers must implement a status object and furnish properties from it to the session status table.</span></span> <span data-ttu-id="8c531-106">管理するリソースの数に応じて、[状態] テーブルに1つ以上の行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8c531-106">You can include one or more rows in the status table, depending on the number of resources that you control.</span></span> <span data-ttu-id="8c531-107">たとえば、トランスポートプロバイダーは、管理する各メッセージキューの状態テーブルに行を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-107">A transport provider, for example, should create a row in the status table for each message queue it manages.</span></span> <span data-ttu-id="8c531-108">変更が発生した場合は、適切な状態テーブル行を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-108">When changes occur, the appropriate status table row must be updated.</span></span> <span data-ttu-id="8c531-109">status オブジェクトは、状態テーブルに含まれている情報と、テーブルに含まれていない追加情報の両方にアクセスできるように実装されています。</span><span class="sxs-lookup"><span data-stu-id="8c531-109">Status objects are implemented to provide access both to the information included in the status table and to additional information not included in the table.</span></span>
  
### <a name="to-implement-a-status-object"></a><span data-ttu-id="8c531-110">status オブジェクトを実装するには</span><span class="sxs-lookup"><span data-stu-id="8c531-110">To implement a status object</span></span>

1. <span data-ttu-id="8c531-111">ログオンオブジェクトの**openstatusentry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="8c531-111">Implement the **OpenStatusEntry** method of your logon object.</span></span> <span data-ttu-id="8c531-112">クライアントは、状態オブジェクトを開こうとすると、 [imapisession:: openentry](imapisession-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8c531-112">When clients want to open your status object, they call [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="8c531-113">MAPI はプロバイダーの**openstatusentry**メソッドを呼び出して open 要求を処理します。これにより、プロバイダーはその状態オブジェクトを開き、 **imapistatus**実装へのポインターをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="8c531-113">MAPI fulfills the open request by calling your provider's **OpenStatusEntry** method, causing your provider to open its status object and return to the client a pointer to its **IMAPIStatus** implementation.</span></span> <span data-ttu-id="8c531-114">**openstatusentry**実装で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c531-114">In your **OpenStatusEntry** implementation, complete the following steps:</span></span> 
    
   1. <span data-ttu-id="8c531-115">ログオンオブジェクトがステータスオブジェクトをまだ作成していない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8c531-115">Perform the following tasks if your logon object has not yet created a status object:</span></span>
    
      1. <span data-ttu-id="8c531-116">サポートオブジェクトの[imapisupport:: openprofilesection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロバイダーのプロファイルセクションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8c531-116">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your provider's profile section.</span></span> 
          
      2. <span data-ttu-id="8c531-117">新しい status オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8c531-117">Create a new status object.</span></span>
          
      3. <span data-ttu-id="8c531-118">プロバイダーの状態オブジェクトのプロファイルセクションへの参照を格納し、プロファイルセクションの[IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="8c531-118">Store a reference to the profile section in your provider's status object and call the profile section's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count.</span></span> 
          
      4. <span data-ttu-id="8c531-119">プロバイダーの status オブジェクトにログオンオブジェクトへの参照を格納し、ログオンオブジェクトの**IUnknown:: AddRef**メソッドを呼び出して、参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="8c531-119">Store a reference to the logon object in your provider's status object and call the logon object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
          
      5. <span data-ttu-id="8c531-120">プロバイダーのログオンオブジェクトに状態オブジェクトへの参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="8c531-120">Store a reference to the status object in your provider's logon object.</span></span>
    
   2. <span data-ttu-id="8c531-121">状態オブジェクトの**IUnknown:: AddRef**メソッドを呼び出して、ログオンオブジェクトの参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="8c531-121">Call the status object's **IUnknown::AddRef** method to increment its reference count in the logon object.</span></span> 
    
   3. <span data-ttu-id="8c531-122">status オブジェクトの**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティを MAPI_STATUS に設定します。</span><span class="sxs-lookup"><span data-stu-id="8c531-122">Set the status object's **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property to MAPI_STATUS.</span></span>
    
   4. <span data-ttu-id="8c531-123">_lppMAPIStatus_ output パラメーターを status オブジェクトを指すように設定し、を返します。</span><span class="sxs-lookup"><span data-stu-id="8c531-123">Set the  _lppMAPIStatus_ output parameter to point to the status object, and return.</span></span> 
    
   5. <span data-ttu-id="8c531-124">_ulflags_入力パラメーターを確認します。</span><span class="sxs-lookup"><span data-stu-id="8c531-124">Check the  _ulFlags_ input parameter.</span></span> <span data-ttu-id="8c531-125">MAPI_MODIFY に設定されており、プロバイダーがその状態オブジェクトへの読み取り/書き込みアクセスをサポートしている場合は、書き込み可能なオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="8c531-125">If it is set to MAPI_MODIFY and your provider supports read/write access to its status object, return a writeable object.</span></span> <span data-ttu-id="8c531-126">ただし、プロバイダーが status オブジェクトへの読み取り/書き込みアクセスをサポートしていない場合は、失敗しません。</span><span class="sxs-lookup"><span data-stu-id="8c531-126">However, if your provider does not support read/write access to its status object, do not fail.</span></span> <span data-ttu-id="8c531-127">読み取り専用の status オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="8c531-127">Return a status object that is read-only.</span></span> <span data-ttu-id="8c531-128">読み取り/書き込み状態のオブジェクトを受信すると予想されるクライアントは、変更を行う前に読み取り/書き込みアクセス許可が付与されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-128">Clients that expect to receive read/write status objects should verify that read/write permission has been granted before attempting to make any changes.</span></span> 
    
2. <span data-ttu-id="8c531-129">必要なすべての status オブジェクトおよび status テーブルのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c531-129">Set all of the required status object and status table properties.</span></span> <span data-ttu-id="8c531-130">状態テーブルの行に含めるプロパティは、MAPI によって計算されたプロパティを除き、状態オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c531-130">The properties that you include in your status table row should be available through your status object, except for the properties calculated by MAPI.</span></span> <span data-ttu-id="8c531-131">必要なプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8c531-131">The required properties are as follows:</span></span>
    
   - <span data-ttu-id="8c531-132">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="8c531-133">**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-133">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="8c531-134">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   - <span data-ttu-id="8c531-135">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-135">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>
    
   - <span data-ttu-id="8c531-136">**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-136">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>
    
   - <span data-ttu-id="8c531-137">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-137">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>
    
   - <span data-ttu-id="8c531-138">**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c531-138">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>
    
3. <span data-ttu-id="8c531-139">プロバイダーに適した[imapistatus: imapistatus](imapistatusimapiprop.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="8c531-139">Implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) methods that are appropriate for your provider.</span></span> <span data-ttu-id="8c531-140">プロバイダーによっては、 **imapistatus**にすべての4つのメソッドを実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8c531-140">Depending on your provider, you do not need to implement all of the four methods in **IMAPIStatus**.</span></span> <span data-ttu-id="8c531-141">すべてのプロバイダーは、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスおよび[imapiprop:: validatestate](imapistatus-validatestate.md)メソッドの読み取り専用バージョンを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-141">Every provider should implement a read-only version of the methods of the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 

   <span data-ttu-id="8c531-142">また、トランスポートプロバイダーは[imapistatus:: flushqueues](imapistatus-flushqueues.md)を実装する必要があります。また、すべてのプロバイダーは[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-142">Transport providers should also implement [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md), and all providers should support [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md).</span></span> <span data-ttu-id="8c531-143">ただし、 [imapistatus:: ChangePassword](imapistatus-changepassword.md)のサポートはオプションです。</span><span class="sxs-lookup"><span data-stu-id="8c531-143">However, support for [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) is optional.</span></span> <span data-ttu-id="8c531-144">パスワードを必要とし、ユーザーがプログラムによって変更できるようにするサービスプロバイダーのみが、このメソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-144">Only service providers that require passwords and want to allow users to change them programmatically need to implement this method.</span></span> <span data-ttu-id="8c531-145">サポートしているすべてのメソッドについて、 **PR_RESOURCE_METHODS**プロパティに対応するビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c531-145">For every method that you support, set the corresponding bit in the **PR_RESOURCE_METHODS** property.</span></span> <span data-ttu-id="8c531-146">たとえば、 **validatestate**と**settingsdialog**のみをサポートする場合は、 **PR_RESOURCE_METHODS**を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="8c531-146">For example, if you support **ValidateState** and **SettingsDialog** only, set **PR_RESOURCE_METHODS** to the following:</span></span> 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   <span data-ttu-id="8c531-147">クライアントは、status オブジェクトの呼び出しを試行する前に、 **PR_RESOURCE_METHODS**の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c531-147">Clients should check the value of **PR_RESOURCE_METHODS** before attempting to call your status object.</span></span> <span data-ttu-id="8c531-148">MAPI_E_NO_SUPPORT を返すことで、サポートされていないメソッドの呼び出しを処理します。</span><span class="sxs-lookup"><span data-stu-id="8c531-148">Handle calls to any of your unsupported methods by returning MAPI_E_NO_SUPPORT.</span></span> 
    
4. <span data-ttu-id="8c531-149">状態テーブルに行または行を追加するには、ログオン時に[imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8c531-149">Call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) during logon to add your row or rows to the status table.</span></span> <span data-ttu-id="8c531-150">行の列情報を含むプロパティ値の配列、および_ulflags_パラメーターに0を渡します。</span><span class="sxs-lookup"><span data-stu-id="8c531-150">Pass a property value array that contains the column information for the row and 0 for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8c531-151">セッションの後の方の時点で、プロバイダーの状態が変化し、列情報を更新する必要が生じた場合は、STATUSROW_UPDATE フラグセットを使用して、再度**modifystatusrow**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8c531-151">If at some point later in the session your provider's status changes and it becomes necessary to update the column information, call **ModifyStatusRow** again with the STATUSROW_UPDATE flag set.</span></span> 
    
<span data-ttu-id="8c531-152">状態オブジェクトの詳細については、「 [MAPI status objects](mapi-status-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c531-152">For more information about status objects, see [MAPI Status Objects](mapi-status-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c531-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c531-153">See also</span></span>

- [<span data-ttu-id="8c531-154">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="8c531-154">MAPI Service Providers</span></span>](mapi-service-providers.md)

