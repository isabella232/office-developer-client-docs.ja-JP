---
title: アドレス帳オプションの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c64f84da6bece809176bf67985b6f55ce92414a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803889"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="4422d-103">アドレス帳オプションの設定</span><span class="sxs-lookup"><span data-stu-id="4422d-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="4422d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4422d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4422d-105">アドレス帳を使用するためのオプションについて説明する 3 つのプロパティを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4422d-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="4422d-106">**PR_AB_SEARCH_PATH**([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4422d-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="4422d-107">[IAddrBook::ResolveName](iaddrbook-resolvename.md)で**PR_AB_SEARCH_PATH**プロパティを使用して、名前解決、およびそれらに関連する注文に使用するコンテナーを決定します。</span><span class="sxs-lookup"><span data-stu-id="4422d-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="4422d-108">**PR_AB_SEARCH_PATH**内の各コンテナーには、 **IAddrBook::ResolveName**は、その[IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4422d-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="4422d-109">**PR_AB_SEARCH_PATH**の最後にコンテナーの前に**PR_AB_SEARCH_PATH**の先頭にコンテナーが検索されます。</span><span class="sxs-lookup"><span data-stu-id="4422d-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="4422d-110">[SRowSet](srowset.md)構造体、テーブル内の行を表すために使用するのと同じ構造を使用して、 **PR_AB_SEARCH_PATH**での検索順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="4422d-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="4422d-111">[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)メソッドを呼び出して、現在の検索パスを表示し、 [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出すことによって変更できます。</span><span class="sxs-lookup"><span data-stu-id="4422d-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="4422d-112">**PR_AB_DEFAULT_DIR**([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4422d-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="4422d-113">**PR_AB_DEFAULT_DIR**プロパティは、アドレス帳が表示されるときに最初に表示するアドレス帳コンテナーのエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="4422d-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="4422d-114">ディレクトリの既定の設定は、 [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドを呼び出すことによって変更するまで有効です。</span><span class="sxs-lookup"><span data-stu-id="4422d-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="4422d-115">既定のディレクトリを表示するには、 [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="4422d-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="4422d-116">**PR_AB_DEFAULT_PAB**([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4422d-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="4422d-117">これら 3 つのプロパティは、標準の**IMAPIProp**メソッドを使用してそれらを使用することはできませんので特殊です。</span><span class="sxs-lookup"><span data-stu-id="4422d-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="4422d-118">代わりに、 **IAddrBook**メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4422d-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="4422d-119">これらのプロパティの [なし] を変更するには**IMAPIProp::SetProps**でため、変更を永続的に**IMAPIProp::SaveChanges**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4422d-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="4422d-120">**IAddrBook**の方法で行われた変更は直ちに有効にします。</span><span class="sxs-lookup"><span data-stu-id="4422d-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4422d-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="4422d-121">See also</span></span>



[<span data-ttu-id="4422d-122">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4422d-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

