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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438737"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="956ac-103">アドレス帳プロバイダーのログオンとログオフの実装</span><span class="sxs-lookup"><span data-stu-id="956ac-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="956ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="956ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="956ac-105">アドレス帳プロバイダーは [、IABProvider : IUnknown](iabprovideriunknown.md) インターフェイスのメソッドを実装することで、セッション のログオンとログオフをサポートします。</span><span class="sxs-lookup"><span data-stu-id="956ac-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="956ac-106">\*\* IABProvider \*\* インターフェイスは **IUnknown** から直接継承し、ログオンとシャットダウンの 2 つのメソッド **のみを** 追加 **します**。</span><span class="sxs-lookup"><span data-stu-id="956ac-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="956ac-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="956ac-107">Logoff</span></span>

<span data-ttu-id="956ac-108">MAPI は、すべてのセッションの開始時に、プロバイダーが現在のプロファイルに追加され、クライアントが動的再構成をサポートするたびに、プロバイダーの [IABProvider::Logon](iabprovider-logon.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="956ac-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="956ac-109">MAPI が **IABProvider::Logon** メソッドを呼び出す場合、アドレス帳プロバイダーはログオン プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="956ac-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="956ac-110">**IABProvider を実装するには::Log**</span><span class="sxs-lookup"><span data-stu-id="956ac-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="956ac-111">MAPI で渡された出力パラメーター ポインターのすべてを初期化します。</span><span class="sxs-lookup"><span data-stu-id="956ac-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="956ac-112">サポート オブジェクトの **IUnknown::AddRef** メソッドを呼び出して、参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="956ac-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="956ac-113">サポート オブジェクトの [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、プロバイダーに関する構成情報を含むプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="956ac-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="956ac-114">変更を行う  _場合は、lpUID_ パラメーター MAPI_MODIFYフラグに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="956ac-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="956ac-115">プロファイル セクションの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、データ ファイルやデータベース テーブルの名前など、プロバイダーがログオンに必要なプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="956ac-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="956ac-116">すべてのプロパティが使用可能で有効なプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="956ac-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="956ac-117">必要に応じて許可されている場合は、ダイアログ ボックスを表示して、無効または不足している情報に修正または追加を行い、プロファイル セクションの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、変更を保存するようにユーザーに求めるメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="956ac-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="956ac-118">使用できる一般的なプロパティには、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="956ac-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="956ac-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="956ac-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="956ac-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="956ac-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="956ac-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="956ac-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="956ac-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="956ac-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="956ac-123">[PidTagResourceFlags](pidtagresourceflags-canonical-property.md) **)** または PR_RESOURCE_FLAGS ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))**をPR_PROVIDER_DLL_NAME** 設定しない。</span><span class="sxs-lookup"><span data-stu-id="956ac-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="956ac-124">ログオン時に、これらのプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="956ac-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="956ac-125">1 つ以上の構成プロパティが使用できない場合は、エラーが発生し、その値をMAPI_E_UNCONFIGURED。</span><span class="sxs-lookup"><span data-stu-id="956ac-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="956ac-126">[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を呼び出して[MAPIUID を登録します](mapiuid.md)。</span><span class="sxs-lookup"><span data-stu-id="956ac-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="956ac-127">プロバイダーは、次の **方法で MAPIUID を作成** できます。</span><span class="sxs-lookup"><span data-stu-id="956ac-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="956ac-128">[IMAPISupport::NewUID メソッドを呼び出](imapisupport-newuid.md)します。</span><span class="sxs-lookup"><span data-stu-id="956ac-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="956ac-129">プロバイダーがUUIDGEN.EXEファイルに含める GUID を定義するために、このツールを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="956ac-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="956ac-130">必要に応じて、プロファイル セクションの \*\* IMAPIProp::SetProps \*\* メソッドを呼び出して、新しく作成した **MAPIUID** を現在のプロファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="956ac-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="956ac-131">プロファイル セクションを解放するには **、IUnknown::Release メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="956ac-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="956ac-132">新しいログオン オブジェクトをインスタンス化し  _、lppABLogon_ パラメーターの内容をこの新しいオブジェクトのアドレスに設定します。</span><span class="sxs-lookup"><span data-stu-id="956ac-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="956ac-133">MAPI はセッション中に \*\* Logon \*\* メソッドを複数回呼び出す可能性があるから、複数のログオン オブジェクトを作成し、作成された各オブジェクトを追跡することで、実装でこの可能性をサポートする方が賢明です。</span><span class="sxs-lookup"><span data-stu-id="956ac-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="956ac-134">複数の **ログオン呼び** 出しをサポートすると、クライアント アプリケーションのユーザーは、たとえば、異なる ID を持つセッションにログオンしたり、異なる配信先を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="956ac-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="956ac-135">**セッション** の終了時にシャットダウンが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="956ac-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="956ac-136">MAPI は、セッションのシャットダウンに関連する最後のタスクの 1 つとして [、IABProvider::Shutdown](iabprovider-shutdown.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="956ac-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="956ac-137">MAPI は、プロバイダーのすべてのログオン オブジェクトを解放し、プロバイダーがこの呼び出しを受信すると、これが最後に受信する呼び出しと見なす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="956ac-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="956ac-138">**IABProvider::Shutdown** の実装では、必要と思う最終クリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="956ac-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="956ac-139">たとえば、セッション中にアイドル エンジンを使用するために **MAPIInitIdle** を呼び出した場合、プロバイダーは **MAPIDeinitIdle** を呼び出したり、まだリリースされていないオブジェクトの **IUnknown::Release** メソッドを呼び出したりします。</span><span class="sxs-lookup"><span data-stu-id="956ac-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="956ac-140">プロバイダーに最終的なクリーンアップがない場合、その実装は 1 行のコードで構成できます。</span><span class="sxs-lookup"><span data-stu-id="956ac-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


