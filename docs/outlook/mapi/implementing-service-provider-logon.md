---
title: サービス プロバイダー ログオンの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eb64f2780530fd30784bf9a9b197bcde205b4a5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800949"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="b1815-103">サービス プロバイダー ログオンの実装</span><span class="sxs-lookup"><span data-stu-id="b1815-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="b1815-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1815-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1815-105">MAPI は、エントリ ポイント関数から返すするポインターを使用してログオン プロセスを開始するのには、プロバイダーのオブジェクトでメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1815-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="b1815-106">方法は異なります、サービス ・ プロバイダーの種類によって次のように。</span><span class="sxs-lookup"><span data-stu-id="b1815-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="b1815-107">アドレス帳プロバイダーの[IABProvider::Logon](iabprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="b1815-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="b1815-108">メッセージ ストア プロバイダーの[IMSProvider::Logon](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="b1815-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="b1815-109">トランスポート プロバイダーの[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)</span><span class="sxs-lookup"><span data-stu-id="b1815-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="b1815-110">ログオン方法を実装するには、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="b1815-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="b1815-111">[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、入力パラメーターとして渡されるサポート オブジェクトの参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="b1815-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="b1815-112">[プロファイル] セクションにアクセスするためのサポート オブジェクトの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1815-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="b1815-113">次のプロパティを設定するのには、プロファイルのセクションの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1815-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="b1815-114">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1815-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="b1815-115">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1815-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="b1815-116">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1815-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="b1815-117">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b1815-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="b1815-118">プロファイル セクションの**PR_RESOURCE_FLAGS**または**PR_PROVIDER_DLL_NAME**のプロパティを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="b1815-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="b1815-119">ログオン時に、これらのプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="b1815-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="b1815-120">プロパティを構成する必要がありますがプロファイルに格納されるか、またはユーザーから利用できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b1815-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="b1815-121">構成の確認の詳細については、[サービス プロバイダーの構成を確認する](verifying-service-provider-configuration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1815-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="b1815-122">プロバイダーがアドレス帳またはメッセージ ストア プロバイダーの場合は、一意の識別子、または[MAPIUID](mapiuid.md)、登録のサポート オブジェクトの[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1815-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="b1815-123">トランスポート プロバイダーは、MAPI は、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すと、 **MAPIUID**構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="b1815-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="b1815-124">の**MAPIUID**を登録の詳細については、[登録するサービス プロバイダー固有の識別子](registering-service-provider-unique-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1815-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="b1815-125">ログオン オブジェクトをインスタンス化し、次の値のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="b1815-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="b1815-126">ログオンが成功を示すために S_OK です。</span><span class="sxs-lookup"><span data-stu-id="b1815-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="b1815-127">構成のプロパティの 1 つ以上を示すために MAPI_E_UNCONFIGURED を使用できませんでした。</span><span class="sxs-lookup"><span data-stu-id="b1815-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="b1815-128">ユーザー キャンセルされたこと [構成] ダイアログ ボックスが使用できない設定のプロパティの原因を示すために MAPI_E_USER_CANCEL。</span><span class="sxs-lookup"><span data-stu-id="b1815-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="b1815-129">プロバイダーを構成できませんでしたが、MAPI に関係なく使用することを許可する必要があることを示すために MAPI_E_FAILONEPROVIDER。</span><span class="sxs-lookup"><span data-stu-id="b1815-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="b1815-130">ログオン方法には、プロバイダーがパスワードが必要ですし、ユーザー インターフェイスが無効であるため、ユーザーに確認ことはできませんなど、致命的でないエラーを報告するには、この値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1815-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="b1815-131">上記のタスクの一覧では、サービス プロバイダーのログオン方法の最低限の実装について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1815-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="b1815-132">必要に応じて、追加の機能を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b1815-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="b1815-133">など、一部のプロバイダーは、そのログオン方法で状態テーブルを更新する[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1815-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b1815-134">ログオン時に最高のパフォーマンスを達成するために[IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)または[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)のいずれかの呼び出しを避けるためです。</span><span class="sxs-lookup"><span data-stu-id="b1815-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="b1815-135">これらの呼び出しが完了し、ログオン メソッドに制御を返すことができます、前に MAPI スプーラーを起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1815-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1815-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1815-136">See also</span></span>

- [<span data-ttu-id="b1815-137">サービス プロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="b1815-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

