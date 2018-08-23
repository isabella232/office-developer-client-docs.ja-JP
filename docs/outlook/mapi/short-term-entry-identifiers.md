---
title: 短期的なエントリ id
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 03352b55589138d406ad3e4ee0756fc44bca8c78
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580615"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="495d5-103">短期的なエントリ id</span><span class="sxs-lookup"><span data-stu-id="495d5-103">Short-term entry identifiers</span></span>

<span data-ttu-id="495d5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="495d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="495d5-105">短期的なエントリの識別子は、識別子が迅速に構築する必要があり、最後の時間または距離にする必要はありません、オブジェクトへのサービス プロバイダーによって割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="495d5-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="495d5-106">のみ期間中の現在のセッションでは、現在のワークステーションでは、短期的なエントリ id の一意性が保証されます。</span><span class="sxs-lookup"><span data-stu-id="495d5-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="495d5-107">通常、短期的なエントリ id は、それが表すオブジェクトが解放されるまでにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="495d5-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="495d5-108">ダイアログ ボックスで、参照するために迅速にデータを提供する必要があるエントリをテーブル内の行には、短期的なエントリ id が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="495d5-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="495d5-109">などのコンテンツ テーブル内のメッセージの行に、受信者テーブル内の受信者に、メッセージ ストア プロバイダーは短期的なエントリの識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="495d5-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="495d5-110">クライアントは、テーブルの行によって表されるオブジェクトを開く、これらの短期的なエントリ id を使用できます。</span><span class="sxs-lookup"><span data-stu-id="495d5-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="495d5-111">ただし、 **OpenEntry**メソッドのいずれかで使用できる長期のエントリ id とは異なり、短期的なエントリ id はコンテナーの**OpenEntry**メソッドで使用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="495d5-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="495d5-112">短期的なエントリ id を実装します。</span><span class="sxs-lookup"><span data-stu-id="495d5-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="495d5-113">短期的なエントリ id を実装する最も一般的な方法を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="495d5-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="495d5-114">すべてのフラグの設定を解除のまま、長期的な識別子として同じ短期のエントリ id を行っています。</span><span class="sxs-lookup"><span data-stu-id="495d5-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="495d5-115">短期的なエントリの識別子のすべてのフラグの設定、長期的な識別子とは異なるを行っています。</span><span class="sxs-lookup"><span data-stu-id="495d5-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="495d5-116">クライアントは、次のように、 **abFlags**メンバーを調べることでの 2 つ目の短期的なエントリ id を特定できます。</span><span class="sxs-lookup"><span data-stu-id="495d5-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="495d5-117">サービス プロバイダーによってより妥当性のある短期のエントリの識別子を作成する 1 つまたは複数のフラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="495d5-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="495d5-118">などの次の**abFlags**メンバーは、複数の日または複数のセッションに使用できる短期的なエントリ id を表します。</span><span class="sxs-lookup"><span data-stu-id="495d5-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="495d5-119">クライアントが簡単に取得、使用、および短期的なエントリ id を破棄します。</span><span class="sxs-lookup"><span data-stu-id="495d5-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="495d5-120">大部分は、長期のエントリ id と同じように使用することができます。</span><span class="sxs-lookup"><span data-stu-id="495d5-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="495d5-121">**OpenEntry**メソッドに渡され、 **CompareEntryIDs**メソッドと比較して、テーブルからは、それらを取得できます。</span><span class="sxs-lookup"><span data-stu-id="495d5-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="495d5-122">1 つの例外は、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドから返されますしないことです。</span><span class="sxs-lookup"><span data-stu-id="495d5-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="495d5-123">**GetProps**から返されるプロパティは、常に長期的なエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="495d5-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="495d5-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="495d5-124">See also</span></span>

- [<span data-ttu-id="495d5-125">MAPI エントリの識別子</span><span class="sxs-lookup"><span data-stu-id="495d5-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

