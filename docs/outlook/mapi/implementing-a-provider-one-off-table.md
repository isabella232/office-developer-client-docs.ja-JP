---
title: プロバイダーの 1 回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800923"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="1bc89-103">プロバイダーの 1 回限りのテーブルの実装</span><span class="sxs-lookup"><span data-stu-id="1bc89-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="1bc89-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1bc89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1bc89-105">MAPI は、クライアント アプリケーションのユーザーは、送信メッセージに受信者を追加するときに、プロバイダーの[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="1bc89-106">通常、要求されたアドレスの種類は、メッセージング システムに固有です。</span><span class="sxs-lookup"><span data-stu-id="1bc89-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="1bc89-107">プロバイダーは、受信者の作成をサポートする場合、サポートされている受信者のアドレスの種類ごとにテンプレートを公開する一時テーブルが必要です。</span><span class="sxs-lookup"><span data-stu-id="1bc89-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="1bc89-108">プロバイダーが受信者の作成をサポートしていない場合は、 **GetOneOffTable**の呼び出しから MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="1bc89-109">MAPI は通常、プロバイダーの一時テーブルを開いたまま、セッションの有効期間をクライアントが呼び出すサブシステムの場合にのみそれを解放するか、ブックの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドに対応します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="1bc89-110">MAPI をするよう、ユーザーにこれらの変更を反映できる場合は、テンプレートを追加または削除、このテーブルで通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="1bc89-111">**IABLogon::GetOneOffTable を実装するには**</span><span class="sxs-lookup"><span data-stu-id="1bc89-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="1bc89-112">_UlFlags_、flags パラメーターの値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="1bc89-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="1bc89-113">MAPI_UNICODE フラグが設定されて、プロバイダーが Unicode をサポートしていない場合は、失敗し、MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="1bc89-114">プロバイダーの一時テーブルが既に作成されているを確認します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="1bc89-115">一時テーブルは静的であるため、プロバイダーが複数回作成プロセスを経由します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="1bc89-116">テーブルが既に存在する場合、それへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="1bc89-117">一時テーブルが存在しない場合は、1 つを作成するのには、 **CreateTable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="1bc89-118">テーブル行の列の次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="1bc89-119">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) にテンプレートを作成できる受信者の種類の名前。</span><span class="sxs-lookup"><span data-stu-id="1bc89-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="1bc89-120">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) に 1 回限りのテンプレートのエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="1bc89-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="1bc89-121">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md)) の 1 回限りの一覧が表示階層レベルを示す。</span><span class="sxs-lookup"><span data-stu-id="1bc89-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="1bc89-122">**PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md)) かどうか、行を表すテンプレートと FALSE それ以外の場合を示すために TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="1bc89-123">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のテンプレートで作成されたアドレスの種類にします。</span><span class="sxs-lookup"><span data-stu-id="1bc89-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="1bc89-124">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER またはテンプレートの表示の種類を示す別の値にします。</span><span class="sxs-lookup"><span data-stu-id="1bc89-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="1bc89-125">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) に固有のバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="1bc89-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="1bc89-126">テーブルを直接変更するのには[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="1bc89-127">呼び出し元に戻るには**IMAPITable**インターフェイスの実装を作成するのには、 [ITableData::HrGetView](itabledata-hrgetview.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1bc89-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

