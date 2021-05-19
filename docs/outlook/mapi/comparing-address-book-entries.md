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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415356"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="3435f-103">アドレス帳エントリの比較</span><span class="sxs-lookup"><span data-stu-id="3435f-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="3435f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3435f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3435f-105">プロバイダーの [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) 実装は、プロバイダーの 2 つのオブジェクトのエントリ識別子を比較します。</span><span class="sxs-lookup"><span data-stu-id="3435f-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="3435f-106">MAPI は、2 つのエントリ識別子にプロバイダーの登録済み MAPIUID が含まれていると判断した後、このメソッド [を呼び出します](mapiuid.md)。</span><span class="sxs-lookup"><span data-stu-id="3435f-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="3435f-107">そのため **、CompareEntryIDs** メソッドは  _、lpEntryID1_ および  _lpEntryID2_ パラメーターに渡されたエントリ識別子がプロバイダーに属している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3435f-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="3435f-108">**IABLogon::CompareEntryIDs** の呼び出しは **、2** つのオブジェクトごとに PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを取得し、それらを直接比較するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="3435f-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="3435f-109">**CompareEntryIds を実装する方法**</span><span class="sxs-lookup"><span data-stu-id="3435f-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="3435f-110">プロバイダーが情報を格納している場合は、渡されたエントリ識別子の種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="3435f-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="3435f-111">たとえば、1 つのエントリ識別子がメッセージング ユーザーに属し、もう一方が配布リストに属している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3435f-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="3435f-112">型が一致しない場合は  _、lpulResult_ パラメーターの内容を FALSE に設定して返します。</span><span class="sxs-lookup"><span data-stu-id="3435f-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="3435f-113">2 つのエントリ識別子のサイズを比較します。</span><span class="sxs-lookup"><span data-stu-id="3435f-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="3435f-114">同じではない場合は  _、lpulResult_ パラメーターの内容を FALSE に設定して戻します。</span><span class="sxs-lookup"><span data-stu-id="3435f-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="3435f-115">エントリ識別子のサイズが、その種類に対して正しいサイズである必要があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3435f-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="3435f-116">指定しない場合は  _、lpulResult_ パラメーターの内容を FALSE に設定し、エラー値を false にMAPI_E_UNKNOWN_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="3435f-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="3435f-117">エントリ識別子が同じか確認します。</span><span class="sxs-lookup"><span data-stu-id="3435f-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="3435f-118">等しく比較する場合は  _、lpulResult_ パラメーターの内容を TRUE に設定して返します。</span><span class="sxs-lookup"><span data-stu-id="3435f-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="3435f-119">それ以外の場合は、返す前に FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="3435f-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="3435f-120">プロバイダーが短期エントリ識別子と長期識別子を比較している場合は、同じように比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3435f-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

