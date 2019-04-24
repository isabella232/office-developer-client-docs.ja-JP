---
title: 名前解決の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310081"
---
# <a name="implementing-name-resolution"></a><span data-ttu-id="11a3b-103">名前解決の実装</span><span class="sxs-lookup"><span data-stu-id="11a3b-103">Implementing Name Resolution</span></span>

  
  
<span data-ttu-id="11a3b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11a3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11a3b-105">アドレス帳プロバイダーは、名前解決のサポートを担当します。これには、エントリ識別子と表示名を関連付けるプロセスがあります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-105">Address book providers are responsible for supporting name resolution — the process of associating an entry identifier with a display name.</span></span> <span data-ttu-id="11a3b-106">クライアントは、 [IAddrBook:: ResolveName](iaddrbook-resolvename.md)を呼び出して名前解決を開始し、送信メッセージの受信者リストの各メンバーが有効なアドレスに対応するようにします。</span><span class="sxs-lookup"><span data-stu-id="11a3b-106">Clients initiate name resolution when they call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to ensure that each member of an outgoing message's recipient list corresponds to a valid address.</span></span> 
  
<span data-ttu-id="11a3b-107">プロバイダーは、次の方法で名前解決をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-107">Your provider can support name resolution by:</span></span>
  
- <span data-ttu-id="11a3b-108">**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限のサポート (すべてのアドレス帳コンテナーの要件)。</span><span class="sxs-lookup"><span data-stu-id="11a3b-108">Supporting the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction, a requirement for all address book containers.</span></span>
    
- <span data-ttu-id="11a3b-109">すべてのアドレス帳コンテナーのオプションである[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-109">Implementing the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method, an option for all address book containers.</span></span> 
    
<span data-ttu-id="11a3b-110">**IABContainer:: ResolveNames**をサポートすることを選択した場合は、 _lpadrlist_パラメーターを使用して渡された[adrlist](adrlist.md)構造で、未解決の表示名ごとに正確に一致するものを検索します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-110">If you choose to support **IABContainer::ResolveNames**, attempt to locate an exact match for each unresolved display name in the [ADRLIST](adrlist.md) structure passed in with the  _lpAdrList_ parameter.</span></span> <span data-ttu-id="11a3b-111">未解決の表示名を identifiy することができるのは、 **adrlist**構造の**aentries**メンバーの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティがプロパティ値の配列に含まれていないためです。</span><span class="sxs-lookup"><span data-stu-id="11a3b-111">You can identifiy an unresolved display name because it is missing the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property in the property value array in its **aEntries** member of the **ADRLIST** structure.</span></span> <span data-ttu-id="11a3b-112">0個のプロパティが関連付けられているエントリは無視されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-112">Ignore any entries that have zero properties associated with them.</span></span> 
  
<span data-ttu-id="11a3b-113">_lpflaglist_パラメーターの解決結果を報告します。 _lpadrlist_内の表示名の配列に対応するフラグの配列です。</span><span class="sxs-lookup"><span data-stu-id="11a3b-113">Report the result of your attempt at resolution in the  _lpFlagList_ parameter, an array of flags that corresponds to the array of display names in  _lpAdrList_.</span></span> <span data-ttu-id="11a3b-114">このフラグは、最初のフラグが**adrlist**構造の最初の**aentries**メンバーに対応するように位置指定し、2番目のフラグは2番目の**aentries**メンバーに対応します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-114">The flags are positional such that the first flag corresponds to the first **aEntries** member in the **ADRLIST** structure, the second flag corresponds to the second **aEntries** member, and so on.</span></span> 
  
<span data-ttu-id="11a3b-115">未解決の各エントリに対して、次の3つの結果が考えられます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-115">There are three possible results for each unresolved entry:</span></span>
  
- <span data-ttu-id="11a3b-116">一致が見つかりませんでした。これは、コンテナーエントリ内のエントリが**adrlist**構造体のエントリと一致しないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-116">No match was found, meaning that none of the entries in your container entries match the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="11a3b-117">_lpflaglist_パラメーターの対応するエントリを MAPI_UNRESOLVED に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-117">Set the corresponding entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED.</span></span> 
    
- <span data-ttu-id="11a3b-118">複数の一致がある場合は、 **adrlist**構造のエントリに一致する複数のコンテナーエントリがあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-118">Several matches can be found, meaning that there are multiple container entries that match the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="11a3b-119">_lpflaglist_パラメーターの対応するエントリを MAPI_AMBIGUOUS に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-119">Set the corresponding entry in the  _lpFlagList_ parameter to MAPI_AMBIGUOUS.</span></span> <span data-ttu-id="11a3b-120">**adrlist**構造体のエントリの数を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="11a3b-120">Do not change the number of entries in the **ADRLIST** structure.</span></span> 
    
- <span data-ttu-id="11a3b-121">完全一致を見つけることができます。つまり、 **adrlist**構造体のエントリに一致するコンテナーエントリが1つだけであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-121">An exact match can be found, meaning that there is only one container entry that matches the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="11a3b-122">_lpflaglist_パラメーターの対応するメンバを MAPI_RESOLVED に設定し、 **adrlist**エントリに関連付けられているプロパティの配列にエントリ識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-122">Set the corresponding member in the  _lpFlagList_ parameter to MAPI_RESOLVED and add the entry identifier to the array of properties associated with the **ADRLIST** entry.</span></span> 
    
<span data-ttu-id="11a3b-123">**IABContainer:: ResolveNames**をサポートしない場合は、実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-123">If you choose not to support **IABContainer::ResolveNames**, return MAPI_E_NO_SUPPORT from your implementation.</span></span>
  
<span data-ttu-id="11a3b-124">あいまいな名前解決 ( **PR_ANR**プロパティ制限) をコンテナーのコンテンツテーブルに対してサポートするには、すべてのアドレス帳プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="11a3b-124">All address book providers are required to support ambiguous name resolution — the **PR_ANR** property restriction — on their containers' contents tables.</span></span> <span data-ttu-id="11a3b-125">このサポートを提供するには、お客様のプロバイダーにとって意味のある1つ以上のプロパティと照合して、"最適な推測" の検索を実行して、 [IMAPITable:: Restrict](imapitable-restrict.md)の実装で PR_ANR 制限を処理します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-125">To provide this support, handle the PR_ANR restriction in your implementation of [IMAPITable::Restrict](imapitable-restrict.md) by performing a "best guess" type of search, matching against one or more particular properties that make sense for your provider.</span></span> <span data-ttu-id="11a3b-126">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) など、同じプロパティまたはプロパティを毎回使用したり、管理者が受け入れ可能なプロパティの一覧から選択できるようにしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-126">You can choose to use the same property or properties every time, such as **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) or **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), or allow an administrator to choose from a list of acceptable properties.</span></span> 
  
<span data-ttu-id="11a3b-127">ほとんどのプロバイダーは、独自のコンテンツテーブル実装を提供していますが、 [CreateTable](createtable.md)関数を使用して MAPI で提供される実装をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-127">Although most providers supply their own contents table implementation, you can customize the implementation supplied by MAPI through the [CreateTable](createtable.md) function.</span></span> <span data-ttu-id="11a3b-128">ただし、MAPI 実装はあらゆる種類の制限をサポートしていないため、ラッパーオブジェクトを作成して、呼び出しをインターセプトするカスタマイズされたバージョンの**制限**を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-128">However, because the MAPI implementation does not support restrictions of any kind, you must create a wrapper object to include a customized version of **Restrict** that intercepts the call.</span></span> 
  

