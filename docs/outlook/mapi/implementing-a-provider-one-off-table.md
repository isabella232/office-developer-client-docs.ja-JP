---
title: プロバイダー テーブルのOne-Offする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436294"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="5d782-103">プロバイダー テーブルのOne-Offする</span><span class="sxs-lookup"><span data-stu-id="5d782-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="5d782-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d782-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d782-105">MAPI は、クライアント アプリケーションのユーザーが受信者を送信メッセージに追加するときに、プロバイダーの [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5d782-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="5d782-106">通常、要求されるアドレスの種類はメッセージング システムに固有です。</span><span class="sxs-lookup"><span data-stu-id="5d782-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="5d782-107">プロバイダーが受信者の作成をサポートしている場合は、サポートされている受信者アドレスのすべての種類のテンプレートを公開する 1 回のテーブルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d782-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="5d782-108">プロバイダーが受信者の作成をサポートしていない場合は **、GetOneOffTable** 呼び出MAPI_E_NO_SUPPORTを返します。</span><span class="sxs-lookup"><span data-stu-id="5d782-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="5d782-109">MAPI は通常、セッションの有効期間中、プロバイダーの一時テーブルを開いた状態に保ち、クライアントがサブシステムまたはアドレス帳の [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを呼び出す場合にのみ解放します。</span><span class="sxs-lookup"><span data-stu-id="5d782-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="5d782-110">MAPI は、テンプレートが追加または削除された場合、これらの変更をユーザーに反映できるよう、このテーブルの通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="5d782-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="5d782-111">**IABLogon::GetOneOffTable を実装するには**</span><span class="sxs-lookup"><span data-stu-id="5d782-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="5d782-112">flags パラメーター  _ulFlags の値を確認します_。</span><span class="sxs-lookup"><span data-stu-id="5d782-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="5d782-113">このフラグMAPI_UNICODE設定され、プロバイダーが Unicode をサポートしていない場合は、エラーが発生し、MAPI_E_BAD_CHARWIDTH。</span><span class="sxs-lookup"><span data-stu-id="5d782-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="5d782-114">プロバイダーの 1 回のテーブルが既に作成済みか確認します。</span><span class="sxs-lookup"><span data-stu-id="5d782-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="5d782-115">通常、1 回のテーブルは静的なので、プロバイダーは作成プロセスを 2 回以上実行する必要がなされません。</span><span class="sxs-lookup"><span data-stu-id="5d782-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="5d782-116">テーブルが既に存在する場合は、そのテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5d782-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="5d782-117">1 回のテーブルがまだ存在しない場合は **、CreateTable を呼び出して** 作成します。</span><span class="sxs-lookup"><span data-stu-id="5d782-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="5d782-118">テーブル行の列に対して、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5d782-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="5d782-119">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)をテンプレートで作成できる受信者の種類の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d782-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="5d782-120">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)を一時テンプレートのエントリ識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="5d782-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="5d782-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) を使用して、1 回のテーブル表示で階層レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="5d782-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="5d782-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) を TRUE に設定して、行がテンプレートを表すかどうかを示し、それ以外の場合は FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d782-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="5d782-123">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)をテンプレートによって作成されたアドレスの種類に設定します。</span><span class="sxs-lookup"><span data-stu-id="5d782-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="5d782-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を使用して、DT_MAILUSERの表示の種類を示す別の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d782-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="5d782-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) を一意のバイナリ値に変換します。</span><span class="sxs-lookup"><span data-stu-id="5d782-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="5d782-126">[ITableData::HrModifyRow を呼び出して](itabledata-hrmodifyrow.md)、テーブルを直接変更します。</span><span class="sxs-lookup"><span data-stu-id="5d782-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="5d782-127">[ITableData::HrGetView](itabledata-hrgetview.md)を呼び出して、呼び出し元に戻る **IMAPITable** インターフェイス実装を作成します。</span><span class="sxs-lookup"><span data-stu-id="5d782-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

