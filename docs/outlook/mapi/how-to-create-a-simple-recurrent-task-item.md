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
ms.openlocfilehash: 68d7472f993bcc35abbd4b733bae9f137b948608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576842"
---
# <a name="create-a-simple-recurrent-task-item"></a>単純な繰り返しのタスク アイテムを作成します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
タスク アイテムを作成する作成するのには、MAPI を使用できます。 このトピックでは、単純な繰り返しのタスク項目を作成する方法について説明します。
  
ダウンロード、表示、および、MFCMAPI アプリケーションと CreateOutlookItemsAddin にこのトピックで参照されるプロジェクトからコードを実行する方法の詳細については、[このセクションで使用されるサンプルのインストール](how-to-install-the-samples-used-in-this-section.md)を参照してください。

### <a name="to-create-a-task-item"></a>タスク項目を作成するには

1. メッセージ ストアを開きます。 メッセージ ストアを開く方法の詳細については、[メッセージ ストアを開く](opening-a-message-store.md)を参照してください。
    
2. メッセージ ・ ストア内の [仕事] フォルダーを開きます。 詳細については、 **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)) を参照してください。
    
3. 新規タスク アイテムを作成するのには [タスク] フォルダーには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 
    
4. **DispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) のプロパティは、定期的なタスクを作成するために必要なその他のタスクに関連するプロパティを設定します。
    
5. 新規タスク アイテムを保存します。
    
`AddTask` CreateOutlookItemsAddin プロジェクトの Tasks.cpp のソース ファイル内の関数は、次の手順を示します。 `AddTask`関数は、MFCMAPI サンプル アプリケーションの [**アドイン**] メニューの [**タスクの追加**をクリックすると表示される [**タスクの追加**] ダイアログ ボックスからパラメーターを受け取ります。 `DisplayAddTaskDialog` Tasks.cpp で関数は、ダイアログ ボックスが表示され、ダイアログ ボックスから値が渡されます、`AddTask`関数です。 `DisplayAddTaskDialog`関数がここで記載されていないために、MAPI を使用して作業項目を作成するのには直接関係ありません。 
  
> [!IMPORTANT]
> MFCMAPI アプリケーション内のコードでは、[**アドイン**] メニューの**タスクの追加**] をクリックすると **[仕事**] フォルダーが選択されているは確保されません。 **[仕事**] フォルダー以外のフォルダーに仕事アイテムを作成すると、未定義の動作が発生することができます。 MFCMAPI アプリケーションで、[**タスクの追加**] コマンドを使用する前に、[**タスク**] フォルダーを選択していることを確認します。 
  
`AddTask`関数は、下に表示されます。 _LpFolder_パラメーターが渡されることに注意、`AddTask`関数は、新しいタスクが作成されるフォルダーを表す[IMAPIFolder](imapifolderimapicontainer.md)インターフェイスへのポインター。 コードは、 **IMAPIFolder**インターフェイスを表す_lpFolder_を指定するには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 **メイル**メソッドは、 **IMessage**インターフェイスへのポインターへの成功コードとポインターを返します。 ほとんどの`AddTask`関数のコードは、プロパティを指定する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すための準備としての作業を行っています。 **SetProps**メソッドの呼び出しが成功した場合、ストアに変更をコミットし、新しい作業項目を作成する[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されます。 
  
`AddTask`関数は、いくつかの名前付きプロパティを設定します。 名前付きプロパティと作成方法については、 [Outlook 2007 のアイテムの作成に MAPI を使用する](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)を参照してください。 作業項目に使用する名前付きプロパティが複数のプロパティ セットを占有するため注意する必要があるパラメーターを作成するとき[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドに渡されます。 
  
`AddTask`機能は、 `BuildWeeklyTaskRecurrencePattern` 、 **dispidTaskRecur**プロパティを設定するために定期的な仕事を表す構造を構築するヘルパー関数です。 タスクの繰り返し構造については、`BuildWeeklyTaskRecurrencePattern`ビルドの機能、[標準的なプロパティの PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)と[PidLidRecurrencePattern の標準的なプロパティ](pidlidrecurrencepattern-canonical-property.md)を参照してください。 

定期的なパターンにさまざまなことが可能であれば、メモ、`BuildWeeklyTaskRecurrencePattern`関数は、毎週の定期的なパターンだけをビルドします。 ハード コーディングされているいくつかの前提条件、カレンダーの種類 (グレゴリオ暦)、最初の日曜日 (日曜日)、および (なし)、変更または削除されたインスタンスの数です。 一般的な目的定期的なパターンの作成機能は、この種のパラメーターとして変数をそのまま使用する必要があります。 
  
次の完全な一覧では、`AddTask`関数です。 
  
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

- [MAPI を使用して Outlook 2007 のアイテムを作成するには](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

