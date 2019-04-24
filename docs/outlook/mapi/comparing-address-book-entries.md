---
title: アドレス帳エントリの比較
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335533"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="6c245-103">アドレス帳エントリの比較</span><span class="sxs-lookup"><span data-stu-id="6c245-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="6c245-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c245-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c245-105">プロバイダーの[IABLogon:: compareentryids](iablogon-compareentryids.md)実装は、プロバイダーのオブジェクトの2つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="6c245-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="6c245-106">MAPI は、2つのエントリ識別子にプロバイダーの登録済み[MAPIUID](mapiuid.md)が含まれていることを確認した後、このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6c245-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="6c245-107">そのため、 **compareentryids**メソッドは、 _lpEntryID1_パラメーターと_lpEntryID2_パラメーターに渡されたエントリ識別子がプロバイダーに属していることを確認する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6c245-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="6c245-108">**IABLogon:: compareentryids**は、2つのオブジェクトの**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを取得して、それらを直接比較することと同じです。</span><span class="sxs-lookup"><span data-stu-id="6c245-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="6c245-109">**compareentryids を実装するには**</span><span class="sxs-lookup"><span data-stu-id="6c245-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="6c245-110">プロバイダーに情報が格納されている場合は、渡されたエントリ識別子の種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="6c245-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="6c245-111">たとえば、一方のエントリ識別子はメッセージングユーザーに属している可能性がありますが、一方は配布リストに属している場合があります。</span><span class="sxs-lookup"><span data-stu-id="6c245-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="6c245-112">型が一致しない場合は、 _l出 result_パラメーターの内容を FALSE に設定して戻ります。</span><span class="sxs-lookup"><span data-stu-id="6c245-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="6c245-113">2つのエントリ識別子のサイズを比較します。</span><span class="sxs-lookup"><span data-stu-id="6c245-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="6c245-114">同じでない場合は、 _l出 result_パラメーターの内容を FALSE に設定して返します。</span><span class="sxs-lookup"><span data-stu-id="6c245-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="6c245-115">入力識別子のサイズが、種類に適したサイズであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c245-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="6c245-116">含まれていない場合は、 _lMAPI_E_UNKNOWN_ENTRYID result_パラメーターの内容を FALSE に設定し、エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="6c245-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="6c245-117">エントリ識別子が同じであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c245-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="6c245-118">同等に比較する場合は、 _l出 result_パラメーターの内容を TRUE に設定して返します。</span><span class="sxs-lookup"><span data-stu-id="6c245-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="6c245-119">それ以外の場合は、値を FALSE に設定してから返します。</span><span class="sxs-lookup"><span data-stu-id="6c245-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="6c245-120">プロバイダーが短期的なエントリ識別子と長期識別子を比較している場合は、同等に比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c245-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

