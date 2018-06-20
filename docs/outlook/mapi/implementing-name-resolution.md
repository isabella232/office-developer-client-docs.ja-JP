---
title: 名前解決を実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4d55404149baca07a64b75d460bdfb2a8c541725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800936"
---
# <a name="implementing-name-resolution"></a><span data-ttu-id="05ebd-103">名前解決を実装します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-103">Implementing Name Resolution</span></span>

  
  
<span data-ttu-id="05ebd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05ebd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05ebd-105">アドレス帳プロバイダーは、名前解決をサポートするため、表示名を持つエントリ識別子を関連付けるプロセスです。</span><span class="sxs-lookup"><span data-stu-id="05ebd-105">Address book providers are responsible for supporting name resolution — the process of associating an entry identifier with a display name.</span></span> <span data-ttu-id="05ebd-106">クライアントは、送信メッセージの受信者の一覧の各メンバーが有効なアドレスに対応していることを確認するのには[IAddrBook::ResolveName](iaddrbook-resolvename.md)を呼び出すときに名前解決を開始します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-106">Clients initiate name resolution when they call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to ensure that each member of an outgoing message's recipient list corresponds to a valid address.</span></span> 
  
<span data-ttu-id="05ebd-107">プロバイダーによる名前解決をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="05ebd-107">Your provider can support name resolution by:</span></span>
  
- <span data-ttu-id="05ebd-108">**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限、アドレス帳コンテナーのすべての要件をサポートします。</span><span class="sxs-lookup"><span data-stu-id="05ebd-108">Supporting the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction, a requirement for all address book containers.</span></span>
    
