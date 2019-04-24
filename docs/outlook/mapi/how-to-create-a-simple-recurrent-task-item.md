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
# <a name="create-a-simple-recurrent-task-item"></a>単純な定期的作業アイテムを作成する

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI を使用して、タスクアイテムを作成することができます。 このトピックでは、単純な定期的なタスクアイテムを作成する方法について説明します。
  
このトピックで参照されている mfcmapi アプリケーションおよび createoutlookitemsaddin プロジェクトからコードをダウンロード、表示、および実行する方法については、[このセクションで使用しているサンプルをインストール](how-to-install-the-samples-used-in-this-section.md)するを参照してください。

### <a name="to-create-a-task-item"></a>タスクアイテムを作成するには

1. メッセージストアを開きます。 メッセージストアを開く方法については、「[メッセージストアを開く](opening-a-message-store.md)」を参照してください。
    
2. メッセージストアの [タスク] フォルダーを開きます。 詳細については、「 **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))」を参照してください。
    
3. 新しいタスクアイテムを作成するには、[タスク] フォルダーの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 
    
4. タスクを繰り返し作成するために必要な、 **dispidtaskrecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) プロパティおよびその他のタスク関連のプロパティを設定します。
    
5. 新しいタスクアイテムを保存します。
    
createoutlookitemsaddin プロジェクトの Tasks ソースファイルの関数は、 `AddTask`これらの手順を示しています。 この`AddTask`関数は、mfcmapi サンプルアプリケーションの [ **Addins** ] メニューの [**タスクの追加**] をクリックしたときに表示される [**タスクの追加**] ダイアログボックスのパラメーターを受け取ります。 タスク`DisplayAddTaskDialog` .cpp の関数は、ダイアログボックスを表示し、ダイアログボックスの値を`AddTask`関数に渡します。 この`DisplayAddTaskDialog`関数は MAPI を使用したタスクアイテムの作成に直接関連付けられていないため、ここには記載されていません。 
  
> [!IMPORTANT]
> mfcmapi アプリケーションのコードでは、 **Addins**メニューの [**タスクの追加**] コマンドをクリックしたときに、 **Tasks**フォルダーが選択されているかどうかは確認されません。 タスクフォルダー以外のフォルダーにタスクアイテムを**** 作成すると、未定義の動作が発生することがあります。 mfcmapi アプリケーションの [**タスクの追加**] コマンドを使用する前に、 **Tasks**フォルダーが選択されていることを確認してください。 
  
`AddTask`関数は以下のとおりです。 関数に渡される_lpfolder_パラメーターは、新しいタスクが作成されるフォルダーを表す[imapifolder](imapifolderimapicontainer.md)インターフェイスへのポインターであることに注意してください。 `AddTask` **imapifolder**インターフェイスを表す_lpfolder_を指定すると、コードは[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 **CreateMessage**メソッドは、成功コードと、 **IMessage**インターフェイスへのポインターへのポインターを返します。 ほとんどの`AddTask`関数コードは、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すための準備として、プロパティを指定する作業を処理します。 **setprops**メソッドの呼び出しが成功すると、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、変更をストアにコミットし、新しいタスクアイテムを作成します。 
  
関数`AddTask`は、いくつかの名前付きプロパティを設定します。 名前付きプロパティとその作成方法の詳細については、「 [MAPI を使用して Outlook 2007 アイテムを作成する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)」を参照してください。 タスクアイテムに使用される名前付きプロパティは複数のプロパティセットを使用するため、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドに渡すパラメーターを構築するときは、注意を払う必要があります。 
  
この`AddTask`関数は、 `BuildWeeklyTaskRecurrencePattern` **dispidtaskrecur**プロパティを設定するためのタスクの繰り返しを表す構造を作成するために、ヘルパー関数を使用します。 関数によっ`BuildWeeklyTaskRecurrencePattern`て作成されるタスクの繰り返し構造の詳細については、「 [PidLidTaskRecurrence 標準プロパティ](pidlidtaskrecurrence-canonical-property.md)と[PidLidRecurrencePattern 標準プロパティ](pidlidrecurrencepattern-canonical-property.md)」を参照してください。 

さまざまな定期的なパターンが可能ですが、関数は`BuildWeeklyTaskRecurrencePattern`週単位の定期的なパターンを作成するだけです。 また、予定表の種類 (グレゴリオ暦)、週の最初の曜日 (日曜日)、変更または削除されたインスタンスの数 (none) など、さまざまな前提条件に対してハードコーディングされています。 一般的な目的パターン作成関数では、これらの種類の変数をパラメーターとして受け入れる必要があります。 
  
次に、 `AddTask`関数の完全な一覧を示します。 
  
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

## <a name="see-also"></a>関連項目

- [MAPI を使用して Outlook 2007 アイテムを作成する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

