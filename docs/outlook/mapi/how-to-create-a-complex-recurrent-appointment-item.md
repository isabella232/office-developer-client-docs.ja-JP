---
title: 複雑な定期実行予定アイテムを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da9626da-5ba5-4f18-954c-4e23971d23e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d44bf5cccd7e846530eae0c03b8d3ff525f3c012
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344535"
---
# <a name="create-a-complex-recurrent-appointment-item"></a>複雑な定期実行予定アイテムを作成する
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI を使用して定期的な予定アイテムを作成できます。
  
このトピックで参照されている MFCMAPI アプリケーションおよび CreateOutlookItemsAddin プロジェクトからコードをダウンロード、表示、実行する方法については、「このセクションで使用されるサンプルのインストール」を参照 [してください](how-to-install-the-samples-used-in-this-section.md)。

### <a name="to-create-an-appointment-item"></a>予定アイテムを作成するには

1. メッセージ ストアを開きます。 メッセージ ストアを開く方法については、「メッセージ ストアを開 [く」を参照してください](opening-a-message-store.md)。
    
2. メッセージ ストアで予定表フォルダーを開きます。 **「PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId)」を参照してください](pidtagipmappointmententryid-canonical-property.md)。
    
3. 予定表フォルダー [の IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、新しい予定アイテムを作成します。 
    
4. **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティと、繰り返し予定を作成するために必要なその他のプロパティを設定します。
    
5. 新しい予定アイテムを保存します。
    
`AddAppointment`CreateOutlookItemsAddin プロジェクトの Appointments.cpp ソース ファイルの関数は、次の手順を示しています。 関数は、MFCMAPI サンプル アプリケーションの [アドイン] メニューの [予定の追加] をクリックすると表示される [予定の追加] ダイアログ ボックスからパラメーター `AddAppointment` を受け取ります。    `DisplayAddAppointmentDialog`Appointments.cpp の関数はダイアログ ボックスを表示し、ダイアログ ボックスから関数に値を渡 `AddAppointment` します。 この関数は、MAPI を使用した予定アイテムの作成とは直接関係ないので、ここに  `DisplayAddAppointmentDialog` は表示されません。 
  
> [!IMPORTANT]
> MFCMAPI アプリケーションのコードでは、[アドイン] メニューの [予定の追加] コマンドをクリックしても、予定表フォルダー **が選択されたという保証はありません**。 予定表フォルダー以外のフォルダーに予定アイテムを作成 **すると、未定義** の動作が発生する可能性があります。 MFCMAPI アプリケーションで [**予定** の追加]コマンドを使用する前に、予定表フォルダーが選択されている必要があります。 
  
メソッド  `AddAppointment` の一覧を以下に示します。 メソッドに  _渡される lpFolder_ パラメーターは、繰り返し予定が作成されるフォルダーを表す  `AddAppointment` [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスへのポインターです。 _IMAPIFolder インターフェイスを_ 表す **lpFolder** パラメーターを指定すると、このコードは [IMAPIFolder::CreateMessage メソッドを呼び出](imapifolder-createmessage.md)します。 **CreateMessage メソッド** は、成功コードと IMessage インターフェイスへのポインター **を返** します。 ほとんどの関数コード  `AddAppointment` は [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備としてプロパティを指定する作業を処理します。 **SetProps** メソッドの呼び出しが成功すると [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、変更をストアにコミットし、新しい予定表アイテムを作成します。 
  
関数  `AddAppointment` は、名前付きプロパティの数を設定します。 名前付きプロパティの詳細と作成方法については[、「Using MAPI to Create to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)」を参照してください。 予定アイテムに使用される名前付きプロパティは複数のプロパティ セットを占めるので [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドに渡すパラメーターを構築する場合は注意が必要です。 
  
この  `AddAppointment` 関数は、いくつかのヘルパー関数を使用して、さまざまな予定関連のプロパティの構造を構築します。 ヘルパー  `BuildTimeZoneStruct` 関数  `BuildTimeZoneDefinition` とヘルパー関数は、タイム ゾーン関連のプロパティを指定する構造を構築するために使用されます。 タイム ゾーン関連のプロパティは **、dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) **、dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)) **、dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)) **、dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) 、 **および dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)) と、それらは [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)の対応するセクションで説明されています。 

