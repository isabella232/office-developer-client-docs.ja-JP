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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434705"
---
# <a name="implementing-name-resolution"></a><span data-ttu-id="fd3f5-103">名前解決の実装</span><span class="sxs-lookup"><span data-stu-id="fd3f5-103">Implementing Name Resolution</span></span>

  
  
<span data-ttu-id="fd3f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd3f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd3f5-105">アドレス帳プロバイダーは、名前解決をサポートする責任があります。エントリ識別子を表示名に関連付け処理します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-105">Address book providers are responsible for supporting name resolution — the process of associating an entry identifier with a display name.</span></span> <span data-ttu-id="fd3f5-106">クライアントは [、IAddrBook::ResolveName](iaddrbook-resolvename.md) を呼び出す際に名前解決を開始し、送信メッセージの受信者リストの各メンバーが有効なアドレスに対応します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-106">Clients initiate name resolution when they call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to ensure that each member of an outgoing message's recipient list corresponds to a valid address.</span></span> 
  
<span data-ttu-id="fd3f5-107">プロバイダーは、次の方法で名前解決をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-107">Your provider can support name resolution by:</span></span>
  
- <span data-ttu-id="fd3f5-108">すべてのアドレス **PR_ANR** [(PidTagAnr)](pidtaganr-canonical-property.md)プロパティ制限をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-108">Supporting the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction, a requirement for all address book containers.</span></span>
    
- <span data-ttu-id="fd3f5-109">すべてのアドレス帳 [コンテナーのオプションである IABContainer::ResolveNames](iabcontainer-resolvenames.md) メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-109">Implementing the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method, an option for all address book containers.</span></span> 
    
<span data-ttu-id="fd3f5-110">**IABContainer::ResolveNames** をサポートする場合は _、lpAdrList_ パラメーターと一緒に渡された [ADRLIST](adrlist.md)構造体の未解決の表示名ごとに完全に一致する位置を探します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-110">If you choose to support **IABContainer::ResolveNames**, attempt to locate an exact match for each unresolved display name in the [ADRLIST](adrlist.md) structure passed in with the  _lpAdrList_ parameter.</span></span> <span data-ttu-id="fd3f5-111">**ADRLIST** 構造体の **aEntries** メンバーのプロパティ値配列に **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが存在しないので、未解決の表示名を特定できます。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-111">You can identifiy an unresolved display name because it is missing the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property in the property value array in its **aEntries** member of the **ADRLIST** structure.</span></span> <span data-ttu-id="fd3f5-112">関連付けられたプロパティが 0 のエントリは無視します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-112">Ignore any entries that have zero properties associated with them.</span></span> 
  
<span data-ttu-id="fd3f5-113">_lpFlagList パラメーター (lpAdrList_ の表示名の配列に対応するフラグの配列) で解決を試みる結果 _を報告します_。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-113">Report the result of your attempt at resolution in the  _lpFlagList_ parameter, an array of flags that corresponds to the array of display names in  _lpAdrList_.</span></span> <span data-ttu-id="fd3f5-114">フラグは、最初のフラグが **ADRLIST** 構造体の最初の **aEntries** メンバーに対応し、2 番目のフラグが 2 番目の **aEntries** メンバーに対応する位置です。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-114">The flags are positional such that the first flag corresponds to the first **aEntries** member in the **ADRLIST** structure, the second flag corresponds to the second **aEntries** member, and so on.</span></span> 
  
<span data-ttu-id="fd3f5-115">未解決のエントリごとに、次の 3 つの結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-115">There are three possible results for each unresolved entry:</span></span>
  
- <span data-ttu-id="fd3f5-116">一致が見つかりませんでした。つまり、コンテナー エントリ内のエントリのいずれも ADRLIST 構造内の **エントリと一致** しません。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-116">No match was found, meaning that none of the entries in your container entries match the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="fd3f5-117">_lpFlagList_ パラメーターの対応するエントリを設定して、MAPI_UNRESOLVED。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-117">Set the corresponding entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED.</span></span> 
    
- <span data-ttu-id="fd3f5-118">いくつかの一致が見つかる可能性があります。つまり **、ADRLIST** 構造内のエントリに一致するコンテナー エントリが複数あります。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-118">Several matches can be found, meaning that there are multiple container entries that match the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="fd3f5-119">_lpFlagList_ パラメーターの対応するエントリを設定して、MAPI_AMBIGUOUS。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-119">Set the corresponding entry in the  _lpFlagList_ parameter to MAPI_AMBIGUOUS.</span></span> <span data-ttu-id="fd3f5-120">**ADRLIST** 構造内のエントリの数を変更しない。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-120">Do not change the number of entries in the **ADRLIST** structure.</span></span> 
    
- <span data-ttu-id="fd3f5-121">完全一致を見つけることができます。つまり **、ADRLIST** 構造内のエントリに一致するコンテナー エントリは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-121">An exact match can be found, meaning that there is only one container entry that matches the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="fd3f5-122">_lpFlagList_ パラメーターの対応するメンバーを MAPI_RESOLVED に設定し **、ADRLIST** エントリに関連付けられたプロパティの配列にエントリ識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-122">Set the corresponding member in the  _lpFlagList_ parameter to MAPI_RESOLVED and add the entry identifier to the array of properties associated with the **ADRLIST** entry.</span></span> 
    
<span data-ttu-id="fd3f5-123">**IABContainer::ResolveNames** をサポートしない場合は、実装MAPI_E_NO_SUPPORT返します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-123">If you choose not to support **IABContainer::ResolveNames**, return MAPI_E_NO_SUPPORT from your implementation.</span></span>
  
<span data-ttu-id="fd3f5-124">すべてのアドレス帳プロバイダーは、コンテナーのコンテンツ テーブルのあいまいな名前解決 (PR_ANR **プロパティ制限** ) をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-124">All address book providers are required to support ambiguous name resolution — the **PR_ANR** property restriction — on their containers' contents tables.</span></span> <span data-ttu-id="fd3f5-125">このサポートを提供するには [、IMAPITable::Restrict](imapitable-restrict.md) の実装で PR_ANR 制限を処理し、プロバイダーに適した 1 つ以上の特定のプロパティと照合して、"最適な推測" 型の検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-125">To provide this support, handle the PR_ANR restriction in your implementation of [IMAPITable::Restrict](imapitable-restrict.md) by performing a "best guess" type of search, matching against one or more particular properties that make sense for your provider.</span></span> <span data-ttu-id="fd3f5-126">PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) や **PR_ACCOUNT** ([PidTagAccount)](pidtagaccount-canonical-property.md)など、毎回同じプロパティまたはプロパティを使用するか、管理者が受け入れ可能なプロパティの一覧から選択できます。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-126">You can choose to use the same property or properties every time, such as **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) or **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), or allow an administrator to choose from a list of acceptable properties.</span></span> 
  
<span data-ttu-id="fd3f5-127">ほとんどのプロバイダーは、独自のコンテンツ テーブルの実装を提供しますが [、CreateTable](createtable.md) 関数を使用して MAPI によって提供される実装をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-127">Although most providers supply their own contents table implementation, you can customize the implementation supplied by MAPI through the [CreateTable](createtable.md) function.</span></span> <span data-ttu-id="fd3f5-128">ただし、MAPI 実装はいかなる種類の制限もサポートしていないので、呼び出しを傍受するカスタマイズされたバージョンの **Restrict** を含めるラッパー オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd3f5-128">However, because the MAPI implementation does not support restrictions of any kind, you must create a wrapper object to include a customized version of **Restrict** that intercepts the call.</span></span> 
  

