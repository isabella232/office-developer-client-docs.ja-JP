---
title: '[よく使うアドレス] ダイアログ ボックスの表示'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00d1063310aaf1a8948e04d725d7e11418cf986c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592424"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="ea723-103">[よく使うアドレス] ダイアログ ボックスの表示</span><span class="sxs-lookup"><span data-stu-id="ea723-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="ea723-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea723-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea723-105">MAPI の [アドレス] コモン ダイアログ ボックスは、さまざまな受信者リストを構築するなどのアドレス指定のタスクを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ea723-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="ea723-106">このダイアログ ボックスを表示するには、 **IAddrBook::Address**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea723-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="ea723-107">多くのパラメーターを設定して、それらの組み合わせによって、特定のコンテナーから、特定の種類のエントリを表示を制限できます。</span><span class="sxs-lookup"><span data-stu-id="ea723-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="ea723-108">**個人用アドレス帳 (PAB) のエントリのみを表示するのには、[アドレス] ダイアログ ボックスを制限するには**</span><span class="sxs-lookup"><span data-stu-id="ea723-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="ea723-109">個人アドレス帳のエントリ id を取得するために[られたユーザーのプライマリ](iaddrbook-getpab.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea723-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="ea723-110">として RELOP_EQ を使用して、 **relop** 、 [SPropertyRestriction](spropertyrestriction.md)の構造と、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のメンバーのプロパティ制約を作成します**ulPropTag**のメンバーです。</span><span class="sxs-lookup"><span data-stu-id="ea723-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="ea723-111">**PR_ENTRYID**を使用する場合は、 **GetPAB**から取得したエントリの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="ea723-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="ea723-112">**PR_AB_PROVIDER_ID**を使用する場合は、MSPAB に含まれている値を渡します。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="ea723-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="ea723-113">**PR_AB_PROVIDER_ID**は、MAPI によって設計された PAB の一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="ea723-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="ea723-114">プロパティ制限を指定する_lpHierRestriction_パラメーターで[IAddrBook::Address](iaddrbook-address.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea723-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

