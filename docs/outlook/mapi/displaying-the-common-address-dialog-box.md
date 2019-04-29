---
title: '[共通アドレス] ダイアログボックスを表示する'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436904"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="36ab0-103">[共通アドレス] ダイアログボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="36ab0-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="36ab0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36ab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36ab0-105">[MAPI 共通アドレス] ダイアログボックスは、受信者リストの作成など、さまざまなアドレス指定タスクに使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab0-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="36ab0-106">このダイアログボックスを表示するには、 **IAddrBook:: Address**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36ab0-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="36ab0-107">設定されているパラメーターの種類およびそれらの設定方法に応じて、特定のコンテナーから特定の種類のエントリへの表示を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="36ab0-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="36ab0-108">**[アドレス] ダイアログボックスで個人用アドレス帳 (PAB) エントリのみを表示するように制限するには**</span><span class="sxs-lookup"><span data-stu-id="36ab0-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="36ab0-109">[IAddrBook:: getpab](iaddrbook-getpab.md)を呼び出して、pab のエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="36ab0-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="36ab0-110">[spropertyrestriction](spropertyrestriction.md)構造の**relop**メンバに対して RELOP_EQ を使用し、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のどちらかとしてのプロパティ制限を作成します。**ulPropTag**メンバー。</span><span class="sxs-lookup"><span data-stu-id="36ab0-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="36ab0-111">**PR_ENTRYID**を使用する場合は、 **getpab**から取得したエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="36ab0-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="36ab0-112">**PR_AB_PROVIDER_ID**を使用する場合は、mspab に含まれる値を渡します。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="36ab0-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="36ab0-113">**PR_AB_PROVIDER_ID**は、MAPI によって設計された PAB の一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="36ab0-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="36ab0-114">プロパティ制限を指す_lpHierRestriction_パラメーターを使用して、 [IAddrBook:: Address](iaddrbook-address.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36ab0-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

