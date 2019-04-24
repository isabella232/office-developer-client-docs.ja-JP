---
title: アドレス帳プロバイダーのログオンとログオフの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332929"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="b59dd-103">アドレス帳プロバイダーのログオンとログオフの実装</span><span class="sxs-lookup"><span data-stu-id="b59dd-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="b59dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b59dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b59dd-105">アドレス帳プロバイダーは、 [IABProvider: IUnknown](iabprovideriunknown.md)インターフェイスのメソッドを実装することによって、セッションのログオンとログオフをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b59dd-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="b59dd-106">\* \* IABProvider \* \* インターフェイスは**IUnknown**から直接継承し、次の2つのメソッドを追加します。**ログオン**と**シャットダウン**。</span><span class="sxs-lookup"><span data-stu-id="b59dd-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="b59dd-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="b59dd-107">Logoff</span></span>

<span data-ttu-id="b59dd-108">MAPI は、プロバイダーの[IABProvider:: Logon](iabprovider-logon.md)メソッドをすべてのセッションの開始時に呼び出し、プロバイダーが現在のプロファイルに追加され、クライアントが動的再構成をサポートするようになります。</span><span class="sxs-lookup"><span data-stu-id="b59dd-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="b59dd-109">MAPI が**IABProvider:: logon**メソッドを呼び出すと、アドレス帳プロバイダーのログオンプロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="b59dd-110">**IABProvider:: Log を実装するには**</span><span class="sxs-lookup"><span data-stu-id="b59dd-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="b59dd-111">MAPI によって渡されたすべての出力パラメータポインターを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="b59dd-112">サポートオブジェクトの**IUnknown:: AddRef**メソッドを呼び出して、参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="b59dd-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="b59dd-113">サポートオブジェクトの[imapisupport:: openprofilesection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロバイダーに関する構成情報を含むプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="b59dd-114">変更を行う予定がある場合は、 _lpuid_パラメーターと MAPI_MODIFY フラグに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="b59dd-115">プロファイルセクションの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、プロバイダーがログオンに必要とするプロパティ (データファイルやデータベーステーブルの名前など) を取得します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="b59dd-116">プロパティがすべて使用可能で有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b59dd-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="b59dd-117">必要であり、許可されている場合は、ユーザーに無効な情報や不足している情報を修正または追加するように求めるダイアログボックスを表示し、プロファイルセクションの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="b59dd-118">利用できるようにする必要がある一般的なプロパティのいくつかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="b59dd-119">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b59dd-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="b59dd-120">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b59dd-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="b59dd-121">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b59dd-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="b59dd-122">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b59dd-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="b59dd-123">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) または**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) を設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="b59dd-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="b59dd-124">ログオン時に、これらのプロパティは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="b59dd-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="b59dd-125">1つ以上の構成プロパティが使用できない場合は、エラーが発生し、MAPI_E_UNCONFIGURED 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="b59dd-126">[MAPIUID](mapiuid.md)を登録するには、呼び出し[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="b59dd-127">プロバイダーは、次の方法で**MAPIUID**を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="b59dd-128">[imapisupport:: newuid](imapisupport-newuid.md)メソッドを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="b59dd-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="b59dd-129">UUIDGEN を呼び出しています。EXE ツールを使用して、プロバイダーがヘッダーファイルの1つに含める GUID を定義します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="b59dd-130">必要に応じて、プロファイルセクションの \* \* imapiprop:: setprops \* \* メソッドを呼び出して、新しく作成した**MAPIUID**を現在のプロファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="b59dd-131">**IUnknown:: release**メソッドを呼び出して、プロファイルセクションを解放します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="b59dd-132">新しいログオンオブジェクトをインスタンス化し、 _lppablogon_パラメーターの内容をこの新しいオブジェクトのアドレスに設定します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="b59dd-133">セッション中に MAPI が \* \* Logon \* \* メソッドを何度も呼び出すことができるため、複数のログオンオブジェクトを作成し、作成された各オブジェクトを追跡できるように、実装でこの可能性をサポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b59dd-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="b59dd-134">複数の**ログオン**呼び出しをサポートすることにより、クライアントアプリケーションのユーザーは、異なる id を使用してセッションにログオンしたり、別の配信先を使用したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="b59dd-135">**Shutdown**は、セッションが終了するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="b59dd-136">MAPI は、セッションのシャットダウンに関連する最後のタスクの1つとして[IABProvider:: Shutdown](iabprovider-shutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="b59dd-137">MAPI では、プロバイダーのすべてのログオンオブジェクトが解放され、プロバイダーがこの呼び出しを受信するときに、これが最後に受信する呼び出しであると想定できます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="b59dd-138">**IABProvider:: Shutdown**の実装で、必要と思われる最終的なクリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="b59dd-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="b59dd-139">たとえば、プロバイダーが**MAPIInitIdle**を呼び出し、セッション中にアイドル状態のエンジンを使用する場合、またはまだ解放されていないオブジェクトの**IUnknown:: Release**メソッドを呼び出した場合、 **MAPIDeinitIdle**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="b59dd-140">プロバイダーが最終的なクリーンアップを行わない場合は、次の1行のコードでその実装を構成できます。</span><span class="sxs-lookup"><span data-stu-id="b59dd-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


