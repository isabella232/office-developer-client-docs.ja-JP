---
title: サービス プロバイダー ログオンの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310088"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="0a5fe-103">サービス プロバイダー ログオンの実装</span><span class="sxs-lookup"><span data-stu-id="0a5fe-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="0a5fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a5fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a5fe-105">MAPI は、プロバイダー オブジェクト内のメソッドを呼び出して、エントリ ポイント関数から返すポインターを使用してログオン プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="0a5fe-106">このメソッドは、サービス プロバイダーの種類に応じて、次のように異なります。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="0a5fe-107">[IABProvider::アドレス帳](iabprovider-logon.md) プロバイダーのログオン</span><span class="sxs-lookup"><span data-stu-id="0a5fe-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="0a5fe-108">[IMSProvider::メッセージ ストア](imsprovider-logon.md) プロバイダーのログオン</span><span class="sxs-lookup"><span data-stu-id="0a5fe-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="0a5fe-109">[IXPProvider::トランスポート](ixpprovider-transportlogon.md) プロバイダーの TransportLogon</span><span class="sxs-lookup"><span data-stu-id="0a5fe-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="0a5fe-110">実装するログオン方法で、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="0a5fe-111">[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、入力パラメーターとして渡されるサポート オブジェクトの参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="0a5fe-112">サポート オブジェクトの [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、プロファイル セクションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="0a5fe-113">プロファイル セクションの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="0a5fe-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a5fe-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="0a5fe-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a5fe-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="0a5fe-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a5fe-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="0a5fe-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a5fe-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="0a5fe-118">プロファイル セクションのプロパティを設定したり、プロパティ **PR_RESOURCE_FLAGS PR_PROVIDER_DLL_NAME** したりしない。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="0a5fe-119">ログオン時に、これらのプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="0a5fe-120">構成に必要なプロパティがプロファイルに格納されている、またはユーザーが使用できるプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="0a5fe-121">構成の確認の詳細については [、「Verifying Service Provider Configuration」を参照してください](verifying-service-provider-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="0a5fe-122">プロバイダーがアドレス帳またはメッセージ ストア プロバイダーである場合は、サポート オブジェクトの [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) メソッドを呼び出して、一意の識別子 [(MAPIUID)](mapiuid.md)を登録します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="0a5fe-123">MAPI が [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出す場合、トランスポート プロバイダーは **MAPIUID** 構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="0a5fe-124">**MAPIUID** の登録の詳細については、「Registering Service [Provider Unique IDENTIFIERs」を参照してください](registering-service-provider-unique-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="0a5fe-125">ログオン オブジェクトをインスタンス化し、次のいずれかの値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="0a5fe-126">S_OK正常にログオンされたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="0a5fe-127">MAPI_E_UNCONFIGURED 1 つ以上の構成プロパティが使用できなかったかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="0a5fe-128">MAPI_E_USER_CANCELが構成ダイアログ ボックスをキャンセルし、構成プロパティが使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="0a5fe-129">MAPI_E_FAILONEPROVIDERプロバイダーを構成できないが、MAPI で使用を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="0a5fe-130">ログオン メソッドは、この値を返して、プロバイダーがパスワードを要求し、ユーザー インターフェイスが無効になっているため、ユーザーにメッセージを表示できない場合など、非fatal エラーを報告する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="0a5fe-131">前のタスクの一覧では、サービス プロバイダーのログオン メソッドの最小実装について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="0a5fe-132">必要に応じて、追加の機能を含めできます。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="0a5fe-133">たとえば、一部のプロバイダーは [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) を呼び出して、ログオン メソッドで状態テーブルを更新します。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0a5fe-134">ログオン時に最高のパフォーマンスを実現するには [、IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) または [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)を呼び出さしないようにします。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="0a5fe-135">これらの呼び出しを完了し、ログオン メソッドに制御を戻す前に、MAPI スプーラーを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a5fe-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a5fe-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a5fe-136">See also</span></span>

- [<span data-ttu-id="0a5fe-137">サービス プロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="0a5fe-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

