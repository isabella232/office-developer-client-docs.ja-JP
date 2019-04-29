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
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="e9fe1-103">サービス プロバイダー構成の検証</span><span class="sxs-lookup"><span data-stu-id="e9fe1-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="e9fe1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9fe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9fe1-105">ログオン方法 ([IABProvider:: logon](iabprovider-logon.md)、 [IMSProvider:: logon](imsprovider-logon.md)、または[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)) は、プロバイダーの構成を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="e9fe1-106">これには、完全な操作に必要なすべてのプロパティが正しく設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="e9fe1-107">すべてのプロバイダーは、異なる数のプロパティを必要とします。構成は、プロバイダーと、許可するユーザー操作の程度によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="e9fe1-108">一部のサービスプロバイダーは、必要なすべてのプロパティをプロファイルに保持します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="e9fe1-109">その他のサービスプロバイダーは、プロファイルにプロパティの一部のセットを保持し、ユーザーに不足している値を要求します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="e9fe1-110">それでも、他のプロバイダーはプロファイルにプロパティを保存しません。また、構成に必要なすべての情報をユーザーが指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="e9fe1-111">プロファイルに格納されているプロパティを取得するには</span><span class="sxs-lookup"><span data-stu-id="e9fe1-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="e9fe1-112">[MAPIUID](mapiuid.md)を入力パラメーターとして渡して、 [imapisupport:: openプロファイル](imapisupport-openprofilesection.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="e9fe1-113">プロファイルセクションの[imapiprop:: GetProps](imapiprop-getprops.md)または[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出して、個々のプロパティまたはプロパティリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="e9fe1-114">ユーザー情報からプロパティを設定するには</span><span class="sxs-lookup"><span data-stu-id="e9fe1-114">To set properties from user information</span></span>
  
<span data-ttu-id="e9fe1-115">MAPI が表示の禁止フラグを設定していない場合は、プロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="e9fe1-116">次のフラグは、ユーザーインターフェイスを表示できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="e9fe1-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e9fe1-117">**Flag**</span></span>|<span data-ttu-id="e9fe1-118">**サービスプロバイダー**</span><span class="sxs-lookup"><span data-stu-id="e9fe1-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9fe1-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e9fe1-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e9fe1-120">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9fe1-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="e9fe1-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e9fe1-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e9fe1-122">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9fe1-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="e9fe1-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e9fe1-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e9fe1-124">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9fe1-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="e9fe1-125">プロバイダーがプロファイルにすべての構成プロパティを格納せず、ユーザーの操作を必要とし、MAPI がログオン方法にダイアログボックス抑制フラグの1つを渡す場合は、MAPI_E_UNCONFIGURED を返します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="e9fe1-126">ダイアログ抑制フラグが設定されていないが、ユーザーが必要な情報をすべて指定していない場合にも、このエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="e9fe1-127">サービスプロバイダーが MAPI_E_UNCONFIGURED を使用してログオン方法に失敗すると、MAPI はエントリポイント関数を再度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="e9fe1-128">2番目の呼び出しで情報が見つからない場合は、サービスプロバイダーの重要度によってはセッションが終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="e9fe1-129">次の図は、サービスプロバイダーのログオン方法での構成に必要なロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="e9fe1-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="e9fe1-130">**構成検証のフローチャート**</span><span class="sxs-lookup"><span data-stu-id="e9fe1-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="e9fe1-131">![構成検証のフローチャート](media/amapi_62.gif "構成検証のフローチャート")</span><span class="sxs-lookup"><span data-stu-id="e9fe1-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9fe1-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9fe1-132">See also</span></span>

- [<span data-ttu-id="e9fe1-133">サービスプロバイダーログオンの実装</span><span class="sxs-lookup"><span data-stu-id="e9fe1-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

