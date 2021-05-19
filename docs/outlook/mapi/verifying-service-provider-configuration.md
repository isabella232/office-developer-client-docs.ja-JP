---
title: サービス プロバイダー構成の検証
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418849"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="e7260-103">サービス プロバイダー構成の検証</span><span class="sxs-lookup"><span data-stu-id="e7260-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="e7260-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7260-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7260-105">ログオン方法[(IABProvider::Logon、IMSProvider::Logon、](iabprovider-logon.md)[または IXPProvider::TransportLogon)](ixpprovider-transportlogon.md)は、プロバイダーの構成を確認する必要があります。 [](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="e7260-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="e7260-106">これには、完全な操作に必要なすべてのプロパティが正しく設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7260-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="e7260-107">プロバイダーごとに異なる数のプロパティが必要です。構成は、プロバイダーと、許可するユーザー操作の程度によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e7260-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="e7260-108">一部のサービス プロバイダーは、プロファイルに必要なすべてのプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="e7260-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="e7260-109">他のサービス プロバイダーは、プロファイル内のプロパティの部分的なセットを保持し、不足している値をユーザーに求めるメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="e7260-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="e7260-110">それでも他のプロバイダーは、構成に必要なすべての情報を提供するためにユーザーに依存して、プロファイルにプロパティを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7260-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="e7260-111">プロファイルに格納されているプロパティを取得するには</span><span class="sxs-lookup"><span data-stu-id="e7260-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="e7260-112">[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)を呼び出し、プロバイダーの[MAPIUID](mapiuid.md)を入力パラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="e7260-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="e7260-113">プロファイル セクションの [IMAPIProp::GetProps](imapiprop-getprops.md) または [IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドを呼び出して、個々のプロパティまたはプロパティ リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e7260-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="e7260-114">ユーザー情報からプロパティを設定するには</span><span class="sxs-lookup"><span data-stu-id="e7260-114">To set properties from user information</span></span>
  
<span data-ttu-id="e7260-115">MAPI が表示を禁止するフラグを設定していない場合は、プロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="e7260-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="e7260-116">次のフラグは、ユーザー インターフェイスを表示できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="e7260-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="e7260-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e7260-117">**Flag**</span></span>|<span data-ttu-id="e7260-118">**サービス プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="e7260-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7260-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7260-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e7260-120">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7260-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="e7260-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7260-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e7260-122">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7260-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="e7260-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7260-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e7260-124">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7260-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="e7260-125">プロバイダーがプロファイル内のすべての構成プロパティを保存せず、ユーザーの操作が必要で、MAPI がダイアログ ボックスの抑制フラグの 1 つをログオン メソッドに渡す場合は、MAPI_E_UNCONFIGURED を返します。</span><span class="sxs-lookup"><span data-stu-id="e7260-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="e7260-126">ダイアログ抑制フラグが設定されていないが、ユーザーが必要な情報の一部を提供していない場合も、このエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="e7260-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="e7260-127">サービス プロバイダーがログオン メソッドに失敗すると、MAPI_E_UNCONFIGURED MAPI はエントリ ポイント関数を再度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7260-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="e7260-128">2 番目の呼び出しで情報を見つけできない場合は、サービス プロバイダーの重要な内容に応じてセッションが終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e7260-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="e7260-129">次の図は、サービス プロバイダーのログオン方法の構成に必要なロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="e7260-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="e7260-130">**構成検証のフローチャート**</span><span class="sxs-lookup"><span data-stu-id="e7260-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="e7260-131">![構成検証フローチャート](media/amapi_62.gif "構成検証フローチャート")</span><span class="sxs-lookup"><span data-stu-id="e7260-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7260-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7260-132">See also</span></span>

- [<span data-ttu-id="e7260-133">サービス プロバイダー ログオンの実装</span><span class="sxs-lookup"><span data-stu-id="e7260-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

