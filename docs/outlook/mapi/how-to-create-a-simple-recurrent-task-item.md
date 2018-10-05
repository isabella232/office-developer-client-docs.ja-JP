---
title: 単純な繰り返しのタスク アイテムを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394343"
---
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="a9ad5-103">単純な繰り返しのタスク アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="a9ad5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9ad5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9ad5-105">タスク アイテムを作成する作成するのには、MAPI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="a9ad5-106">このトピックでは、単純な繰り返しのタスク項目を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="a9ad5-107">ダウンロード、表示、および、MFCMAPI アプリケーションと CreateOutlookItemsAddin にこのトピックで参照されるプロジェクトからコードを実行する方法の詳細については、[このセクションで使用されるサンプルのインストール](how-to-install-the-samples-used-in-this-section.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="a9ad5-108">タスク項目を作成するには</span><span class="sxs-lookup"><span data-stu-id="a9ad5-108">To create a task item</span></span>

1. <span data-ttu-id="a9ad5-109">メッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-109">Open a message store.</span></span> <span data-ttu-id="a9ad5-110">メッセージ ストアを開く方法の詳細については、[メッセージ ストアを開く](opening-a-message-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="a9ad5-111">メッセージ ・ ストア内の [仕事] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="a9ad5-112">詳細については、 **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="a9ad5-113">新規タスク アイテムを作成するのには [タスク] フォルダーには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="a9ad5-114">**DispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) のプロパティは、定期的なタスクを作成するために必要なその他のタスクに関連するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="a9ad5-115">新規タスク アイテムを保存します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-115">Save the new task item.</span></span>
    
<span data-ttu-id="a9ad5-116">`AddTask` CreateOutlookItemsAddin プロジェクトの Tasks.cpp のソース ファイル内の関数は、次の手順を示します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="a9ad5-117">`AddTask`関数は、MFCMAPI サンプル アプリケーションの [**アドイン**] メニューの [**タスクの追加**をクリックすると表示される [**タスクの追加**] ダイアログ ボックスからパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="a9ad5-118">`DisplayAddTaskDialog` Tasks.cpp で関数は、ダイアログ ボックスが表示され、ダイアログ ボックスから値が渡されます、`AddTask`関数です。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="a9ad5-119">`DisplayAddTaskDialog`関数がここで記載されていないために、MAPI を使用して作業項目を作成するのには直接関係ありません。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a9ad5-120">MFCMAPI アプリケーション内のコードでは、[**アドイン**] メニューの**タスクの追加**] をクリックすると **[仕事**] フォルダーが選択されているは確保されません。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="a9ad5-121">**[仕事**] フォルダー以外のフォルダーに仕事アイテムを作成すると、未定義の動作が発生することができます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="a9ad5-122">MFCMAPI アプリケーションで、[**タスクの追加**] コマンドを使用する前に、[**タスク**] フォルダーを選択していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="a9ad5-123">`AddTask`関数は、下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="a9ad5-124">_LpFolder_パラメーターが渡されることに注意、`AddTask`関数は、新しいタスクが作成されるフォルダーを表す[IMAPIFolder](imapifolderimapicontainer.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="a9ad5-125">コードは、 **IMAPIFolder**インターフェイスを表す_lpFolder_を指定するには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="a9ad5-126">**メイル**メソッドは、 **IMessage**インターフェイスへのポインターへの成功コードとポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="a9ad5-127">ほとんどの`AddTask`関数のコードは、プロパティを指定する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すための準備としての作業を行っています。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="a9ad5-128">**SetProps**メソッドの呼び出しが成功した場合、ストアに変更をコミットし、新しい作業項目を作成する[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="a9ad5-129">`AddTask`関数は、いくつかの名前付きプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="a9ad5-130">名前付きプロパティと作成方法については、 [Outlook 2007 のアイテムの作成に MAPI を使用する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="a9ad5-131">作業項目に使用する名前付きプロパティが複数のプロパティ セットを占有するため注意する必要があるパラメーターを作成するとき[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="a9ad5-132">`AddTask`機能は、 `BuildWeeklyTaskRecurrencePattern` 、 **dispidTaskRecur**プロパティを設定するために定期的な仕事を表す構造を構築するヘルパー関数です。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="a9ad5-133">タスクの繰り返し構造については、`BuildWeeklyTaskRecurrencePattern`ビルドの機能、[標準的なプロパティの PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)と[PidLidRecurrencePattern の標準的なプロパティ](pidlidrecurrencepattern-canonical-property.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="a9ad5-134">定期的なパターンにさまざまなことが可能であれば、メモ、`BuildWeeklyTaskRecurrencePattern`関数は、毎週の定期的なパターンだけをビルドします。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="a9ad5-135">ハード コーディングされているいくつかの前提条件、カレンダーの種類 (グレゴリオ暦)、最初の日曜日 (日曜日)、および (なし)、変更または削除されたインスタンスの数です。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="a9ad5-136">一般的な目的定期的なパターンの作成機能は、この種のパラメーターとして変数をそのまま使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="a9ad5-137">次の完全な一覧では、`AddTask`関数です。</span><span class="sxs-lookup"><span data-stu-id="a9ad5-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a9ad5-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9ad5-138">See also</span></span>

- [<span data-ttu-id="a9ad5-139">MAPI を使用して Outlook 2007 のアイテムを作成するには</span><span class="sxs-lookup"><span data-stu-id="a9ad5-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