- <span data-ttu-id="05ebd-109">アドレス帳コンテナーのすべてのオプション、 [IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-109">Implementing the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method, an option for all address book containers.</span></span> 
    
<span data-ttu-id="05ebd-110">**IABContainer::ResolveNames**をサポートするために選択した場合は、 _lpAdrList_パラメーターで渡される[ADRLIST](adrlist.md)構造内の未解決名ごとに正確に一致を検索ましょう。</span><span class="sxs-lookup"><span data-stu-id="05ebd-110">If you choose to support **IABContainer::ResolveNames**, attempt to locate an exact match for each unresolved display name in the [ADRLIST](adrlist.md) structure passed in with the  _lpAdrList_ parameter.</span></span> <span data-ttu-id="05ebd-111">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、 **aEntries** 、 **ADRLIST**構造体のプロパティ値の配列ではないためには、identifiy に未解決の表示名を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="05ebd-111">You can identifiy an unresolved display name because it is missing the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property in the property value array in its **aEntries** member of the **ADRLIST** structure.</span></span> <span data-ttu-id="05ebd-112">プロパティが関連付けられているすべてのエントリを無視します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-112">Ignore any entries that have zero properties associated with them.</span></span> 
  
<span data-ttu-id="05ebd-113">_LpAdrList_での表示名の配列に対応するフラグの配列を_lpFlagList_パラメーターでの解像度で、試行の結果を報告します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-113">Report the result of your attempt at resolution in the  _lpFlagList_ parameter, an array of flags that corresponds to the array of display names in  _lpAdrList_.</span></span> <span data-ttu-id="05ebd-114">フラグは、最初のフラグは、 **ADRLIST**構造体の最初の**aEntries**メンバーに対応するように位置、2 番目のフラグは、 **aEntries**の 2 番目のメンバーというように対応します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-114">The flags are positional such that the first flag corresponds to the first **aEntries** member in the **ADRLIST** structure, the second flag corresponds to the second **aEntries** member, and so on.</span></span> 
  
<span data-ttu-id="05ebd-115">未解決のエントリごとに次の 3 つの可能な結果があります。</span><span class="sxs-lookup"><span data-stu-id="05ebd-115">There are three possible results for each unresolved entry:</span></span>
  
- <span data-ttu-id="05ebd-116">一致しませんでした、 **ADRLIST**構造体のエントリをコンテナーのエントリのエントリと一致することを意味します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-116">No match was found, meaning that none of the entries in your container entries match the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="05ebd-117">MAPI_UNRESOLVED に_lpFlagList_パラメーターに対応するエントリを設定します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-117">Set the corresponding entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED.</span></span> 
    
- <span data-ttu-id="05ebd-118">**ADRLIST**構造体のエントリに一致する複数のコンテナーのエントリがあることを意味する、いくつかの項目を確認できます。</span><span class="sxs-lookup"><span data-stu-id="05ebd-118">Several matches can be found, meaning that there are multiple container entries that match the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="05ebd-119">MAPI_AMBIGUOUS に_lpFlagList_パラメーターに対応するエントリを設定します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-119">Set the corresponding entry in the  _lpFlagList_ parameter to MAPI_AMBIGUOUS.</span></span> <span data-ttu-id="05ebd-120">**ADRLIST**構造体のエントリの数は変更されません。</span><span class="sxs-lookup"><span data-stu-id="05ebd-120">Do not change the number of entries in the **ADRLIST** structure.</span></span> 
    
- <span data-ttu-id="05ebd-121">**ADRLIST**構造体のエントリに一致するコンテナーを 1 つだけエントリがあることを意味する、厳密な一致を確認できます。</span><span class="sxs-lookup"><span data-stu-id="05ebd-121">An exact match can be found, meaning that there is only one container entry that matches the entry in the **ADRLIST** structure.</span></span> <span data-ttu-id="05ebd-122">MAPI_RESOLVED に_lpFlagList_パラメーターに対応するメンバーを設定し、 **ADRLIST**エントリに関連付けられているプロパティの配列のエントリの識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-122">Set the corresponding member in the  _lpFlagList_ parameter to MAPI_RESOLVED and add the entry identifier to the array of properties associated with the **ADRLIST** entry.</span></span> 
    
<span data-ttu-id="05ebd-123">**IABContainer::ResolveNames**をサポートしないように選択した場合は、実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-123">If you choose not to support **IABContainer::ResolveNames**, return MAPI_E_NO_SUPPORT from your implementation.</span></span>
  
<span data-ttu-id="05ebd-124">あいまいな名前解決をサポートするために必要なすべてのアドレス帳プロバイダー- **PR_ANR**プロパティの制限-そのコンテナーの内容のテーブルにします。</span><span class="sxs-lookup"><span data-stu-id="05ebd-124">All address book providers are required to support ambiguous name resolution — the **PR_ANR** property restriction — on their containers' contents tables.</span></span> <span data-ttu-id="05ebd-125">このサポートを提供するには、最適な推測の一種で、プロバイダーの意味のある 1 つまたは複数の特定プロパティと一致する、検索を実行することによって[IMAPITable::Restrict](imapitable-restrict.md)の実装では、PR_ANR の制限を処理します。</span><span class="sxs-lookup"><span data-stu-id="05ebd-125">To provide this support, handle the PR_ANR restriction in your implementation of [IMAPITable::Restrict](imapitable-restrict.md) by performing a "best guess" type of search, matching against one or more particular properties that make sense for your provider.</span></span> <span data-ttu-id="05ebd-126">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) や**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) など、毎回同じプロパティまたはプロパティを使用して、許容可能なプロパティの一覧から選択するには管理者の許可を選択できます。</span><span class="sxs-lookup"><span data-stu-id="05ebd-126">You can choose to use the same property or properties every time, such as **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) or **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), or allow an administrator to choose from a list of acceptable properties.</span></span> 
  
<span data-ttu-id="05ebd-127">ほとんどのプロバイダーは、独自の内容のテーブルの実装を提供、 [CreateTable](createtable.md)関数を介して、MAPI によって提供される実装をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="05ebd-127">Although most providers supply their own contents table implementation, you can customize the implementation supplied by MAPI through the [CreateTable](createtable.md) function.</span></span> <span data-ttu-id="05ebd-128">ただし、MAPI 実装がどのような制限をサポートしていないために、呼び出しをインターセプトする**制限**のカスタマイズ バージョンを含むようにラッパー オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05ebd-128">However, because the MAPI implementation does not support restrictions of any kind, you must create a wrapper object to include a customized version of **Restrict** that intercepts the call.</span></span> 
  

