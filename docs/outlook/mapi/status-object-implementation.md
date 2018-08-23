---
title: ステータス オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 379378f2092f7b119a40ac44cbdcfa03f254b448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804019"
---
# <a name="status-object-implementation"></a><span data-ttu-id="447ce-103">ステータス オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="447ce-103">Status object implementation</span></span>

<span data-ttu-id="447ce-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="447ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="447ce-105">すべてのサービス プロバイダーは、状態オブジェクトを実装し、セッション ・ ステータス ・ テーブルからのプロパティを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="447ce-105">All service providers must implement a status object and furnish properties from it to the session status table.</span></span> <span data-ttu-id="447ce-106">制御するリソースの数によっては、状態テーブルでは、1 つまたは複数の行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="447ce-106">You can include one or more rows in the status table, depending on the number of resources that you control.</span></span> <span data-ttu-id="447ce-107">たとえば、トランスポート プロバイダーは、状態テーブルには、各メッセージ キューの管理行を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="447ce-107">A transport provider, for example, should create a row in the status table for each message queue it manages.</span></span> <span data-ttu-id="447ce-108">を変更した場合は、適切な状態のテーブルの行を更新しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="447ce-108">When changes occur, the appropriate status table row must be updated.</span></span> <span data-ttu-id="447ce-109">状態オブジェクトを実装すると、状態テーブルに含まれている情報およびテーブルに含まれていないその他の情報へのアクセスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="447ce-109">Status objects are implemented to provide access both to the information included in the status table and to additional information not included in the table.</span></span>
  
### <a name="to-implement-a-status-object"></a><span data-ttu-id="447ce-110">状態オブジェクトを実装するには</span><span class="sxs-lookup"><span data-stu-id="447ce-110">To implement a status object</span></span>

1. <span data-ttu-id="447ce-111">ログオン オブジェクトの**OpenStatusEntry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="447ce-111">Implement the **OpenStatusEntry** method of your logon object.</span></span> <span data-ttu-id="447ce-112">クライアントは、状態オブジェクトを開く場合、それらは[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="447ce-112">When clients want to open your status object, they call [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="447ce-113">MAPI は、その状態オブジェクトを開き、その**IMAPIStatus**実装へのポインターをクライアントに返すには、プロバイダーの原因と、プロバイダーの**OpenStatusEntry**メソッドを呼び出すことによって、開く操作の要求を満たします。</span><span class="sxs-lookup"><span data-stu-id="447ce-113">MAPI fulfills the open request by calling your provider's **OpenStatusEntry** method, causing your provider to open its status object and return to the client a pointer to its **IMAPIStatus** implementation.</span></span> <span data-ttu-id="447ce-114">実装では、 **OpenStatusEntry** 、次の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="447ce-114">In your **OpenStatusEntry** implementation, complete the following steps:</span></span> 
    
   1. <span data-ttu-id="447ce-115">ログオン オブジェクトが状態オブジェクトをまだ作成していない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="447ce-115">Perform the following tasks if your logon object has not yet created a status object:</span></span>
    
      1. <span data-ttu-id="447ce-116">プロバイダーのプロファイル セクションにアクセスするためのサポート オブジェクトの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="447ce-116">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your provider's profile section.</span></span> 
          
      2. <span data-ttu-id="447ce-117">新しい状態オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="447ce-117">Create a new status object.</span></span>
          
      3. <span data-ttu-id="447ce-118">プロファイル セクションへの参照をプロバイダーの状態のオブジェクトに格納し、メソッドを呼び出してプロファイル セクションの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)を参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="447ce-118">Store a reference to the profile section in your provider's status object and call the profile section's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count.</span></span> 
          
      4. <span data-ttu-id="447ce-119">ログオン オブジェクトへの参照をプロバイダーの状態のオブジェクトに格納し、参照カウントをインクリメントするのには、ログオン オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="447ce-119">Store a reference to the logon object in your provider's status object and call the logon object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
          
      5. <span data-ttu-id="447ce-120">プロバイダーのログオン オブジェクトでは、状態オブジェクトへの参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="447ce-120">Store a reference to the status object in your provider's logon object.</span></span>
    
   2. <span data-ttu-id="447ce-121">ログオン オブジェクトでは、その参照カウントをインクリメントするのには、状態オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="447ce-121">Call the status object's **IUnknown::AddRef** method to increment its reference count in the logon object.</span></span> 
    
   3. <span data-ttu-id="447ce-122">MAPI_STATUS するには、状態オブジェクトの**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="447ce-122">Set the status object's **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property to MAPI_STATUS.</span></span>
    
   4. <span data-ttu-id="447ce-123">状態のオブジェクト] をポイントして、 _lppMAPIStatus_の出力パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="447ce-123">Set the  _lppMAPIStatus_ output parameter to point to the status object, and return.</span></span> 
    
   5. <span data-ttu-id="447ce-124">_UlFlags_の入力パラメーターをチェックします。</span><span class="sxs-lookup"><span data-stu-id="447ce-124">Check the  _ulFlags_ input parameter.</span></span> <span data-ttu-id="447ce-125">MAPI_MODIFY に設定されている場合は、プロバイダーがその状態のオブジェクトへの読み取り/書き込みアクセスをサポートして、書き込み可能なオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="447ce-125">If it is set to MAPI_MODIFY and your provider supports read/write access to its status object, return a writeable object.</span></span> <span data-ttu-id="447ce-126">ただし、プロバイダーがその状態のオブジェクトへの読み取り/書き込みアクセスをサポートしていない場合は失敗しません。</span><span class="sxs-lookup"><span data-stu-id="447ce-126">However, if your provider does not support read/write access to its status object, do not fail.</span></span> <span data-ttu-id="447ce-127">読み取り専用である状態のオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="447ce-127">Return a status object that is read-only.</span></span> <span data-ttu-id="447ce-128">読み取り/書き込みステータスのオブジェクトを受信することがあるクライアントは、変更する前に、読み取り/書き込み権限が付与されているを確認してください。</span><span class="sxs-lookup"><span data-stu-id="447ce-128">Clients that expect to receive read/write status objects should verify that read/write permission has been granted before attempting to make any changes.</span></span> 
    
