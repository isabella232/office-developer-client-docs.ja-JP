---
title: 受信者情報を表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7071c05f6f59740163f97f840c7fa48d83bea815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799952"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="2b059-103">受信者情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="2b059-103">Displaying recipient information</span></span>

<span data-ttu-id="2b059-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b059-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b059-105">MAPI には、受信者の詳細を表示するためのコモン ダイアログ ボックスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="2b059-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="2b059-106">**IMAPIProp**実装とディスプレイ テーブルから、[詳細情報] ダイアログ ボックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2b059-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="2b059-107">表示された表の詳細の表示の外観を記述して、 **IMAPIProp**の実装は、受信者のデータを制御します。</span><span class="sxs-lookup"><span data-stu-id="2b059-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="2b059-108">プロバイダーは、表示された表と各受信者の**IMAPIProp**の実装を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b059-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="2b059-109">[DTPAGE](dtpage.md)構造体を定義し、 [BuildDisplayTable](builddisplaytable.md)を呼び出すには、表示された表を作成する最も簡単な方法です。</span><span class="sxs-lookup"><span data-stu-id="2b059-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="2b059-110">ただし、一部のプロバイダーでは、具体的には読み取り専用プロバイダーを 1 回限りの受信者の作成は、 **IPropData**を使用します。</span><span class="sxs-lookup"><span data-stu-id="2b059-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="2b059-111">**IMAPIProp**の実装は、オブジェクトのプロパティの任意の型にできます。</span><span class="sxs-lookup"><span data-stu-id="2b059-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="2b059-112">このダイアログ ボックスを起動するための 2 つの方法があります: [IAddrBook::Details](iaddrbook-details.md)と[IMAPISupport::Details](imapisupport-details.md)。</span><span class="sxs-lookup"><span data-stu-id="2b059-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="2b059-113">プロバイダーを呼び出すと、受信者の詳細を要求するこれらのメソッドのいずれか、MAPI はまずコンテナーの[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを呼び出すことによって、受信者を開きます。</span><span class="sxs-lookup"><span data-stu-id="2b059-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="2b059-114">次に**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求するための受信者の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2b059-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="2b059-115">**PR_DETAILS_TABLE**は、受信者の詳細表示のテーブルを表すプロパティです。</span><span class="sxs-lookup"><span data-stu-id="2b059-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="2b059-116">[IPropData: IMAPIProp](ipropdataimapiprop.md)以下の手順で説明したようにテーブル コントロールの表示上の変更を監視するインターフェイスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2b059-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="2b059-117">コントロールへの変更を監視します。</span><span class="sxs-lookup"><span data-stu-id="2b059-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="2b059-118">ユーザーは、コントロールへのアクセス権を取得、前に、コントロールのアクセスを IPROP_CLEAN に設定するのには[IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2b059-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="2b059-119">ダイアログ ボックスを操作するユーザーを許可します。</span><span class="sxs-lookup"><span data-stu-id="2b059-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="2b059-120">ユーザーが完了したら、コントロールの現在のアクセス レベルを取得するために[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2b059-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="2b059-121">アクセス レベルが IPROP_DIRTY の場合は、ユーザーがコントロールを変更します。</span><span class="sxs-lookup"><span data-stu-id="2b059-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="2b059-122">プロバイダーは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2b059-122">Your provider should:</span></span>
    
   - <span data-ttu-id="2b059-123">IPROP_CLEAN にレベルのアクセス権を設定するのには[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2b059-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="2b059-124">プロパティの変更を取得し、 [IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出すことによって更新するのには、プロパティのデータ オブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2b059-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="2b059-125">アクセス レベルがまだ IPROP_CLEAN である場合、コントロールは変更されていません。</span><span class="sxs-lookup"><span data-stu-id="2b059-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="2b059-126">表示のテーブルを作成する方法の詳細については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b059-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

