---
title: 複数の Exchange アカウントの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '最終更新日: 2012 年 6 月 25 日'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329654"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="f12f2-103">複数の Exchange アカウントの使用</span><span class="sxs-lookup"><span data-stu-id="f12f2-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="f12f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f12f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f12f2-105">Microsoft Outlook 2010 および Microsoft Outlook 2013 では、複数の Exchange 電子メール アカウントの統合をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f12f2-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="f12f2-106">Outlook 2010 または Outlook 2013 では、ユーザーは 2 つの Exchange アカウントを同一のプロファイルに追加できます。その場合も、Exchange の豊富な機能 (公開されたグローバル アドレス一覧 (GAL)、Exchange の不在時構成、フォルダー共有など) は、そのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="f12f2-106">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange e-mail accounts. In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="f12f2-107">Microsoft Office Outlook 2007 以前の MAPI プロファイルの各セクションに詳しいユーザーは、Exchange の設定 (ユーザー名やサービス名など) が固定の Exchange グローバル プロファイル セクション **pbGlobalProfileSectionGuid** に保存されていることを知っています。</span><span class="sxs-lookup"><span data-stu-id="f12f2-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the e-mail user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**. For more information about the Exchange Global Profile, see How To Open the Global Profile Section. In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the pbGlobalProfileSectionGuid obsolete.</span></span> <span data-ttu-id="f12f2-108">Outlook 2010 および Outlook 2013 では、設定を保存するための専用のプロファイル セクションが、それぞれの Exchange アカウントに必要になるため、**pbGlobalProfileSectionGuid** は使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f12f2-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="f12f2-p103">Outlook 2010 および Outlook 2013 の Exchange 設定は、以前と同様にプロファイルに保存されますが、その設定を格納しているプロファイル セクションにはプロファイルごとに動的に一意識別子が割り当てられます。プロファイルに収められた Exchange 設定の場所は、[PidTagExchangeProfileSectionId 標準プロパティ](pidtagexchangeprofilesectionid-canonical-property.md)に保存されていて、Exchange アカウントのメッセージ サービス プロファイル セクションで確認できます。また、このプロパティは、このアカウントのメッセージ サービスの各プロバイダーに対応するプロファイル セクションでも確認できます。一意識別子は、サーバーには保存されず、プロファイル間で異なるものになります。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="f12f2-p104">Outlook 2010 および Outlook 2013 では、Exchange アカウントを特定する一意識別として **PidTagExchangeProfileSectionId** が使用されます。この目的に使用される場合、この一意識別子は **emsmdbUID** と呼ばれます。MAPI および Outlook の一部の操作では、その操作に使用する Exchange アカウントを指定するために、**emsmdbUID** が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="f12f2-p105">複数の Exchange アカウントをサポートするために、いくつかの新しい関数の呼び出しをコード内で使用する必要があります。**entryID** と、[IMailUser : IMAPIProp](imailuserimapiprop.md) および [IDistList : IMAPIContainer](idistlistimapicontainer.md) の [IAddrBook::OpenEntry](iaddrbook-openentry.md) または [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) を使用する呼び出しがあれば、その呼び出しを次のいずれかに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="f12f2-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="f12f2-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="f12f2-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f12f2-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="f12f2-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="f12f2-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="f12f2-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="f12f2-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="f12f2-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f12f2-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="f12f2-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="f12f2-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="f12f2-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="f12f2-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="f12f2-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f12f2-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="f12f2-128">レガシ サポート</span><span class="sxs-lookup"><span data-stu-id="f12f2-128">Legacy support</span></span>

<span data-ttu-id="f12f2-p106">この新しい **emsmdbUID** セクションが現れる前に作成された MAPI クライアントは、引き続きサポートされます。このようなクライアントは、これまでどおりに以前のグローバル セクション **pbGlobalProfileSectionGuid** を取得します。このプロファイル セクションに対するクエリは、従来のクエリを処理する指定された 1 つの Exchange アカウントにリダイレクトされます。この従来の呼び出しを処理するアカウントは、メッセージ サービス テーブルを調べて、PR_EMSMDB_LEGACY の列を追加することで判断できます。これが true に設定されているメッセージ サービスは 1 つのみであり、そのサービスの **PidTagExchangeProfileSectionId** は従来の **emsmdbUID** と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f12f2-p107">構成可能な MAPI 設定 (既定のストアや既定のアカウントなど) は、どのアカウントが従来の呼び出しを処理するかについて影響しません。従来の呼び出しを処理するアカウントは構成できません。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="f12f2-p108">従来のアカウントの **emsmdbUID** は、Outlook グローバル プロファイル セクションにコピーされます。このプロパティが存在しない場合は、メッセージ サービス テーブルをクエリすることで、どのアカウントがレガシ ハンドラであるかを判断して、その値を Outlook グローバル プロファイル セクションで設定します。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="f12f2-p109">明確に説明すると、Outlook グローバル プロファイル セクションは Exchange グローバル プロファイル セクションとは別のものであり、Outlook 2010 および Outlook 2013 の Exchange グローバル プロファイル セクションは、複数の Exchange アカウントを持てるようになったため、実際にはグローバルではなくなっています。Outlook グローバル プロファイル セクションには、Outlook に関するプロパティ (フォルダー MRU の状態やグローバル接続の状態など) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="f12f2-140">アドレス帳アカウントのコンテキスト</span><span class="sxs-lookup"><span data-stu-id="f12f2-140">Address Book Account Contexts</span></span>

