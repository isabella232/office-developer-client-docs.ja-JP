---
title: 単純な定期的作業アイテムを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345473"
---
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="6ce18-103">単純な定期的作業アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="6ce18-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="6ce18-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ce18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ce18-105">MAPI を使用して、タスク アイテムを作成するために作成できます。</span><span class="sxs-lookup"><span data-stu-id="6ce18-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="6ce18-106">このトピックでは、単純な繰り返しタスク アイテムを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="6ce18-107">このトピックで参照されている MFCMAPI アプリケーションおよび CreateOutlookItemsAddin プロジェクトからコードをダウンロード、表示、実行する方法については、「このセクションで使用されるサンプルのインストール」を参照 [してください](how-to-install-the-samples-used-in-this-section.md)。</span><span class="sxs-lookup"><span data-stu-id="6ce18-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="6ce18-108">タスク アイテムを作成するには</span><span class="sxs-lookup"><span data-stu-id="6ce18-108">To create a task item</span></span>

1. <span data-ttu-id="6ce18-109">メッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="6ce18-109">Open a message store.</span></span> <span data-ttu-id="6ce18-110">メッセージ ストアを開く方法については、「メッセージ ストアを開 [く」を参照してください](opening-a-message-store.md)。</span><span class="sxs-lookup"><span data-stu-id="6ce18-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="6ce18-111">メッセージ ストアの [タスク] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="6ce18-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="6ce18-112">詳細については、「PR_IPM_TASK_ENTRYID **(** [PidTagIpmTaskEntryId)」を参照してください](pidtagipmtaskentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="6ce18-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="6ce18-113">タスク フォルダー [の IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、新しいタスク アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="6ce18-114">**dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) プロパティと、繰り返しタスクを作成するために必要なその他のタスク関連のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="6ce18-115">新しいタスク アイテムを保存します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-115">Save the new task item.</span></span>
    
<span data-ttu-id="6ce18-116">`AddTask`CreateOutlookItemsAddin プロジェクトの Tasks.cpp ソース ファイル内の関数は、次の手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="6ce18-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="6ce18-117">この関数は、MFCMAPI サンプル アプリケーションの [Addins] メニューの [タスクの追加] をクリックすると表示される [タスクの追加] ダイアログ ボックスからパラメーター `AddTask` を受け取ります。   </span><span class="sxs-lookup"><span data-stu-id="6ce18-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="6ce18-118">`DisplayAddTaskDialog`Tasks.cpp の関数はダイアログ ボックスを表示し、ダイアログ ボックスから関数に値を渡 `AddTask` します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="6ce18-119">この関数は、MAPI を使用したタスク アイテムの作成には直接関係しないので、ここに  `DisplayAddTaskDialog` は表示されません。</span><span class="sxs-lookup"><span data-stu-id="6ce18-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6ce18-120">MFCMAPI アプリケーションのコードでは、[Addins]メニューの [タスクの追加]コマンドをクリックしても、タスク フォルダーが選択された **という保証はありません**。</span><span class="sxs-lookup"><span data-stu-id="6ce18-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="6ce18-121">タスク フォルダー以外のフォルダーにタスク アイテムを作成 **すると、未定義** の動作が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ce18-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="6ce18-122">MFCMAPI アプリケーションでタスクの追加コマンドを使用する前に、タスク フォルダーを選択してください。</span><span class="sxs-lookup"><span data-stu-id="6ce18-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="6ce18-123">関数  `AddTask` の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="6ce18-124">関数に  _渡される lpFolder_ パラメーターは、新しいタスクが作成されるフォルダーを表す  `AddTask` [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6ce18-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="6ce18-125">_IMAPIFolder インターフェイス_ を表す **lpFolder** を指定すると、このコードは [IMAPIFolder::CreateMessage メソッドを呼び出](imapifolder-createmessage.md)します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="6ce18-126">**CreateMessage メソッド** は、成功コードと IMessage インターフェイスへのポインター **を返** します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="6ce18-127">ほとんどの関数コード  `AddTask` は [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備としてプロパティを指定する作業を処理します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="6ce18-128">**SetProps** メソッドの呼び出しが成功すると [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、変更をストアにコミットし、新しいタスク アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="6ce18-129">関数  `AddTask` は、名前付きプロパティの数を設定します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="6ce18-130">名前付きプロパティの詳細と作成方法については [、「USING MAPI to Create Outlook 2007 Items」を参照してください](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6ce18-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="6ce18-131">タスク アイテムに使用される名前付きプロパティは複数のプロパティ セットを占めるので [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドに渡すパラメーターを構築する場合は注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="6ce18-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="6ce18-132">この  `AddTask` 関数はヘルパー  `BuildWeeklyTaskRecurrencePattern` 関数を使用して **、dispidTaskRecur** プロパティを設定するためのタスクの定期的な構造を構築します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="6ce18-133">関数がビルドするタスクの繰り返し構造の詳細については  `BuildWeeklyTaskRecurrencePattern` [、「PidLidTaskRecurrence 標準プロパティ](pidlidtaskrecurrence-canonical-property.md) 」および [「PidLidRecurrencePattern 標準プロパティ」を参照してください](pidlidrecurrencepattern-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="6ce18-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="6ce18-134">さまざまな繰り返しパターンが可能ですが、この関数は毎週の定期的なパターン  `BuildWeeklyTaskRecurrencePattern` のみを作成します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="6ce18-135">また、カレンダーの種類 (グレゴリオ暦)、週の最初の日 (日曜日)、変更または削除されたインスタンスの数 (なし) など、多くの前提に対してハードコードされています。</span><span class="sxs-lookup"><span data-stu-id="6ce18-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="6ce18-136">より一般的な目的の定期的なパターン作成関数は、これらの種類の変数をパラメーターとして受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ce18-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="6ce18-137">関数の完全な一覧を次に示  `AddTask` します。</span><span class="sxs-lookup"><span data-stu-id="6ce18-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
```cpp
HRESULT AddTask(LPMAPIFOLDER lpFolder,
            SYSTEMTIME* lpstStart, // PidLidCommonEnd, PidLidTaskDueDate, PidLidTaskRecurrence
            SYSTEMTIME* lpstEnd, // PidLidTaskRecurrence
            SYSTEMTIME* lpstFirstDOW, // PidLidTaskRecurrence
            DWORD dwPeriod, // PidLidTaskRecurrence
            DWORD dwOccurrenceCount, // PidLidTaskRecurrence
            DWORD dwPatternTypeSpecific, // PidLidTaskRecurrence
            LPWSTR szSubject, // PR_SUBJECT_W
            LPWSTR szBody) // PR_BODY_W
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulTaskProps];
      LPMAPINAMEID rgpnmid[ulTaskProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulTaskProps ; i++)
      {
         if (i < ulFirstTaskProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Task;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulTaskProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulTaskProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidTaskMode].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskMode],PT_LONG);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidTaskStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskStatus],PT_LONG);
         spvProps[p_PidLidPercentComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidPercentComplete],PT_DOUBLE);
         spvProps[p_PidLidTaskState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskState],PT_LONG);
         spvProps[p_PidLidTaskRecurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskRecurrence],PT_BINARY);
         spvProps[p_PidLidTaskDeadOccurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDeadOccurrence],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwner].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwner],PT_UNICODE);
         spvProps[p_PidLidTaskFRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFRecurring],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwnership].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwnership],PT_LONG);
         spvProps[p_PidLidTaskAcceptanceState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskAcceptanceState],PT_LONG);
         spvProps[p_PidLidTaskFFixOffline].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFFixOffline],PT_BOOLEAN);
         spvProps[p_PidLidTaskDueDate].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDueDate],PT_SYSTIME);
         spvProps[p_PidLidTaskComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskComplete],PT_SYSTIME);
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag   = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag        = PR_ICON_INDEX;
         spvProps[p_PR_SUBJECT_W].ulPropTag         = PR_SUBJECT_W;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag     = PR_MESSAGE_FLAGS;
         spvProps[p_PR_BODY_W].ulPropTag            = PR_BODY_W;
         spvProps[p_PidLidTaskMode].Value.l = tdmtNothing;
         SYSTEMTIME stStartUTC = {0};
         TzSpecificLocalTimeToSystemTime(NULL,lpstStart,&stStartUTC);
         SystemTimeToFileTime(&stStartUTC,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidTaskStatus].Value.l = tsvNotStarted;
         spvProps[p_PidLidPercentComplete].Value.dbl = 0.0;
         spvProps[p_PidLidTaskState].Value.l = tdsOWNNEW;
         spvProps[p_PidLidTaskDeadOccurrence].Value.b = false;
         spvProps[p_PidLidTaskOwner].Value.lpszW = L"Unknown";
         spvProps[p_PidLidTaskFRecurring].Value.b = true;
         spvProps[p_PidLidTaskOwnership].Value.l = tovNew;
         spvProps[p_PidLidTaskAcceptanceState].Value.l = tdvNone;
         spvProps[p_PidLidTaskFFixOffline].Value.b = true;
         SystemTimeToFileTime(lpstStart,&spvProps[p_PidLidTaskDueDate].Value.ft);
         spvProps[p_PidLidTaskComplete].Value.b = false;
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Task";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x501; // Unassigned Recurring Task
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         spvProps[p_PR_BODY_W].Value.lpszW = szBody;
         hRes = BuildWeeklyTaskRecurrencePattern(
            lpstStart,
            lpstEnd,
            lpstFirstDOW,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.cb,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.lpb);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
            if (SUCCEEDED(hRes))
            {
               hRes = lpMessage->SaveChanges(FORCE_SAVE);
            }
         }
         if (spvProps[p_PidLidTaskRecurrence].Value.bin.lpb)
            delete[] spvProps[p_PidLidTaskRecurrence].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a><span data-ttu-id="6ce18-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ce18-138">See also</span></span>

- [<span data-ttu-id="6ce18-139">MAPI を使用して Outlook 2007 アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="6ce18-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

