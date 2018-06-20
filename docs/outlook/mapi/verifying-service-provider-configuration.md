---
title: サービス プロバイダーの構成の確認
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 047a3b99b2d615984252071a1264521a4b2240f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804215"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="c178f-103">サービス プロバイダーの構成の確認</span><span class="sxs-lookup"><span data-stu-id="c178f-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="c178f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c178f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c178f-105">([IABProvider::Logon](iabprovider-logon.md)、 [IMSProvider::Logon](imsprovider-logon.md)、または[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) は、logon メソッドは、プロバイダーの構成を確認してください。</span><span class="sxs-lookup"><span data-stu-id="c178f-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="c178f-106">これには、すべての完全な運用に必要なプロパティが正しく設定されてチェックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c178f-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="c178f-107">すべてのプロバイダーのプロパティ数を変更する必要があります。構成は、プロバイダーとを許可するユーザーの介入の度合いによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c178f-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="c178f-108">サービス プロバイダーによっては、プロファイルに必要なプロパティのすべてをしてください。</span><span class="sxs-lookup"><span data-stu-id="c178f-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="c178f-109">他のサービス プロバイダーでは、プロファイルのプロパティのセットの一部を保持し、欠落している値をユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="c178f-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="c178f-110">他のプロバイダーに格納しないでプロパティ、プロファイル、ユーザーはすべての構成に必要な情報に依存しています。</span><span class="sxs-lookup"><span data-stu-id="c178f-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="c178f-111">プロファイルに格納されているプロパティを取得するには</span><span class="sxs-lookup"><span data-stu-id="c178f-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="c178f-112">[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)、入力パラメーターとして、プロバイダーの[MAPIUID](mapiuid.md)を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c178f-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="c178f-113">個々 のプロパティまたはプロパティの一覧を取得するためにプロファイル セクションの[IMAPIProp::GetProps](imapiprop-getprops.md)または[IMAPIProp::GetPropList](imapiprop-getproplist.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c178f-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="c178f-114">ユーザー情報のプロパティを設定するのには</span><span class="sxs-lookup"><span data-stu-id="c178f-114">To set properties from user information</span></span>
  
<span data-ttu-id="c178f-115">MAPI では、表示を禁止するフラグを設定していない場合、プロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="c178f-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="c178f-116">次のフラグは、ユーザー インターフェイスを表示できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="c178f-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="c178f-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c178f-117">**Flag**</span></span>|<span data-ttu-id="c178f-118">**サービス プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="c178f-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c178f-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c178f-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="c178f-120">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c178f-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="c178f-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c178f-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="c178f-122">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c178f-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="c178f-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c178f-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="c178f-124">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c178f-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="c178f-125">場合は、プロバイダーに保存しません。 すべての構成プロパティ、プロファイル、ユーザーの介入を必要とするし、MAPI ダイアログ ボックスの抑制のフラグのいずれかのログオン方法として、MAPI_E_UNCONFIGURED を返します。</span><span class="sxs-lookup"><span data-stu-id="c178f-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="c178f-126">ダイアログの抑制のフラグが設定されていないが、ユーザーがすべての必要な情報を提供しない場合もこのエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c178f-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="c178f-127">サービス ・ プロバイダーには、MAPI_E_UNCONFIGURED では、そのログオン方法が失敗した場合、MAPI は、エントリ ポイント関数をもう一度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c178f-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="c178f-128">情報を 2 番目の呼び出しを特定できない場合は、サービス プロバイダーの重要度に応じて、そのセッション可能性があります終了します。</span><span class="sxs-lookup"><span data-stu-id="c178f-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="c178f-129">次の図は、サービス プロバイダーのログオン方法の構成に必要なロジックを示します。</span><span class="sxs-lookup"><span data-stu-id="c178f-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="c178f-130">**構成の確認フローチャート**</span><span class="sxs-lookup"><span data-stu-id="c178f-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="c178f-131">![構成の確認フローチャート](media/amapi_62.gif "構成の確認フローチャート")</span><span class="sxs-lookup"><span data-stu-id="c178f-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c178f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c178f-132">See also</span></span>

- [<span data-ttu-id="c178f-133">サービス プロバイダーへのログオンを実装します。</span><span class="sxs-lookup"><span data-stu-id="c178f-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