`BuildGlobalObjectID`この関数は **、LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) プロパティと **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) プロパティを指定する構造を構築するために使用されます。これは [、[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)の対応するセクションで説明されています。 **dispidApptRecur プロパティを** 指定する構造体は、関数を使用して構築 `BuildWeeklyAppointmentRecurrencePattern` されます。 

関数によって構築された構造の詳細については  `BuildWeeklyAppointmentRecurrencePattern` [、「PidLidAppointmentRecur 標準プロパティ」を参照してください](pidlidappointmentrecur-canonical-property.md)。 さまざまな予定の定期的なパターンを使用できる一方で、関数は週 1 回の予定の定期的なパターン  `BuildWeeklyAppointmentRecurrencePattern` のみを作成します。 また、予定表の種類 (グレゴリオ暦)、週の最初の日 (日曜日)、変更または削除されたインスタンスの数 (なし) など、いくつかのハードコードされた値を使用します。 より汎用的な予定の定期的なパターン作成関数では、これらの種類の変数をパラメーターとして受け入れる必要があります。 
  
関数の完全な一覧を次に示  `AddAppointment` します。 
  
```cpp
HRESULT AddAppointment(LPMAPIFOLDER lpFolder,
               SYSTEMTIME* lpstStartDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstEndDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstStartFirstUST, // PidLidAppointmentStartWhole, PidLidCommonStart, PR_START_DATE
               SYSTEMTIME* lpstEndFirstUST, // PidLidAppointmentEndWhole, PidLidCommonEnd, PR_END_DATE
               SYSTEMTIME* lpszClipStartUST, // PidLidClipStart
               SYSTEMTIME* lpstClipEndUST, // PidLidClipEnd
               SYSTEMTIME* lpstFirstDOW, // PidLidAppointmentRecur
               DWORD dwStartOffsetLocal, // PidLidAppointmentRecur
               DWORD dwEndOffsetLocal, // PidLidAppointmentRecur
               DWORD dwPeriod, // PidLidAppointmentRecur
               DWORD dwOccurrenceCount, // PidLidAppointmentRecur
               DWORD dwPatternTypeSpecific, // PidLidAppointmentRecur
               ULONG ulDuration, // PidLidAppointmentDuration
               LPWSTR szSubject, // PR_SUBJECT_W
               LPWSTR szLocation, // PidLidLocation
               LPWSTR szPattern) // PidLidRecurrencePattern
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
      MAPINAMEID  rgnmid[ulAppointmentProps];
      LPMAPINAMEID rgpnmid[ulAppointmentProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulAppointmentProps ; i++)
      {
         if (i < ulFirstMeetingProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Appointment;
         else if (i < ulFirstCommonProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Meeting;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulAppointmentProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulAppointmentProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidAppointmentSequence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentSequence],PT_LONG);
         spvProps[p_PidLidBusyStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidBusyStatus],PT_LONG);
         spvProps[p_PidLidLocation].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidLocation],PT_UNICODE);
         spvProps[p_PidLidAppointmentStartWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentStartWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentEndWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentEndWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentDuration].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentDuration],PT_LONG);
         spvProps[p_PidLidAppointmentColor].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentColor],PT_LONG);
         spvProps[p_PidLidResponseStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidResponseStatus],PT_LONG);
         spvProps[p_PidLidRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurring],PT_BOOLEAN);
         spvProps[p_PidLidClipStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipStart],PT_SYSTIME);
         spvProps[p_PidLidClipEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipEnd],PT_SYSTIME);
         spvProps[p_PidLidTimeZoneStruct].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneStruct],PT_BINARY);
         spvProps[p_PidLidTimeZoneDescription].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneDescription],PT_UNICODE);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].ulPropTag
           = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionRecur],
           PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionStartDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionEndDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentRecur].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentRecur],PT_BINARY);
         spvProps[p_PidLidRecurrenceType].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrenceType],PT_LONG);
         spvProps[p_PidLidRecurrencePattern].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrencePattern],PT_UNICODE);
         spvProps[p_PidLidIsRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidIsRecurring],PT_BOOLEAN);
         spvProps[p_PidLidGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCleanGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCleanGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCommonStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonStart],PT_SYSTIME);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidSideEffects].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidSideEffects],PT_LONG);
         spvProps[p_PR_SUBJECT_W].ulPropTag          = PR_SUBJECT_W;
         spvProps[p_PR_START_DATE].ulPropTag         = PR_START_DATE;
         spvProps[p_PR_END_DATE].ulPropTag           = PR_END_DATE;
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag    = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag         = PR_ICON_INDEX;
         spvProps[p_PR_CONVERSATION_INDEX].ulPropTag   = PR_CONVERSATION_INDEX;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag      = PR_MESSAGE_FLAGS;
         spvProps[p_PidLidAppointmentSequence].Value.l = 0;
         spvProps[p_PidLidBusyStatus].Value.l = olBusy;
         spvProps[p_PidLidLocation].Value.lpszW = szLocation;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidAppointmentStartWhole].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidAppointmentEndWhole].Value.ft);
         spvProps[p_PidLidAppointmentDuration].Value.l = ulDuration;
         spvProps[p_PidLidAppointmentColor].Value.l = 0; // No color
         spvProps[p_PidLidResponseStatus].Value.l = respNone;
         spvProps[p_PidLidRecurring].Value.b = true;
         SystemTimeToFileTime(lpszClipStartUST,&spvProps[p_PidLidClipStart].Value.ft);
         SystemTimeToFileTime(lpstClipEndUST,&spvProps[p_PidLidClipEnd].Value.ft);
         SYSTEMTIME stStandard = {0};
         stStandard.wMonth = 0xB;
         stStandard.wDay = 0x1;
         stStandard.wHour = 0x2;
         SYSTEMTIME stDaylight = {0};
         stDaylight.wMonth = 0x3;
         stDaylight.wDay = 0x2;
         stDaylight.wHour = 0x2;
         hRes = BuildTimeZoneStruct(
            300,
            0,
            (DWORD)-60,
            &stStandard,
            &stDaylight,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.cb,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb);
         spvProps[p_PidLidTimeZoneDescription].Value.lpszW = L"(GMT-05:00) Eastern Time (US & Canada)";
         SYSTEMTIME stRule1Standard = {0};
         stRule1Standard.wMonth = 0xA;
         stRule1Standard.wDay = 0x5;
         stRule1Standard.wHour = 0x2;
         SYSTEMTIME stRule1Daylight = {0};
         stRule1Daylight.wMonth = 0x4;
         stRule1Daylight.wDay = 0x1;
         stRule1Daylight.wHour = 0x2;
         if (SUCCEEDED(hRes)) hRes = BuildTimeZoneDefinition(
            L"Eastern Standard Time",
            0, // TZRule Flags
            2006, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stRule1Standard, // stStandardDate
            &stRule1Daylight, // stDaylightDate
            TZRULE_FLAG_EFFECTIVE_TZREG, // TZRule Flags
            2007, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stStandard, // stStandardDate
            &stDaylight, // stDaylightDate
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         if (SUCCEEDED(hRes)) hRes = BuildWeeklyAppointmentRecurrencePattern(
            lpstStartDateLocal,
            lpstEndDateLocal,
            lpstFirstDOW,
            dwStartOffsetLocal,
            dwEndOffsetLocal,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.lpb);
         spvProps[p_PidLidRecurrenceType].Value.l = rectypeWeekly;
         spvProps[p_PidLidRecurrencePattern].Value.lpszW = szPattern;
         spvProps[p_PidLidIsRecurring].Value.b = true;
         if (SUCCEEDED(hRes)) hRes = BuildGlobalObjectId(
            &spvProps[p_PidLidGlobalObjectId].Value.bin.cb,
            &spvProps[p_PidLidGlobalObjectId].Value.bin.lpb);
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.cb  = spvProps[p_PidLidGlobalObjectId].Value.bin.cb;
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.lpb = spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidCommonStart].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidSideEffects].Value.l
            = seOpenToDelete | seOpenToCopy | seOpenToMove | seCoerceToInbox | seOpenForCtxMenu;
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PR_START_DATE].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PR_END_DATE].Value.ft);
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Appointment";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x00000401; // Recurring Appointment
         if (SUCCEEDED(hRes)) hRes = BuildConversationIndex(
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         if (SUCCEEDED(hRes)) hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SaveChanges(FORCE_SAVE);
         }
         if (spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb)
            delete[] spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb;
         if (spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionStartDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionEndDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         if (spvProps[p_PidLidAppointmentRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentRecur].Value.bin.lpb;
         if (spvProps[p_PidLidGlobalObjectId].Value.bin.lpb)
            delete[] spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         // Do not delete p_PidLidCleanGlobalObjectId, it was borrowed from p_PidLidGlobalObjectId
         if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
            delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a>関連項目

- [MAPI を使用して 2007 Outlookアイテムを作成する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

