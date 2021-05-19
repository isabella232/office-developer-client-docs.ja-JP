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
# <a name="setting-address-book-options"></a><span data-ttu-id="93505-103">アドレス帳のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="93505-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="93505-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93505-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93505-105">アドレス帳を使用するためのオプションを説明する 3 つのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="93505-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="93505-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="93505-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="93505-107">PR_AB_SEARCH_PATH **プロパティ** は [、IAddrBook::ResolveName](iaddrbook-resolvename.md) を使用して、名前解決に関与するコンテナーと、それに関係する順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="93505-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="93505-108">**IAddrBook::ResolveName** **は**、PR_AB_SEARCH_PATH内の各コンテナーについて [、IABContainer::ResolveNames メソッドを呼び出](iabcontainer-resolvenames.md)します。</span><span class="sxs-lookup"><span data-stu-id="93505-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="93505-109">コンテナーは、PR_AB_SEARCH_PATHの **末尾** にあるコンテナーの前に検索 **PR_AB_SEARCH_PATH。**</span><span class="sxs-lookup"><span data-stu-id="93505-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="93505-110">テーブル内 **の行PR_AB_SEARCH_PATH** 表すのと同じ構造である [SRowSet](srowset.md) 構造体を使用して、検索順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="93505-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="93505-111">現在の検索パスを表示するには [、IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) メソッドを呼び出し [、IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) メソッドを呼び出して変更します。</span><span class="sxs-lookup"><span data-stu-id="93505-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="93505-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="93505-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="93505-113">PR_AB_DEFAULT_DIR **プロパティ** は、アドレス帳の表示時に最初に表示されるアドレス帳コンテナーのエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="93505-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="93505-114">既定のディレクトリ設定は [、IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) メソッドを呼び出して変更するまで有効です。</span><span class="sxs-lookup"><span data-stu-id="93505-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="93505-115">既定のディレクトリを表示するには [、IAddrBook::GetDefaultDir メソッドを呼び出](iaddrbook-getdefaultdir.md) します。</span><span class="sxs-lookup"><span data-stu-id="93505-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="93505-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="93505-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="93505-117">これらの 3 つのプロパティは、標準の **IMAPIProp** メソッドを使用して処理できないので特別です。</span><span class="sxs-lookup"><span data-stu-id="93505-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="93505-118">代わりに **、IAddrBook メソッドを使用する** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="93505-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="93505-119">**IMAPIProp::SetProps** を使用してこれらのプロパティを変更することはできませんので、変更を永続的に行うために **IMAPIProp::SaveChanges** を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="93505-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="93505-120">**IAddrBook メソッドを使用して行われた** 変更は、直ちに有効になります。</span><span class="sxs-lookup"><span data-stu-id="93505-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93505-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="93505-121">See also</span></span>



[<span data-ttu-id="93505-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="93505-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

