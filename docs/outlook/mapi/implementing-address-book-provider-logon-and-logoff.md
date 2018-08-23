---
title: アドレス帳プロバイダーのログオンとログオフの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1ffde0814fe5024a3f89a93462c48136712f1013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800929"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="39902-103">アドレス帳プロバイダーのログオンとログオフの実装</span><span class="sxs-lookup"><span data-stu-id="39902-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="39902-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39902-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39902-105">アドレス帳プロバイダーのメソッドを実装することによってセッションのログオンとログオフをサポートする、 [IABProvider: IUnknown](iabprovideriunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="39902-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="39902-106">* * IABProvider * * インターフェイス**IUnknown**から直接継承し、他の 2 つの方法:**ログオン**と**シャット ダウン**します。</span><span class="sxs-lookup"><span data-stu-id="39902-106">The ** IABProvider ** interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="39902-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="39902-107">Logoff</span></span>

<span data-ttu-id="39902-108">MAPI は、プロバイダーが現在のプロファイルに追加し、クライアントは、動的再構成をサポートしているときに、すべてのセッションの冒頭に、プロバイダーの[IABProvider::Logon](iabprovider-logon.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="39902-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="39902-109">MAPI では、 **IABProvider::Logon**メソッドを呼び出して、アドレス帳プロバイダーは、ログオン プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="39902-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="39902-110">**IABProvider::Log を実装するには**</span><span class="sxs-lookup"><span data-stu-id="39902-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="39902-111">すべての MAPI によって渡される出力パラメーターのポインターを初期化します。</span><span class="sxs-lookup"><span data-stu-id="39902-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="39902-112">サポート オブジェクトの**IUnknown::AddRef**メソッドを呼び出して、参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="39902-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="39902-113">サポート オブジェクトの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロバイダーの構成情報を含むプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="39902-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="39902-114">変更を加える場合は、 _lpUID_パラメーターと MAPI_MODIFY フラグの NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="39902-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="39902-115">プロファイル セクションの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出して、プロバイダーがデータ ファイルまたはデータベース テーブルの名前などのログオンの必要があるプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="39902-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="39902-116">プロパティは、すべて使用可能で有効なことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="39902-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="39902-117">必要に応じて、許可されている場合は、無効なまたは不足している情報への追加や修正を行うし、メソッドを呼び出してプロファイル セクションの[IMAPIProp::SetProps](imapiprop-setprops.md)をすべての変更を保存するように求めるダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="39902-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="39902-118">使用可能にする必要がある一般的なプロパティの一部は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="39902-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="39902-119">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39902-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="39902-120">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39902-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="39902-121">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39902-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="39902-122">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39902-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="39902-123">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) または**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は設定されていません。</span><span class="sxs-lookup"><span data-stu-id="39902-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="39902-124">ログオン時に、これらのプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="39902-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="39902-125">1 つまたは複数の構成のプロパティが利用できない場合は失敗し、MAPI_E_UNCONFIGURED の値を返します。</span><span class="sxs-lookup"><span data-stu-id="39902-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="39902-126">の[MAPIUID](mapiuid.md)を登録するのには[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="39902-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="39902-127">プロバイダーによっては、 **MAPIUID**を作成できます。</span><span class="sxs-lookup"><span data-stu-id="39902-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="39902-128">[IMAPISupport::NewUID](imapisupport-newuid.md)メソッドを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="39902-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="39902-129">UUIDGEN を呼び出しています。EXE ツールを使用して、いずれかのヘッダー ファイルに含めるには、プロバイダーを使用する GUID を定義します。</span><span class="sxs-lookup"><span data-stu-id="39902-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="39902-130">必要な場合を保存**MAPIUID**の新しく作成された現在のプロファイルのプロファイルのセクションを呼び出すことによって * * IMAPIProp::SetProps * * メソッドです。</span><span class="sxs-lookup"><span data-stu-id="39902-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's ** IMAPIProp::SetProps ** method.</span></span> 
    
9. <span data-ttu-id="39902-131">**** メソッドを呼び出すことによってプロファイル セクションをリリースします。</span><span class="sxs-lookup"><span data-stu-id="39902-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="39902-132">新しいログオン オブジェクトをインスタンス化し、この新しいオブジェクトのアドレスに、 _lppABLogon_パラメーターの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="39902-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="39902-133">MAPI 呼び出しの可能性があるため、* * ログオン * * セッション中に何回かメソッド、複数のログオン オブジェクトを作成し、作成される各オブジェクトの追跡を維持することで、実装では、この可能性をサポートすることが賢明です。</span><span class="sxs-lookup"><span data-stu-id="39902-133">Because it is possible for MAPI to call your ** Logon ** method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="39902-134">**ログオン**の複数の呼び出しをサポートにより、クライアント アプリケーションのユーザーなどの異なるアイデンティティまたは使用して、別の配送先とのセッションにログオンします。</span><span class="sxs-lookup"><span data-stu-id="39902-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="39902-135">**シャット ダウン**は、セッションが終了するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="39902-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="39902-136">MAPI メソッドを呼び出して、 [IABProvider::Shutdown](iabprovider-shutdown.md)最後のタスクの 1 つとして、セッションをシャット ダウンに関連します。</span><span class="sxs-lookup"><span data-stu-id="39902-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="39902-137">MAPI は、すべてのプロバイダーのログオン オブジェクトをリリースしましたし、最後の呼び出しを受信することがあると見なすことが、プロバイダーは、この呼び出しを受信するとします。</span><span class="sxs-lookup"><span data-stu-id="39902-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="39902-138">**IABProvider::Shutdown**の実装では、必要と思われる任意の最終的なクリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="39902-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="39902-139">などのセッションであるか、または解放するがまだ設定されているオブジェクトのメソッド**が**実行中にアイドル状態のエンジンを使用するのには**MAPIInitIdle**が呼び出される場合、プロバイダーでは**MAPIDeinitIdle**を呼び出す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39902-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="39902-140">最終的なクリーンアップは、プロバイダーがない場合は、その実装を 1 行のコード変更できます。</span><span class="sxs-lookup"><span data-stu-id="39902-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


