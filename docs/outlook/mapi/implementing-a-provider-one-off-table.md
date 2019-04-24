---
title: プロバイダーの1回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332866"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="a7b03-103">プロバイダーの1回限りのテーブルの実装</span><span class="sxs-lookup"><span data-stu-id="a7b03-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="a7b03-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7b03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7b03-105">クライアントアプリケーションのユーザーが送信メッセージに受信者を追加すると、MAPI はプロバイダーの[IABLogon:: getoneofftable](iablogon-getoneofftable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="a7b03-106">通常、要求されるアドレスの種類は、メッセージングシステムに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="a7b03-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="a7b03-107">プロバイダーが受信者の作成をサポートしている場合、サポートされている受信者アドレスの種類ごとにテンプレートを公開する、1回限りのテーブルを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7b03-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="a7b03-108">プロバイダーが受信者の作成をサポートしていない場合は、 **getoneofftable**呼び出しから MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="a7b03-109">通常、MAPI はプロバイダーの1回限りのテーブルを開いたままにします。セッションの有効期間は、クライアントがサブシステムまたはアドレス帳の[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出した場合に限られます。</span><span class="sxs-lookup"><span data-stu-id="a7b03-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="a7b03-110">この表の MAPI は、テンプレートが追加または削除された場合に、ユーザーに変更を反映することができるようにするために、この表の通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="a7b03-111">**IABLogon:: getoneofftable を実装するには**</span><span class="sxs-lookup"><span data-stu-id="a7b03-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="a7b03-112">flags パラメーターの_ulflags_の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="a7b03-113">MAPI_UNICODE フラグが設定されており、プロバイダーが UNICODE をサポートしていない場合は、fail および MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="a7b03-114">プロバイダーの1回限りのテーブルが既に作成されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="a7b03-115">通常、1回限りのテーブルは静的であるため、プロバイダーは作成プロセスを複数回実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a7b03-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="a7b03-116">テーブルが既に存在する場合は、そのテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="a7b03-117">1回限りのテーブルがまだ存在しない場合は、 **CreateTable**を呼び出して、1つのテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="a7b03-118">表の行の列に対して次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="a7b03-119">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を使用して、テンプレートが作成できる受信者の種類の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="a7b03-120">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) は、1回限りのテンプレートのエントリ識別子を示します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="a7b03-121">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md)) は、1回限りのテーブル表示で階層レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="a7b03-122">**PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md)) を TRUE にして、行がテンプレートを表しているかどうかを示します。それ以外の場合は FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="a7b03-123">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) は、テンプレートによって作成されたアドレスの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="a7b03-124">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) から DT_MAILUSER またはテンプレートの表示の種類を示す別の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="a7b03-125">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) を一意のバイナリ値にします。</span><span class="sxs-lookup"><span data-stu-id="a7b03-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="a7b03-126">テーブルを直接変更するには、 [itabledata:: hrmodifyrow](itabledata-hrmodifyrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="a7b03-127">呼び出し元に返す**IMAPITable**インターフェイス実装を作成するには、 [itabledata:: hrgetview](itabledata-hrgetview.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a7b03-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

