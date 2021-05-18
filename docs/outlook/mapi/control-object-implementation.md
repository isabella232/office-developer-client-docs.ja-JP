---
title: コントロール オブジェクトの実装
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
# <a name="control-object-implementation"></a><span data-ttu-id="70ea0-103">コントロール オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="70ea0-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="70ea0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70ea0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70ea0-105">[IMAPIControl : IUnknown](imapicontroliunknown.md)インターフェイスをサポートするコントロール オブジェクトまたはオブジェクトは、MAPI ダイアログ ボックスに表示されるボタンに機能を追加するためにプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="70ea0-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="70ea0-106">コントロール オブジェクトはボタンにのみ実装できます。</span><span class="sxs-lookup"><span data-stu-id="70ea0-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="70ea0-107">**IMAPIControl には**[、GetLastError、GetState、](imapicontrol-getlasterror.md)[および](imapicontrol-getstate.md)Activate の 3 つのメソッド [があります](imapicontrol-activate.md)。</span><span class="sxs-lookup"><span data-stu-id="70ea0-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="70ea0-108">MAPI は **GetState を** 呼び出して、ボタンを無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="70ea0-109">**GetState は** 、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="70ea0-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="70ea0-110">ボタンが表示されるダイアログ ボックスが最初に表示される場合。</span><span class="sxs-lookup"><span data-stu-id="70ea0-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="70ea0-111">ボタンに対して表示テーブル通知が発行された場合。</span><span class="sxs-lookup"><span data-stu-id="70ea0-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="70ea0-112">ユーザーがボタンを操作できないMAPI_DISABLED操作できる場合は  _、lpulState_ パラメーター MAPI_ENABLEDに設定します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="70ea0-113">ユーザーがボタンをクリックすると、MAPI は Activate を呼び **出します**。</span><span class="sxs-lookup"><span data-stu-id="70ea0-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="70ea0-114">**[アクティブ** 化] ボタンに関連付けられているタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="70ea0-115">このタスクは、ダイアログ ボックスの表示やプロパティの更新など、プロバイダーに適したタスクです。</span><span class="sxs-lookup"><span data-stu-id="70ea0-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="70ea0-116">ユーザーが取り消したため、タスクが失敗した場合は、タスクをMAPI_E_USER_CANCEL。</span><span class="sxs-lookup"><span data-stu-id="70ea0-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="70ea0-117">その他のエラーの原因については、適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="70ea0-118">タスクが成功し、ダイアログ ボックスの別のコントロールに反映されるプロパティの変更にリンクされている場合は [、ITableData::HrNotify を呼び出します](itabledata-hrnotify.md)。</span><span class="sxs-lookup"><span data-stu-id="70ea0-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="70ea0-119">**HrNotify は**、変更されたプロパティの PR_CONTROL_ID **(** [PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティを持つ表示テーブル通知を [TABLE_NOTIFICATIONします。](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="70ea0-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="70ea0-120">構造体に新しいプロパティ値を配置しない。代わりに [、IMAPIProp::GetProps](imapiprop-getprops.md) が呼び出された場合に返します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="70ea0-121">通常、表示テーブル通知を使用してコントロールを無効または有効にすることはできませんが、ボタンと一緒に使用できます。</span><span class="sxs-lookup"><span data-stu-id="70ea0-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="70ea0-122">MAPI は、変更されたコントロールを更新して通知に応答します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="70ea0-123">MAPI は、コントロールの **GetLastError** メソッドを呼び出します **。Activate** は、コントロール以外のエラーをMAPI_E_USER_CANCEL。</span><span class="sxs-lookup"><span data-stu-id="70ea0-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="70ea0-124">**GetLastError が** _lppMAPIError_ パラメーターの内容で返す [MAPIERROR](mapierror.md)構造体に拡張エラー情報を入れた場合、MAPI はユーザーに対してそれを表示します。</span><span class="sxs-lookup"><span data-stu-id="70ea0-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70ea0-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="70ea0-125">See also</span></span>



[<span data-ttu-id="70ea0-126">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="70ea0-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

