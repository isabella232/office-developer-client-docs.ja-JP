---
title: アドレス帳のエントリを比較します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799797"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="b538e-103">アドレス帳のエントリを比較します。</span><span class="sxs-lookup"><span data-stu-id="b538e-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="b538e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b538e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b538e-105">[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)プロバイダーは、プロバイダーのオブジェクトの 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="b538e-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="b538e-106">MAPI は、 [MAPIUID](mapiuid.md)を登録して、プロバイダーを 2 つのエントリの識別子が含まれていることを確認した後に、このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b538e-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="b538e-107">したがって、 **CompareEntryIDs**メソッドでは、 _lpEntryID1_および_lpEntryID2_パラメーターに渡されたエントリ id をプロバイダーに属している必要があります調べません。</span><span class="sxs-lookup"><span data-stu-id="b538e-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="b538e-108">**IABLogon::CompareEntryIDs**の呼び出しは、2 つのオブジェクトごとに、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティを取得して、直接比較することと等価です。</span><span class="sxs-lookup"><span data-stu-id="b538e-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="b538e-109">**CompareEntryIds を実装するには**</span><span class="sxs-lookup"><span data-stu-id="b538e-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="b538e-110">プロバイダーがその情報を保存する場合は渡されたエントリ id の種類を確認してください。</span><span class="sxs-lookup"><span data-stu-id="b538e-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="b538e-111">たとえば、1 つのエントリ id が属しているメッセージング ユーザーに配布リストに所属している他の中に。</span><span class="sxs-lookup"><span data-stu-id="b538e-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="b538e-112">型が一致しない場合は、false を指定し、戻り値に_lpulResult_パラメーターの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="b538e-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="b538e-113">2 つのエントリ id のサイズを比較します。</span><span class="sxs-lookup"><span data-stu-id="b538e-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="b538e-114">同じである場合は、FALSE を返す_lpulResult_パラメーターの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="b538e-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="b538e-115">エントリ id のサイズが型に対して適切なサイズであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b538e-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="b538e-116">いない場合は、false を指定する_lpulResult_パラメーターの内容を設定し、MAPI_E_UNKNOWN_ENTRYID のエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="b538e-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="b538e-117">エントリ id が同じかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b538e-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="b538e-118">同様に、比較する場合は、true を指定し、戻り値に_lpulResult_パラメーターの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="b538e-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="b538e-119">それ以外の場合、FALSE に設定を返す前にします。</span><span class="sxs-lookup"><span data-stu-id="b538e-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="b538e-120">場合は、プロバイダーは、長期的な識別子を使用して、短期的なエントリ id を比較することは、同じように比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b538e-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

