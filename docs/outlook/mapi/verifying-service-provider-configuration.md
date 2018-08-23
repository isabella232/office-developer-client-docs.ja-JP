---
title: サービス プロバイダーの構成の確認
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589638"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="e3c13-103">サービス プロバイダーの構成の確認</span><span class="sxs-lookup"><span data-stu-id="e3c13-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="e3c13-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3c13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3c13-105">([IABProvider::Logon](iabprovider-logon.md)、 [IMSProvider::Logon](imsprovider-logon.md)、または[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) は、logon メソッドは、プロバイダーの構成を確認してください。</span><span class="sxs-lookup"><span data-stu-id="e3c13-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="e3c13-106">これには、すべての完全な運用に必要なプロパティが正しく設定されてチェックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3c13-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="e3c13-107">すべてのプロバイダーのプロパティ数を変更する必要があります。構成は、プロバイダーとを許可するユーザーの介入の度合いによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e3c13-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="e3c13-108">サービス プロバイダーによっては、プロファイルに必要なプロパティのすべてをしてください。</span><span class="sxs-lookup"><span data-stu-id="e3c13-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="e3c13-109">他のサービス プロバイダーでは、プロファイルのプロパティのセットの一部を保持し、欠落している値をユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="e3c13-110">他のプロバイダーに格納しないでプロパティ、プロファイル、ユーザーはすべての構成に必要な情報に依存しています。</span><span class="sxs-lookup"><span data-stu-id="e3c13-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="e3c13-111">プロファイルに格納されているプロパティを取得するには</span><span class="sxs-lookup"><span data-stu-id="e3c13-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="e3c13-112">[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)、入力パラメーターとして、プロバイダーの[MAPIUID](mapiuid.md)を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="e3c13-113">個々 のプロパティまたはプロパティの一覧を取得するためにプロファイル セクションの[IMAPIProp::GetProps](imapiprop-getprops.md)または[IMAPIProp::GetPropList](imapiprop-getproplist.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="e3c13-114">ユーザー情報のプロパティを設定するのには</span><span class="sxs-lookup"><span data-stu-id="e3c13-114">To set properties from user information</span></span>
  
<span data-ttu-id="e3c13-115">MAPI では、表示を禁止するフラグを設定していない場合、プロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="e3c13-116">次のフラグは、ユーザー インターフェイスを表示できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="e3c13-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e3c13-117">**Flag**</span></span>|<span data-ttu-id="e3c13-118">**サービス プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="e3c13-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3c13-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e3c13-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e3c13-120">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e3c13-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="e3c13-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e3c13-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e3c13-122">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e3c13-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="e3c13-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e3c13-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e3c13-124">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e3c13-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="e3c13-125">場合は、プロバイダーに保存しません。 すべての構成プロパティ、プロファイル、ユーザーの介入を必要とするし、MAPI ダイアログ ボックスの抑制のフラグのいずれかのログオン方法として、MAPI_E_UNCONFIGURED を返します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="e3c13-126">ダイアログの抑制のフラグが設定されていないが、ユーザーがすべての必要な情報を提供しない場合もこのエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="e3c13-127">サービス ・ プロバイダーには、MAPI_E_UNCONFIGURED では、そのログオン方法が失敗した場合、MAPI は、エントリ ポイント関数をもう一度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="e3c13-128">情報を 2 番目の呼び出しを特定できない場合は、サービス プロバイダーの重要度に応じて、そのセッション可能性があります終了します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="e3c13-129">次の図は、サービス プロバイダーのログオン方法の構成に必要なロジックを示します。</span><span class="sxs-lookup"><span data-stu-id="e3c13-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="e3c13-130">**構成検証のフローチャート**</span><span class="sxs-lookup"><span data-stu-id="e3c13-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="e3c13-131">![構成の確認フローチャート](media/amapi_62.gif "構成の確認フローチャート")</span><span class="sxs-lookup"><span data-stu-id="e3c13-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3c13-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3c13-132">See also</span></span>

- [<span data-ttu-id="e3c13-133">サービス プロバイダー ログオンの実装</span><span class="sxs-lookup"><span data-stu-id="e3c13-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

