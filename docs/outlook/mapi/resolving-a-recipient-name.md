---
title: 受信者名の解決
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328673"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="2b4c9-103">受信者名の解決</span><span class="sxs-lookup"><span data-stu-id="2b4c9-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="2b4c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b4c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b4c9-105">メッセージがアドレス指定されると、受信者リストは各受信者に関連するプロパティを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="2b4c9-106">メッセージが送信されるときに、これらのプロパティの1つは、受信者の長い用語のエントリ id である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="2b4c9-107">各受信者に**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれていることを確認するには、受信者の一覧について説明する[adrlist](adrlist.md)構造を IAddrBook:: の呼び出しの_lpadrlist_パラメーターの内容に渡します。 [ResolveName](iaddrbook-resolvename.md)。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="2b4c9-108">**ResolveName**は、既に解決されている**adrlist**構造のエントリを無視することによって処理を開始します。これは、対応する[adrlist](adrentry.md)構造の**spropvalue**にエントリ識別子が存在することによって示されます。配列.</span><span class="sxs-lookup"><span data-stu-id="2b4c9-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="2b4c9-109">次に、 **ResolveName**は、1回限りのエントリ識別子を2種類の受信者に自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="2b4c9-110">アドレスがインターネットアドレスとして書式設定された受信者</span><span class="sxs-lookup"><span data-stu-id="2b4c9-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="2b4c9-111">アドレスが次の形式に設定されている受信者。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="2b4c9-112">残りのすべてのエントリについて、 **ResolveName**は、表示名の完全一致のアドレス帳を検索します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="2b4c9-113">**ResolveName**は、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティを使用して、検索するコンテナーのセットと検索順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="2b4c9-114">MAPI は、すべてのコンテナーの[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出して、すべての名前の解決を試みます。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="2b4c9-115">一部のコンテナーは**ResolveNames**をサポートしていないため、コンテナーが MAPI_E_NO_SUPPORT を返す場合、MAPI は、そのコンテンツテーブルに対して**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="2b4c9-116">この制限を使用して名前解決をサポートするには、すべてのアドレス帳コンテナーが必要です。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="2b4c9-117">すべての名前が解決されると、それ以降のコンテナー呼び出しは行われません。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="2b4c9-118">すべてのコンテナーが呼び出されたが、あいまいまたは未解決の名前が残っている場合は、ユーザーに残りの名前の解決を求めるメッセージが表示される場合は、MAPI がダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="2b4c9-119">**PR_ANR**制限は、 **adrlist**構造の表示名に対する**PR_ANR**プロパティの値と一致します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="2b4c9-120">**PR_ANR**プロパティ制限を使用してコンテナーの contents テーブルの表示を制限すると、アドレス帳プロバイダーは、プロバイダーにとって意味のあるプロパティに一致する検索の種類として "最適な推測" を実行することになります。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="2b4c9-121">たとえば、1つのアドレス帳プロバイダーは、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に対して受信者リスト内の名前と一致する場合がありますが、管理者はこのプロパティを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="2b4c9-122">**アドレス帳コンテナーの contents テーブルに PR_ANR プロパティ制限を設定するには**</span><span class="sxs-lookup"><span data-stu-id="2b4c9-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="2b4c9-123">次のコードに示すように、 [srestriction](srestriction.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="2b4c9-124">コンテンツテーブルの[IMAPITable:: Restrict](imapitable-restrict.md)メソッドを呼び出し、 **srestriction**構造を_lpRestriction_パラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="2b4c9-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

