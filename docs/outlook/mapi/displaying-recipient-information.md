---
title: 受信者情報の表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412955"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="50bd0-103">受信者情報の表示</span><span class="sxs-lookup"><span data-stu-id="50bd0-103">Displaying recipient information</span></span>

<span data-ttu-id="50bd0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50bd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50bd0-105">MAPI には、受信者の詳細を表示する一般的なダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="50bd0-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="50bd0-106">詳細ダイアログ ボックスは、表示テーブルと **IMAPIProp 実装から作成** されます。</span><span class="sxs-lookup"><span data-stu-id="50bd0-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="50bd0-107">表示テーブルは詳細表示の外観を示し **、IMAPIProp 実装** は受信者のデータを制御します。</span><span class="sxs-lookup"><span data-stu-id="50bd0-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="50bd0-108">プロバイダーは、各受信者に対して表示テーブルと **IMAPIProp 実装** を提供する責任があります。</span><span class="sxs-lookup"><span data-stu-id="50bd0-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="50bd0-109">表示テーブルを作成する最も簡単な方法は [、DTPAGE](dtpage.md) 構造を定義し [、BuildDisplayTable を呼び出す方法です](builddisplaytable.md)。</span><span class="sxs-lookup"><span data-stu-id="50bd0-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="50bd0-110">ただし、一部のプロバイダー、特に 1 回限り受信者の作成を許可する読み取り専用 **プロバイダーでは、IPropData を使用します**。</span><span class="sxs-lookup"><span data-stu-id="50bd0-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="50bd0-111">**IMAPIProp の実装** には、任意の種類のプロパティ オブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="50bd0-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="50bd0-112">このダイアログ ボックスを呼び出す方法は [、IAddrBook::D etails](iaddrbook-details.md) と [IMAPISupport::D です](imapisupport-details.md)。</span><span class="sxs-lookup"><span data-stu-id="50bd0-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="50bd0-113">プロバイダーが次のいずれかのメソッドを呼び出して受信者の詳細を要求すると、MAPI は最初にコンテナーの [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) メソッドを呼び出して受信者を開きます。</span><span class="sxs-lookup"><span data-stu-id="50bd0-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="50bd0-114">次に、受信者の [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して、PR_DETAILS_TABLE **(** [PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="50bd0-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="50bd0-115">**PR_DETAILS_TABLE** は、受信者の詳細表示テーブルを表すプロパティです。</span><span class="sxs-lookup"><span data-stu-id="50bd0-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="50bd0-116">[IPropData : IMAPIProp](ipropdataimapiprop.md)インターフェイスは、次の手順で説明するように、表示テーブル コントロールの変更を監視するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="50bd0-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="50bd0-117">コントロールへの変更を監視する</span><span class="sxs-lookup"><span data-stu-id="50bd0-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="50bd0-118">ユーザーがコントロールにアクセスする前に [、IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) を呼び出して、コントロールのアクセス権をコントロールに設定IPROP_CLEAN。</span><span class="sxs-lookup"><span data-stu-id="50bd0-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="50bd0-119">ユーザーがダイアログ ボックスを操作できます。</span><span class="sxs-lookup"><span data-stu-id="50bd0-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="50bd0-120">ユーザーが終了したら [、IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) を呼び出して、コントロールの現在のアクセス レベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="50bd0-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="50bd0-121">アクセス レベルが変更IPROP_DIRTY、ユーザーはコントロールを変更しました。</span><span class="sxs-lookup"><span data-stu-id="50bd0-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="50bd0-122">プロバイダーは以下を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="50bd0-122">Your provider should:</span></span>
    
   - <span data-ttu-id="50bd0-123">[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)を呼び出して、アクセス レベルをユーザーに設定IPROP_CLEAN。</span><span class="sxs-lookup"><span data-stu-id="50bd0-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="50bd0-124">プロパティ データ オブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、変更されたプロパティを取得し [、IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出して更新します。</span><span class="sxs-lookup"><span data-stu-id="50bd0-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="50bd0-125">アクセス レベルが引き続きIPROP_CLEAN、コントロールは変更されません。</span><span class="sxs-lookup"><span data-stu-id="50bd0-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="50bd0-126">表示テーブルの作成の詳細については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="50bd0-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

