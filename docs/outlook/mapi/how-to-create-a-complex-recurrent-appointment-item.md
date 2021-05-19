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
# <a name="create-a-complex-recurrent-appointment-item"></a><span data-ttu-id="6cd1a-103">複雑な定期実行予定アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="6cd1a-103">Create a complex recurrent appointment item</span></span>
  
<span data-ttu-id="6cd1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cd1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cd1a-105">MAPI を使用して定期的な予定アイテムを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-105">MAPI can be used to create recurring appointment items.</span></span>
  
<span data-ttu-id="6cd1a-106">このトピックで参照されている MFCMAPI アプリケーションおよび CreateOutlookItemsAddin プロジェクトからコードをダウンロード、表示、実行する方法については、「このセクションで使用されるサンプルのインストール」を参照 [してください](how-to-install-the-samples-used-in-this-section.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-106">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-an-appointment-item"></a><span data-ttu-id="6cd1a-107">予定アイテムを作成するには</span><span class="sxs-lookup"><span data-stu-id="6cd1a-107">To create an appointment item</span></span>

1. <span data-ttu-id="6cd1a-108">メッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-108">Open a message store.</span></span> <span data-ttu-id="6cd1a-109">メッセージ ストアを開く方法については、「メッセージ ストアを開 [く」を参照してください](opening-a-message-store.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-109">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="6cd1a-110">メッセージ ストアで予定表フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-110">Open a Calendar folder in the message store.</span></span> <span data-ttu-id="6cd1a-111">**「PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId)」を参照してください](pidtagipmappointmententryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-111">See **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="6cd1a-112">予定表フォルダー [の IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、新しい予定アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-112">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Calendar folder to create the new appointment item.</span></span> 
    
4. <span data-ttu-id="6cd1a-113">**dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティと、繰り返し予定を作成するために必要なその他のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-113">Set the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property and other properties required to create a recurrent appointment.</span></span>
    
5. <span data-ttu-id="6cd1a-114">新しい予定アイテムを保存します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-114">Save the new appointment item.</span></span>
    
<span data-ttu-id="6cd1a-115">`AddAppointment`CreateOutlookItemsAddin プロジェクトの Appointments.cpp ソース ファイルの関数は、次の手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-115">The  `AddAppointment` function in the Appointments.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="6cd1a-116">関数は、MFCMAPI サンプル アプリケーションの [アドイン] メニューの [予定の追加] をクリックすると表示される [予定の追加] ダイアログ ボックスからパラメーター `AddAppointment` を受け取ります。   </span><span class="sxs-lookup"><span data-stu-id="6cd1a-116">The  `AddAppointment` function takes parameters from the **Add Appointment** dialog box that is displayed when you click **Add Appointment** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="6cd1a-117">`DisplayAddAppointmentDialog`Appointments.cpp の関数はダイアログ ボックスを表示し、ダイアログ ボックスから関数に値を渡 `AddAppointment` します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-117">The  `DisplayAddAppointmentDialog` function in Appointments.cpp displays the dialog box and passes values from the dialog box to the  `AddAppointment` function.</span></span> <span data-ttu-id="6cd1a-118">この関数は、MAPI を使用した予定アイテムの作成とは直接関係ないので、ここに  `DisplayAddAppointmentDialog` は表示されません。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-118">The  `DisplayAddAppointmentDialog` function does not relate directly to creating an appointment item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6cd1a-119">MFCMAPI アプリケーションのコードでは、[アドイン] メニューの [予定の追加] コマンドをクリックしても、予定表フォルダー **が選択されたという保証はありません**。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-119">The code in the MFCMAPI application does not ensure that the **Calendar** folder has been selected when you click the **Add Appointment** command on the **Addins** menu.</span></span> <span data-ttu-id="6cd1a-120">予定表フォルダー以外のフォルダーに予定アイテムを作成 **すると、未定義** の動作が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-120">Creating an appointment item in a folder other than the **Calendar** folder can cause undefined behavior.</span></span> <span data-ttu-id="6cd1a-121">MFCMAPI アプリケーションで [**予定** の追加]コマンドを使用する前に、予定表フォルダーが選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-121">Make sure that you have selected the **Calendar** folder before using the **Add Appointment** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="6cd1a-122">メソッド  `AddAppointment` の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-122">The  `AddAppointment` method is listed below.</span></span> <span data-ttu-id="6cd1a-123">メソッドに  _渡される lpFolder_ パラメーターは、繰り返し予定が作成されるフォルダーを表す  `AddAppointment` [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-123">Note that the  _lpFolder_ parameter passed to the  `AddAppointment` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the recurrent appointment is created.</span></span> <span data-ttu-id="6cd1a-124">_IMAPIFolder インターフェイスを_ 表す **lpFolder** パラメーターを指定すると、このコードは [IMAPIFolder::CreateMessage メソッドを呼び出](imapifolder-createmessage.md)します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-124">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="6cd1a-125">**CreateMessage メソッド** は、成功コードと IMessage インターフェイスへのポインター **を返** します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-125">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="6cd1a-126">ほとんどの関数コード  `AddAppointment` は [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備としてプロパティを指定する作業を処理します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-126">Most of the  `AddAppointment` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="6cd1a-127">**SetProps** メソッドの呼び出しが成功すると [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、変更をストアにコミットし、新しい予定表アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-127">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new calendar item.</span></span> 
  
<span data-ttu-id="6cd1a-128">関数  `AddAppointment` は、名前付きプロパティの数を設定します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-128">The  `AddAppointment` function sets a number of named properties.</span></span> <span data-ttu-id="6cd1a-129">名前付きプロパティの詳細と作成方法については[、「Using MAPI to Create to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-129">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="6cd1a-130">予定アイテムに使用される名前付きプロパティは複数のプロパティ セットを占めるので [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドに渡すパラメーターを構築する場合は注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-130">Because the named properties used for appointment items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="6cd1a-131">この  `AddAppointment` 関数は、いくつかのヘルパー関数を使用して、さまざまな予定関連のプロパティの構造を構築します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-131">The  `AddAppointment` function uses several helper functions to build a structure for various appointment-related properties.</span></span> <span data-ttu-id="6cd1a-132">ヘルパー  `BuildTimeZoneStruct` 関数  `BuildTimeZoneDefinition` とヘルパー関数は、タイム ゾーン関連のプロパティを指定する構造を構築するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-132">The  `BuildTimeZoneStruct` and  `BuildTimeZoneDefinition` helper functions are used to build a structure that specifies the time-zone-related properties.</span></span> <span data-ttu-id="6cd1a-133">タイム ゾーン関連のプロパティは **、dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) **、dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)) **、dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)) **、dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) 、 **および dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)) と、それらは [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)の対応するセクションで説明されています。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-133">The time-zone-related properties are **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)), and **dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), and they are discussed in the corresponding sections of [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> 

<span data-ttu-id="6cd1a-134">`BuildGlobalObjectID`この関数は **、LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) プロパティと **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) プロパティを指定する構造を構築するために使用されます。これは [、[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)の対応するセクションで説明されています。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-134">The  `BuildGlobalObjectID` function is used to build a structure that specifies the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) and **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) properties, which are discussed in the corresponding sections of [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> <span data-ttu-id="6cd1a-135">**dispidApptRecur プロパティを** 指定する構造体は、関数を使用して構築 `BuildWeeklyAppointmentRecurrencePattern` されます。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-135">The structure that specifies the **dispidApptRecur** property is built using the  `BuildWeeklyAppointmentRecurrencePattern` function.</span></span> 

<span data-ttu-id="6cd1a-136">関数によって構築された構造の詳細については  `BuildWeeklyAppointmentRecurrencePattern` [、「PidLidAppointmentRecur 標準プロパティ」を参照してください](pidlidappointmentrecur-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-136">For information about the structure built by the  `BuildWeeklyAppointmentRecurrencePattern` function, see [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="6cd1a-137">さまざまな予定の定期的なパターンを使用できる一方で、関数は週 1 回の予定の定期的なパターン  `BuildWeeklyAppointmentRecurrencePattern` のみを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-137">Note that while a large variety of appointment recurrence patterns are possible, the  `BuildWeeklyAppointmentRecurrencePattern` function only builds a weekly appointment recurrence pattern.</span></span> <span data-ttu-id="6cd1a-138">また、予定表の種類 (グレゴリオ暦)、週の最初の日 (日曜日)、変更または削除されたインスタンスの数 (なし) など、いくつかのハードコードされた値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-138">It also uses several hard-coded values, such as the calendar type (Gregorian), the first day of the week (Sunday), and number of modified or deleted instances (none).</span></span> <span data-ttu-id="6cd1a-139">より汎用的な予定の定期的なパターン作成関数では、これらの種類の変数をパラメーターとして受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-139">A more general purpose appointment recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="6cd1a-140">関数の完全な一覧を次に示  `AddAppointment` します。</span><span class="sxs-lookup"><span data-stu-id="6cd1a-140">The following is the complete listing of the  `AddAppointment` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="6cd1a-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cd1a-141">See also</span></span>

- [<span data-ttu-id="6cd1a-142">MAPI を使用して 2007 Outlookアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="6cd1a-142">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

