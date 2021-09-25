---
title: 単純な定期的作業アイテムを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 09db0785b8a5d7a895d4d284603a318c623bfcae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604923"
---
# <a name="create-a-simple-recurrent-task-item"></a>単純な定期的作業アイテムを作成する

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI を使用して、タスク アイテムを作成するために作成できます。 このトピックでは、単純な繰り返しタスク アイテムを作成する方法について説明します。
  
このトピックで参照されている MFCMAPI アプリケーションおよび CreateOutlookItemsAddin プロジェクトからコードをダウンロード、表示、実行する方法については、「このセクションで使用されるサンプルのインストール」を参照 [してください](how-to-install-the-samples-used-in-this-section.md)。

### <a name="to-create-a-task-item"></a>タスク アイテムを作成するには

1. メッセージ ストアを開きます。 メッセージ ストアを開く方法については、「メッセージ ストアを開 [く」を参照してください](opening-a-message-store.md)。
    
2. メッセージ ストアの [タスク] フォルダーを開きます。 詳細については、「PR_IPM_TASK_ENTRYID **(** [PidTagIpmTaskEntryId)」を参照してください](pidtagipmtaskentryid-canonical-property.md)。
    
3. タスク フォルダー [の IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、新しいタスク アイテムを作成します。 
    
4. **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) プロパティと、繰り返しタスクを作成するために必要なその他のタスク関連のプロパティを設定します。
    
5. 新しいタスク アイテムを保存します。
    
`AddTask`CreateOutlookItemsAddin プロジェクトの Tasks.cpp ソース ファイル内の関数は、次の手順を示しています。 この関数は、MFCMAPI サンプル アプリケーションの [Addins] メニューの [タスクの追加] をクリックすると表示される [タスクの追加] ダイアログ ボックスからパラメーター `AddTask` を受け取ります。    `DisplayAddTaskDialog`Tasks.cpp の関数はダイアログ ボックスを表示し、ダイアログ ボックスから関数に値を渡 `AddTask` します。 この関数は、MAPI を使用したタスク アイテムの作成には直接関係しないので、ここに  `DisplayAddTaskDialog` は表示されません。 
  
> [!IMPORTANT]
> MFCMAPI アプリケーションのコードでは、[Addins]メニューの [タスクの追加]コマンドをクリックしても、タスク フォルダーが選択された **という保証はありません**。 タスク フォルダー以外のフォルダーにタスク アイテムを作成 **すると、未定義** の動作が発生する可能性があります。 MFCMAPI アプリケーションでタスクの追加コマンドを使用する前に、タスク フォルダーを選択してください。 
  
関数  `AddTask` の一覧を以下に示します。 関数に  _渡される lpFolder_ パラメーターは、新しいタスクが作成されるフォルダーを表す  `AddTask` [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスへのポインターです。 _IMAPIFolder インターフェイス_ を表す **lpFolder** を指定すると、このコードは [IMAPIFolder::CreateMessage メソッドを呼び出](imapifolder-createmessage.md)します。 **CreateMessage メソッド** は、成功コードと IMessage インターフェイスへのポインター **を返** します。 ほとんどの関数コード  `AddTask` は [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備としてプロパティを指定する作業を処理します。 **SetProps** メソッドの呼び出しが成功すると [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、変更をストアにコミットし、新しいタスク アイテムを作成します。 
  
関数  `AddTask` は、名前付きプロパティの数を設定します。 名前付きプロパティの詳細と作成方法については[、「Using MAPI to Create to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)」を参照してください。 タスク アイテムに使用される名前付きプロパティは複数のプロパティ セットを占めるので [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドに渡すパラメーターを構築する場合は注意が必要です。 
  
この  `AddTask` 関数はヘルパー  `BuildWeeklyTaskRecurrencePattern` 関数を使用して **、dispidTaskRecur** プロパティを設定するためのタスクの定期的な構造を構築します。 関数がビルドするタスクの繰り返し構造の詳細については  `BuildWeeklyTaskRecurrencePattern` [、「PidLidTaskRecurrence 標準プロパティ](pidlidtaskrecurrence-canonical-property.md) 」および [「PidLidRecurrencePattern 標準プロパティ」を参照してください](pidlidrecurrencepattern-canonical-property.md)。 

さまざまな繰り返しパターンが可能ですが、この関数は毎週の定期的なパターン  `BuildWeeklyTaskRecurrencePattern` のみを作成します。 また、カレンダーの種類 (グレゴリオ暦)、週の最初の日 (日曜日)、変更または削除されたインスタンスの数 (なし) など、多くの前提に対してハードコードされています。 より一般的な目的の定期的なパターン作成関数は、これらの種類の変数をパラメーターとして受け入れる必要があります。 
  
関数の完全な一覧を次に示  `AddTask` します。 
  
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

- [MAPI を使用して 2007 Outlookアイテムを作成する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

