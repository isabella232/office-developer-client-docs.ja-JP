---
title: コントロール オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565831"
---
# <a name="control-object-implementation"></a><span data-ttu-id="16e48-103">コントロール オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="16e48-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="16e48-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16e48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16e48-105">オブジェクト、またはサポートしているオブジェクトを制御する、 [IMAPIControl: IUnknown](imapicontroliunknown.md)インタ フェースで、MAPI ダイアログ ボックスに表示されるボタンに機能を追加するのにはプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="16e48-106">コントロール オブジェクトは、ボタンの場合にのみ実装できます。</span><span class="sxs-lookup"><span data-stu-id="16e48-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="16e48-107">**IMAPIControl**には 3 つの方法:[発生しました](imapicontrol-getlasterror.md)、 [GetState](imapicontrol-getstate.md)、および[アクティブ化](imapicontrol-activate.md)します。</span><span class="sxs-lookup"><span data-stu-id="16e48-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="16e48-108">MAPI では、ボタンを無効にするかどうかを判断するのには、 **GetState**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16e48-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="16e48-109">**GetState**は、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="16e48-110">ボタンを表示するダイアログ ボックスが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="16e48-111">テーブルの通知を表示は、ボタンに対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="16e48-112">操作すること、ボタンと MAPI_ENABLED 場合は、ユーザーが対話できる場合は、 _lpulState_パラメーターの内容を MAPI_DISABLED に設定します。</span><span class="sxs-lookup"><span data-stu-id="16e48-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="16e48-113">ユーザーは、ボタンをクリックすると、MAPI は、**ライセンス認証を行う**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16e48-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="16e48-114">**アクティブにする**には、ボタンに関連付けられているタスクが実行されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="16e48-115">このタスクは、プロバイダーには、ダイアログ ボックスを表示する、プロパティを更新するなど、適切なものにできます。</span><span class="sxs-lookup"><span data-stu-id="16e48-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="16e48-116">タスクが失敗した場合、ユーザーがキャンセルされたため、MAPI_E_USER_CANCEL を返します。</span><span class="sxs-lookup"><span data-stu-id="16e48-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="16e48-117">障害の原因は他の適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="16e48-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="16e48-118">タスクが成功し、プロパティの変更] ダイアログ ボックスで別のコントロールに反映されるにリンクされている場合は、 [ITableData::HrNotify](itabledata-hrnotify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16e48-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="16e48-119">**HrNotify**は、 [TABLE_NOTIFICATION](table_notification.md)構造体の**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティがプロパティの変更の通知を表示テーブルを発行するために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="16e48-120">構造に新しいプロパティの値を配置しません。代わりに、 [IMAPIProp::GetProps](imapiprop-getprops.md)が呼び出されたときに、それを返します。</span><span class="sxs-lookup"><span data-stu-id="16e48-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="16e48-121">通常、コントロールを有効または無効にするテーブルの通知を表示を使用することはできませんは、ボタンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="16e48-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="16e48-122">MAPI 通知への応答に変更されたコントロールが更新されます。</span><span class="sxs-lookup"><span data-stu-id="16e48-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="16e48-123">MAPI**をアクティブにする**には、MAPI_E_USER_CANCEL 以外のエラーが返されるときに、コントロールの**GetLastError**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16e48-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="16e48-124">_LppMAPIError_パラメーターの内容で返される[MAPIERROR](mapierror.md)構造体に**発生しました**がエラーの詳細情報を置くと、ユーザーの MAPI 表示します。</span><span class="sxs-lookup"><span data-stu-id="16e48-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16e48-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="16e48-125">See also</span></span>



[<span data-ttu-id="16e48-126">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="16e48-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