<span data-ttu-id="f12f2-141">複数の Exchange アカウントでアドレスを正しく解決するには、アカウントのコンテキストを取得する新しい関数を使用して、アドレス帳の呼び出しで正しい Exchange アカウントを検索するようにします。</span><span class="sxs-lookup"><span data-stu-id="f12f2-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="f12f2-p110">以前のアドレス帳 API の一部は、複数の Exchange に完全には対応していなかったため使用されなくなりました。通常、このアカウントのコンテキストは **emsmdbUID** になります。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="f12f2-144">この **emsmdbUID** に加えて、複数の Exchange アカウントには **emsabpUID** もあります。</span><span class="sxs-lookup"><span data-stu-id="f12f2-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="f12f2-145">**emsmdbUID** の値では、アカウントのコンテキストを識別します。</span><span class="sxs-lookup"><span data-stu-id="f12f2-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="f12f2-146">**emsabpUID** の値では、Exchange アドレス帳プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="f12f2-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="f12f2-p111">通常、**emsabpUID** の値は受信者を解決するときに使用されます。受信者の解決に [IAddrBook::ResolveName](iaddrbook-resolvename.md) を使用すると、Exchange の受信者行には **PR_AB_PROVIDERS** (0x3D010102) プロパティが格納されます。**emsabpUID** の値は、このプロパティに格納されています。**emsabpUID** の値によって、特定の受信者の Exchange アドレス帳プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="f12f2-150">特定の **emsmdbUID** に対応する **emsabpUID** の値を調べるには、その **emsmdbUID** のプロファイル セクションを開いて、**PR_EMSABP_USER_UID** (0x0x3D1A0102) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f12f2-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="f12f2-p112">[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) を呼び出す場合は、その呼び出しで渡すリスト内の Exchange の受信者に、**PR_AB_PROVIDERS** プロパティが含まれていて、その受信者が属するアドレス帳プロバイダーと一致する **emsabpUID** が保持されていることを確認してください。[IAddrBook::ResolveName](iaddrbook-resolvename.md) から取得した行に対して [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) を呼び出す場合は追加のアクションは不要ですが、一部のコードでは **PR_ENTRYID** プロパティのみが含まれる行に対して [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) を呼び出すことになります。このような状況の行には、**PR_AB_PROVIDERS** プロパティが正しい **emsabpUID** に設定されている **PR_ENTRYID** と **PR_AB_PROVIDERS** の両方が格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="f12f2-154">複数の Exchange アカウントを解決するためのプロセスについて、簡単な説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f12f2-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="f12f2-p113">サービスの一意識別子がある場合は、コードで、その識別子と一致する **PR_SERVICE_UID** プロパティのメッセージ ストアのテーブルを調べます。正しい **PR_MDB_PROVIDER** は、そこで判断できます。この行には、適切なストアが格納されています。</span><span class="sxs-lookup"><span data-stu-id="f12f2-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="f12f2-158">**emsmdbUID** がある場合は、コードで、その **emsmdbUID** と一致する **PidTagExchangeProfileSectionId** を公開している行についてメッセージ サービス テーブルを調べます。</span><span class="sxs-lookup"><span data-stu-id="f12f2-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f12f2-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="f12f2-159">See also</span></span>



[<span data-ttu-id="f12f2-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="f12f2-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="f12f2-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f12f2-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="f12f2-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="f12f2-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="f12f2-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="f12f2-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f12f2-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="f12f2-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f12f2-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="f12f2-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="f12f2-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="f12f2-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="f12f2-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="f12f2-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f12f2-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="f12f2-170">PidTagExchangeProfileSectionId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f12f2-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="f12f2-171">グローバル プロファイル セクションを開く方法</span><span class="sxs-lookup"><span data-stu-id="f12f2-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

