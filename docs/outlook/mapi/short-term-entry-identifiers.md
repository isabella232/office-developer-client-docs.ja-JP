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
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="b01b9-103">短期エントリ ID</span><span class="sxs-lookup"><span data-stu-id="b01b9-103">Short-term entry identifiers</span></span>

<span data-ttu-id="b01b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b01b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b01b9-105">識別子をすばやく構築する必要があり、最後に時間や距離を必要としない場合は、サービスプロバイダーによって、短い用語のエントリ識別子がオブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="b01b9-106">短い用語エントリ識別子の一意性は、現在のワークステーション上の現在のセッションが終了するまでのみ保証されます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="b01b9-107">通常、短い用語のエントリ識別子は、それが表すオブジェクトが解放されるまで有効です。</span><span class="sxs-lookup"><span data-stu-id="b01b9-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="b01b9-108">短い用語入力識別子は、テーブル内の行に、またはダイアログボックス内のエントリに割り当てられます。ここでは、データを参照用にすばやく入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b01b9-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="b01b9-109">たとえば、メッセージストアプロバイダーは、短い用語のエントリ識別子を、コンテンツテーブル内のメッセージの行と受信者テーブル内の受信者に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="b01b9-110">クライアントは、これらの短い用語入力識別子を使用して、テーブルの行で表されるオブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="b01b9-111">ただし、任意の**openentry**メソッドで使用できる長期間のエントリ識別子とは異なり、短い用語のエントリ識別子をコンテナーの**openentry**メソッドと共に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b01b9-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="b01b9-112">短い用語エントリ識別子の実装</span><span class="sxs-lookup"><span data-stu-id="b01b9-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="b01b9-113">短期間のエントリ識別子を実装する最も一般的な方法は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b01b9-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="b01b9-114">短い用語のエントリ識別子を長期識別子と同じにして、すべてのフラグを未設定のままにします。</span><span class="sxs-lookup"><span data-stu-id="b01b9-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="b01b9-115">短い用語のエントリ識別子を長期識別子とは異なるものにし、すべてのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b01b9-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="b01b9-116">クライアントは、次のように**abflags**メンバーを調べることによって、2番目の種類の短い用語のエントリ識別子を識別できます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="b01b9-117">一部のサービスプロバイダーでは、1つ以上のフラグがクリアされ、有効期限の短い用語エントリ識別子が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="b01b9-118">たとえば、次の**abflags**メンバーは、複数の日または複数のセッションに使用できる短い用語のエントリ識別子を表します。</span><span class="sxs-lookup"><span data-stu-id="b01b9-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="b01b9-119">クライアントは短時間のエントリ識別子を取得、使用、および破棄することができます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="b01b9-120">ほとんどの場合、長期間の入力識別子と同じ方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="b01b9-121">これらはテーブルから取得でき、 **openentry**メソッドに渡され、 **compareentryids**メソッドと比較されます。</span><span class="sxs-lookup"><span data-stu-id="b01b9-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="b01b9-122">1つの例外は、これらが[imapiprop:: GetProps](imapiprop-getprops.md)メソッドから返されることはないということです。</span><span class="sxs-lookup"><span data-stu-id="b01b9-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="b01b9-123">**GetProps**から返されるプロパティは、常に長期間のエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="b01b9-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b01b9-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="b01b9-124">See also</span></span>

- [<span data-ttu-id="b01b9-125">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="b01b9-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