2. <span data-ttu-id="447ce-129">すべて必要なステータスのオブジェクトとステータス ・ テーブルのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="447ce-129">Set all of the required status object and status table properties.</span></span> <span data-ttu-id="447ce-130">状態のテーブルの行に含まれるプロパティは、状態のオブジェクトを計算する MAPI プロパティを通じて使用可能なはずです。</span><span class="sxs-lookup"><span data-stu-id="447ce-130">The properties that you include in your status table row should be available through your status object, except for the properties calculated by MAPI.</span></span> <span data-ttu-id="447ce-131">必要なプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="447ce-131">The required properties are as follows:</span></span>
    
   - <span data-ttu-id="447ce-132">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="447ce-133">**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-133">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="447ce-134">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   - <span data-ttu-id="447ce-135">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-135">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>
    
   - <span data-ttu-id="447ce-136">**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-136">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>
    
   - <span data-ttu-id="447ce-137">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-137">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>
    
   - <span data-ttu-id="447ce-138">**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="447ce-138">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>
    
3. <span data-ttu-id="447ce-139">実装、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)は、プロバイダーの適切なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="447ce-139">Implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) methods that are appropriate for your provider.</span></span> <span data-ttu-id="447ce-140">、プロバイダーによっては、 **IMAPIStatus**内のすべての 4 つのメソッドを実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="447ce-140">Depending on your provider, you do not need to implement all of the four methods in **IMAPIStatus**.</span></span> <span data-ttu-id="447ce-141">すべてのプロバイダーのメソッドの読み取り専用バージョンを実装する必要があります、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースと[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="447ce-141">Every provider should implement a read-only version of the methods of the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 

   <span data-ttu-id="447ce-142">トランスポート プロバイダーは、 [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)も実装する必要があり、すべてのプロバイダーは、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="447ce-142">Transport providers should also implement [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md), and all providers should support [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md).</span></span> <span data-ttu-id="447ce-143">[ただし、IMAPIStatus::ChangePassword](imapistatus-changepassword.md)は省略可能、サポートします。</span><span class="sxs-lookup"><span data-stu-id="447ce-143">However, support for [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) is optional.</span></span> <span data-ttu-id="447ce-144">パスワードを必要とし、それらをプログラムで変更できるようにするサービス ・ プロバイダーだけでは、このメソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="447ce-144">Only service providers that require passwords and want to allow users to change them programmatically need to implement this method.</span></span> <span data-ttu-id="447ce-145">サポートしているすべてのメソッドの**PR_RESOURCE_METHODS**プロパティに対応するビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="447ce-145">For every method that you support, set the corresponding bit in the **PR_RESOURCE_METHODS** property.</span></span> <span data-ttu-id="447ce-146">たとえば、 **ValidateState**と**SettingsDialog**をのみサポートする、次の**PR_RESOURCE_METHODS**を設定します。</span><span class="sxs-lookup"><span data-stu-id="447ce-146">For example, if you support **ValidateState** and **SettingsDialog** only, set **PR_RESOURCE_METHODS** to the following:</span></span> 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   <span data-ttu-id="447ce-147">クライアントでは、状態オブジェクトを呼び出す前に**PR_RESOURCE_METHODS**の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="447ce-147">Clients should check the value of **PR_RESOURCE_METHODS** before attempting to call your status object.</span></span> <span data-ttu-id="447ce-148">MAPI_E_NO_SUPPORT を返すことによって、サポートされていないメソッドのいずれかの呼び出しを処理します。</span><span class="sxs-lookup"><span data-stu-id="447ce-148">Handle calls to any of your unsupported methods by returning MAPI_E_NO_SUPPORT.</span></span> 
    
4. <span data-ttu-id="447ce-149">ステータス テーブルに、行または列を追加するのにはログオン時に[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="447ce-149">Call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) during logon to add your row or rows to the status table.</span></span> <span data-ttu-id="447ce-150">行の列情報と_ulFlags_パラメーターに 0 を含むプロパティ値の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="447ce-150">Pass a property value array that contains the column information for the row and 0 for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="447ce-151">セッションの後のある時点で、プロバイダーの状態の変更が必要になります列の情報を更新するのには場合、STATUSROW_UPDATE フラグを設定して**ModifyStatusRow**をもう一度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="447ce-151">If at some point later in the session your provider's status changes and it becomes necessary to update the column information, call **ModifyStatusRow** again with the STATUSROW_UPDATE flag set.</span></span> 
    
<span data-ttu-id="447ce-152">ステータス オブジェクトの詳細については、 [MAPI オブジェクトのステータス](mapi-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="447ce-152">For more information about status objects, see [MAPI Status Objects](mapi-status-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="447ce-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="447ce-153">See also</span></span>

- [<span data-ttu-id="447ce-154">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="447ce-154">MAPI Service Providers</span></span>](mapi-service-providers.md)

