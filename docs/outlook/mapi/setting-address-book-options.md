---
title: アドレス帳のオプションの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417344"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="51553-103">アドレス帳のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="51553-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="51553-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51553-105">次の3つのプロパティを設定して、アドレス帳を使用するためのオプションを記述できます。</span><span class="sxs-lookup"><span data-stu-id="51553-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="51553-106">**PR_AB_SEARCH_PATH**([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51553-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="51553-107">**PR_AB_SEARCH_PATH**プロパティは[IAddrBook:: ResolveName](iaddrbook-resolvename.md)によって使用され、名前の解決に関係するコンテナーと、それらが関与する必要のある順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="51553-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="51553-108">**PR_AB_SEARCH_PATH**の各コンテナーで、 **IAddrBook:: ResolveName**は[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51553-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="51553-109">**PR_AB_SEARCH_PATH**の先頭にあるコンテナーは、 **PR_AB_SEARCH_PATH**の末尾にあるコンテナーの前に検索されます。</span><span class="sxs-lookup"><span data-stu-id="51553-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="51553-110">**PR_AB_SEARCH_PATH**の検索順序は、テーブル内の行を表すために使用されるものと同じ構造を使用して、 [srowset](srowset.md)構造を使用して指定されます。</span><span class="sxs-lookup"><span data-stu-id="51553-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="51553-111">現在の検索パスを表示するには、 [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md)メソッドを呼び出し、 [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出して変更します。</span><span class="sxs-lookup"><span data-stu-id="51553-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="51553-112">**PR_AB_DEFAULT_DIR**([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51553-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="51553-113">**PR_AB_DEFAULT_DIR**プロパティは、アドレス帳が表示されるときに最初に表示されるアドレス帳コンテナーのエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="51553-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="51553-114">既定のディレクトリ設定は、 [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドを呼び出して変更するまで有効です。</span><span class="sxs-lookup"><span data-stu-id="51553-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="51553-115">[IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md)メソッドを呼び出すことで、既定のディレクトリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="51553-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="51553-116">**PR_AB_DEFAULT_PAB**([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51553-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="51553-117">これら3つのプロパティは、標準の**imapiprop**メソッドを使用して操作できないため、特別なものになります。</span><span class="sxs-lookup"><span data-stu-id="51553-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="51553-118">代わりに、 **IAddrBook**メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51553-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="51553-119">これらのプロパティは、 **imapiprop:: setprops**で変更できないため、変更を永続的にするために**imapiprop:: SaveChanges**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="51553-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="51553-120">**IAddrBook**メソッドを使用して加えた変更は、直ちに有効になります。</span><span class="sxs-lookup"><span data-stu-id="51553-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51553-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="51553-121">See also</span></span>



[<span data-ttu-id="51553-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51553-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

