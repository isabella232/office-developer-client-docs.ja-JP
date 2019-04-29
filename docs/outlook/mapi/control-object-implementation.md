---
title: コントロールオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422608"
---
# <a name="control-object-implementation"></a><span data-ttu-id="3ad70-103">コントロールオブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="3ad70-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="3ad70-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ad70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ad70-105">コントロールオブジェクト、または[IMAPIControl: IUnknown](imapicontroliunknown.md)インターフェイスをサポートするオブジェクトは、プロバイダーによって実装され、MAPI ダイアログボックスに表示されるボタンに機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="3ad70-106">コントロールオブジェクトは、ボタンに対してのみ実装できます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="3ad70-107">**IMAPIControl**には、 [GetLastError](imapicontrol-getlasterror.md)、 [GetState](imapicontrol-getstate.md)、および[Activate](imapicontrol-activate.md)の3つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="3ad70-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="3ad70-108">MAPI は**GetState**を呼び出して、ボタンを無効にするかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="3ad70-109">**GetState**は、次のような場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="3ad70-110">ボタンが表示されるダイアログボックスが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="3ad70-111">ボタンに対して表示テーブル通知が発行されたとき。</span><span class="sxs-lookup"><span data-stu-id="3ad70-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="3ad70-112">ユーザーが操作できる場合は、ボタンと MAPI_ENABLED を操作できない場合は、 _lMAPI_DISABLED state_パラメーターの内容を「」に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="3ad70-113">ユーザーがボタンをクリックすると、MAPI 呼び出しが**アクティブ**になります。</span><span class="sxs-lookup"><span data-stu-id="3ad70-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="3ad70-114">**Activate**は、ボタンに関連付けられているタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="3ad70-115">このタスクは、ダイアログボックスを表示したり、プロパティを更新したりするなど、プロバイダーにとって適切なものでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="3ad70-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="3ad70-116">ユーザーがキャンセルしたためにタスクが失敗した場合は、MAPI_E_USER_CANCEL を返します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="3ad70-117">失敗のその他の原因については、適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="3ad70-118">タスクが正常に実行され、ダイアログボックスの別のコントロールに反映されるプロパティの変更にリンクされている場合は、 [itabledata:: hrnotify](itabledata-hrnotify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="3ad70-119">**hrnotify**は、 [TABLE_NOTIFICATION](table_notification.md)構造の変更されたプロパティの**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティを使用して、表示テーブル通知を発行するために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="3ad70-120">新しいプロパティの値は、構造体に配置しないでください。代わりに、 [imapiprop:: GetProps](imapiprop-getprops.md)が呼び出されたときに返されます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="3ad70-121">通常、表示テーブル通知を使用してコントロールを無効または有効にすることはできませんが、ボタンと共に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="3ad70-122">MAPI は、通知に応答するように変更されたコントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="3ad70-123">MAPI は、**アクティブ化**時に MAPI_E_USER_CANCEL 以外のエラーを返すコントロールの**GetLastError**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3ad70-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="3ad70-124">**GetLastError**が、 _lppMAPIError_パラメーターの内容で返される[MAPIERROR](mapierror.md)構造に拡張エラー情報を配置すると、ユーザーに対して MAPI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ad70-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ad70-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ad70-125">See also</span></span>



[<span data-ttu-id="3ad70-126">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="3ad70-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

