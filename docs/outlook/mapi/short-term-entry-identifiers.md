---
title: 短期エントリ ID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439563"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="8362f-103">短期エントリ ID</span><span class="sxs-lookup"><span data-stu-id="8362f-103">Short-term entry identifiers</span></span>

<span data-ttu-id="8362f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8362f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8362f-105">短期間のエントリ識別子は、識別子を迅速に構築する必要があるときにサービス プロバイダーによってオブジェクトに割り当て、時間や距離の長持ちを必要としない場合に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8362f-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="8362f-106">短期エントリ識別子の一意性は、現在のワークステーション上の現在のセッションの期間のみ保証されます。</span><span class="sxs-lookup"><span data-stu-id="8362f-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="8362f-107">通常、短期エントリ識別子は、それを表すオブジェクトが解放されるまで有効です。</span><span class="sxs-lookup"><span data-stu-id="8362f-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="8362f-108">短期的なエントリ識別子は、テーブル内の行とダイアログ ボックス内のエントリに割り当てられます。ここで、参照用にデータをすばやく提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8362f-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="8362f-109">たとえば、メッセージ ストア プロバイダーは、短期的なエントリ識別子をコンテンツ テーブル内のメッセージの行に、受信者テーブルの受信者に割り当てるとします。</span><span class="sxs-lookup"><span data-stu-id="8362f-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="8362f-110">クライアントは、これらの短期エントリ識別子を使用して、テーブル行で表されるオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="8362f-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="8362f-111">ただし **、OpenEntry** メソッドで使用できる長期エントリ識別子とは異なり、コンテナーの **OpenEntry** メソッドでは、短期エントリ識別子を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8362f-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="8362f-112">短期エントリ識別子の実装</span><span class="sxs-lookup"><span data-stu-id="8362f-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="8362f-113">短期エントリ識別子を実装する最も一般的な方法は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8362f-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="8362f-114">短期エントリ識別子を長期識別子と同じにし、すべてのフラグを設定解除します。</span><span class="sxs-lookup"><span data-stu-id="8362f-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="8362f-115">短期エントリ識別子を長期識別子と異なって、すべてのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="8362f-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="8362f-116">クライアントは **、abFlags** メンバーを次のように調べることによって、2 番目の型の短期エントリ識別子を識別できます。</span><span class="sxs-lookup"><span data-stu-id="8362f-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="8362f-117">一部のサービス プロバイダーは、1 つ以上のフラグをクリアして、より高い有効性を持つ短期エントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="8362f-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="8362f-118">たとえば、次の **abFlags** メンバーは、複数日または複数のセッションで使用できる短期エントリ識別子を表します。</span><span class="sxs-lookup"><span data-stu-id="8362f-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="8362f-119">クライアントは、短期間のエントリ識別子をすばやく取得、使用、破棄します。</span><span class="sxs-lookup"><span data-stu-id="8362f-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="8362f-120">ほとんどの場合、長期エントリ識別子と同じ方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8362f-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="8362f-121">テーブルから取得し **、OpenEntry** メソッドに渡し **、CompareEntryIDs** メソッドと比較できます。</span><span class="sxs-lookup"><span data-stu-id="8362f-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="8362f-122">1 つの例外は [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドから返されません。</span><span class="sxs-lookup"><span data-stu-id="8362f-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="8362f-123">**GetProps から返されるプロパティは**、常に長期的なエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="8362f-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8362f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="8362f-124">See also</span></span>

- [<span data-ttu-id="8362f-125">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="8362f-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

