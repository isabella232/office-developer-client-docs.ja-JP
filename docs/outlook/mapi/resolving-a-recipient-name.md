---
title: 受信者名の解決
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803761"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="b53e8-103">受信者名の解決</span><span class="sxs-lookup"><span data-stu-id="b53e8-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="b53e8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b53e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b53e8-105">メッセージが処理されると、ときに、各受信者に関連するプロパティを持つ受信者のリストが組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="b53e8-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="b53e8-106">メッセージが送信されるまでに、長期のエントリ id を受信者のこれらのプロパティのいずれかの必要があります。</span><span class="sxs-lookup"><span data-stu-id="b53e8-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="b53e8-107">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティが各受信者に含まれていることを確認するには、受信者リストは、 [IAddrBook への呼び出し内のパラメーターに_lpAdrList_の内容を記述する[ADRLIST](adrlist.md)構造体を渡します。ResolveName](iaddrbook-resolvename.md)。</span><span class="sxs-lookup"><span data-stu-id="b53e8-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="b53e8-108">**ResolveName** **SPropValue**の対応する[ADRENTRY](adrentry.md)構造体の内のエントリの識別子が存在することが示されているように、既に解決された**ADRLIST**構造体のエントリを無視することで処理を開始します。配列です。</span><span class="sxs-lookup"><span data-stu-id="b53e8-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="b53e8-109">次に、 **ResolveName**は、2 種類の受信者に 1 回限りのエントリ id を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b53e8-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="b53e8-110">インターネット アドレスとして書式設定されたアドレスを持つ受信者</span><span class="sxs-lookup"><span data-stu-id="b53e8-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="b53e8-111">受信者アドレスの形式次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b53e8-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="b53e8-112">残りのすべてのエントリの**ResolveName**の表示名に正確に一致するアドレス帳が検索されます。</span><span class="sxs-lookup"><span data-stu-id="b53e8-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="b53e8-113">**ResolveName**では、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティを使用して、一連のコンテナーを検索し、検索順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="b53e8-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="b53e8-114">MAPI は、すべての名前を解決しようとするすべてのコンテナーの[IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b53e8-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="b53e8-115">コンテナーによってはサポートしていないため**ResolveNames**コンテナーには、MAPI_E_NO_SUPPORT が返された場合、MAPI には、その内容のテーブルに対して**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="b53e8-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="b53e8-116">すべてのアドレス帳コンテナーは、この制限を名前解決をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b53e8-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="b53e8-117">すべての名前が解決した後はそれ以上のコンテナーの呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="b53e8-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="b53e8-118">すべてのコンテナーが呼び出されると、あいまいな、または未解決の名前が残る場合は、MAPI では、残りの名前を解決するのにはユーザーに確認するの可能な場合にダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b53e8-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="b53e8-119">**PR_ANR**制限では、 **ADRLIST**構造体での表示名に対して**PR_ANR**プロパティの値と一致します。</span><span class="sxs-lookup"><span data-stu-id="b53e8-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="b53e8-120">**PR_ANR**プロパティの制限を持つコンテナーの内容のテーブルのビューを制限すると、「最適な推測」プロバイダーの意味のあるプロパティと一致する、検索の種類を実行するアドレス帳プロバイダーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b53e8-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="b53e8-121">などの 1 つのアドレス帳プロバイダー可能性があります常に名と一致**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に対しては、受信者の一覧でプロパティを選択するには管理者は、別可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b53e8-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="b53e8-122">**アドレス帳コンテナーの内容のテーブルで PR_ANR プロパティの制限を設定するのには**</span><span class="sxs-lookup"><span data-stu-id="b53e8-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="b53e8-123">次のコードに示すように[SRestriction](srestriction.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="b53e8-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="b53e8-124">内容**SRestriction**構造体を_lpRestriction_パラメーターとして渡して、テーブルの[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b53e8-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

