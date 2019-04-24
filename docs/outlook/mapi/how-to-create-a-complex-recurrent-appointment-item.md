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
# <a name="create-a-complex-recurrent-appointment-item"></a><span data-ttu-id="aab04-103">複雑な定期実行予定アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="aab04-103">Create a complex recurrent appointment item</span></span>
  
<span data-ttu-id="aab04-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aab04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aab04-105">MAPI を使用して定期的な予定アイテムを作成できます。</span><span class="sxs-lookup"><span data-stu-id="aab04-105">MAPI can be used to create recurring appointment items.</span></span>
  
<span data-ttu-id="aab04-106">このトピックで参照されている mfcmapi アプリケーションおよび createoutlookitemsaddin プロジェクトからコードをダウンロード、表示、および実行する方法については、[このセクションで使用しているサンプルをインストール](how-to-install-the-samples-used-in-this-section.md)するを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aab04-106">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-an-appointment-item"></a><span data-ttu-id="aab04-107">予定アイテムを作成するには</span><span class="sxs-lookup"><span data-stu-id="aab04-107">To create an appointment item</span></span>

1. <span data-ttu-id="aab04-108">メッセージストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="aab04-108">Open a message store.</span></span> <span data-ttu-id="aab04-109">メッセージストアを開く方法については、「[メッセージストアを開く](opening-a-message-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aab04-109">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="aab04-110">メッセージストア内の予定表フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="aab04-110">Open a Calendar folder in the message store.</span></span> <span data-ttu-id="aab04-111">**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aab04-111">See **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="aab04-112">予定表フォルダーの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して、新しい予定アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="aab04-112">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Calendar folder to create the new appointment item.</span></span> 
    
4. <span data-ttu-id="aab04-113">[PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)( \*\*\*\* 定期的な予定を作成するために必要な) プロパティとその他のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="aab04-113">Set the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property and other properties required to create a recurrent appointment.</span></span>
    
5. <span data-ttu-id="aab04-114">新しい予定アイテムを保存します。</span><span class="sxs-lookup"><span data-stu-id="aab04-114">Save the new appointment item.</span></span>
    
<span data-ttu-id="aab04-115">createoutlookitemsaddin プロジェクトの、アポイントソースファイルの関数は、 `AddAppointment`これらの手順を示します。</span><span class="sxs-lookup"><span data-stu-id="aab04-115">The  `AddAppointment` function in the Appointments.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="aab04-116">この`AddAppointment`関数は、mfcmapi サンプルアプリケーションの [ **Addins** ] メニューの [**予定の追加**] をクリックしたときに表示される [**予定の追加**] ダイアログボックスのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="aab04-116">The  `AddAppointment` function takes parameters from the **Add Appointment** dialog box that is displayed when you click **Add Appointment** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="aab04-117">この`DisplayAddAppointmentDialog`関数は、このダイアログボックスを表示して、ダイアログボックスの値を`AddAppointment`関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="aab04-117">The  `DisplayAddAppointmentDialog` function in Appointments.cpp displays the dialog box and passes values from the dialog box to the  `AddAppointment` function.</span></span> <span data-ttu-id="aab04-118">この`DisplayAddAppointmentDialog`関数は MAPI を使用して予定アイテムを作成するには直接関連付けられていないため、ここには記載されていません。</span><span class="sxs-lookup"><span data-stu-id="aab04-118">The  `DisplayAddAppointmentDialog` function does not relate directly to creating an appointment item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aab04-119">mfcmapi アプリケーションのコードでは、 **Addins**メニューの [**予定の追加**] コマンドをクリックしたときに**予定表**フォルダーが選択されているかどうかは確認されません。</span><span class="sxs-lookup"><span data-stu-id="aab04-119">The code in the MFCMAPI application does not ensure that the **Calendar** folder has been selected when you click the **Add Appointment** command on the **Addins** menu.</span></span> <span data-ttu-id="aab04-120">予定**表**フォルダー以外のフォルダーに予定アイテムを作成すると、未定義の動作が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="aab04-120">Creating an appointment item in a folder other than the **Calendar** folder can cause undefined behavior.</span></span> <span data-ttu-id="aab04-121">mfcmapi アプリケーションで [**予定の追加**] コマンドを使用する前に、**予定表**フォルダーが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="aab04-121">Make sure that you have selected the **Calendar** folder before using the **Add Appointment** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="aab04-122">`AddAppointment`メソッドを次に示します。</span><span class="sxs-lookup"><span data-stu-id="aab04-122">The  `AddAppointment` method is listed below.</span></span> <span data-ttu-id="aab04-123">メソッドに渡される_lpfolder_パラメーターは、定期的な予定が作成されたフォルダーを表す[imapifolder](imapifolderimapicontainer.md)インターフェイスへのポインターであることに注意してください。 `AddAppointment`</span><span class="sxs-lookup"><span data-stu-id="aab04-123">Note that the  _lpFolder_ parameter passed to the  `AddAppointment` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the recurrent appointment is created.</span></span> <span data-ttu-id="aab04-124">**imapifolder**インターフェイスを表す_lpfolder_パラメーターを指定すると、コードは[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aab04-124">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="aab04-125">**CreateMessage**メソッドは、成功コードと、 **IMessage**インターフェイスへのポインターへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="aab04-125">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="aab04-126">ほとんどの`AddAppointment`関数コードは、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すための準備として、プロパティを指定する作業を処理します。</span><span class="sxs-lookup"><span data-stu-id="aab04-126">Most of the  `AddAppointment` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="aab04-127">**setprops**メソッドの呼び出しが成功すると、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、変更をストアにコミットし、新しい予定表アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="aab04-127">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new calendar item.</span></span> 
  
<span data-ttu-id="aab04-128">関数`AddAppointment`は、いくつかの名前付きプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="aab04-128">The  `AddAppointment` function sets a number of named properties.</span></span> <span data-ttu-id="aab04-129">名前付きプロパティとその作成方法の詳細については、「 [MAPI を使用して Outlook 2007 アイテムを作成する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aab04-129">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="aab04-130">予定アイテムに使用される名前付きプロパティは複数のプロパティセットを使用するため、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドに渡すパラメーターを構築する場合は、注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="aab04-130">Because the named properties used for appointment items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="aab04-131">関数`AddAppointment`はいくつかのヘルパー関数を使用して、さまざまな予定関連プロパティの構造を構築します。</span><span class="sxs-lookup"><span data-stu-id="aab04-131">The  `AddAppointment` function uses several helper functions to build a structure for various appointment-related properties.</span></span> <span data-ttu-id="aab04-132">`BuildTimeZoneStruct`および`BuildTimeZoneDefinition`ヘルパー関数を使用して、タイムゾーンに関連するプロパティを指定する構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="aab04-132">The  `BuildTimeZoneStruct` and  `BuildTimeZoneDefinition` helper functions are used to build a structure that specifies the time-zone-related properties.</span></span> <span data-ttu-id="aab04-133">タイムゾーンに関連するプロパティは、 **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md))、 **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md))、 **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md))、 **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md))、および**dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)) については、「 [OXOCAL](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)」の対応するセクションに記載されています。</span><span class="sxs-lookup"><span data-stu-id="aab04-133">The time-zone-related properties are **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)), and **dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), and they are discussed in the corresponding sections of [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> 

<span data-ttu-id="aab04-134">この`BuildGlobalObjectID`関数は、 **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) および**dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) プロパティを指定する構造を構築するために使用されます。これについては、対応する[[OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)のセクション。</span><span class="sxs-lookup"><span data-stu-id="aab04-134">The  `BuildGlobalObjectID` function is used to build a structure that specifies the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) and **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) properties, which are discussed in the corresponding sections of [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> <span data-ttu-id="aab04-135">**dispidapptrecur**プロパティを指定する構造体は、 `BuildWeeklyAppointmentRecurrencePattern`関数を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="aab04-135">The structure that specifies the **dispidApptRecur** property is built using the  `BuildWeeklyAppointmentRecurrencePattern` function.</span></span> 

<span data-ttu-id="aab04-136">`BuildWeeklyAppointmentRecurrencePattern`関数によって構築される構造の詳細については、「 [PidLidAppointmentRecur 標準プロパティ](pidlidappointmentrecur-canonical-property.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aab04-136">For information about the structure built by the  `BuildWeeklyAppointmentRecurrencePattern` function, see [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="aab04-137">さまざまな予定の繰り返しパターンが可能ですが、関数は`BuildWeeklyAppointmentRecurrencePattern`週単位の予定の定期的なパターンを作成するだけです。</span><span class="sxs-lookup"><span data-stu-id="aab04-137">Note that while a large variety of appointment recurrence patterns are possible, the  `BuildWeeklyAppointmentRecurrencePattern` function only builds a weekly appointment recurrence pattern.</span></span> <span data-ttu-id="aab04-138">また、カレンダーの種類 (グレゴリオ暦)、週の最初の曜日 (日曜日)、変更または削除されたインスタンスの数 (none) など、ハードコーディングされた値をいくつか使用します。</span><span class="sxs-lookup"><span data-stu-id="aab04-138">It also uses several hard-coded values, such as the calendar type (Gregorian), the first day of the week (Sunday), and number of modified or deleted instances (none).</span></span> <span data-ttu-id="aab04-139">一般的な目的の予定の定期的なパターン作成関数では、これらの種類の変数をパラメーターとして受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="aab04-139">A more general purpose appointment recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="aab04-140">次に、 `AddAppointment`関数の完全な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="aab04-140">The following is the complete listing of the  `AddAppointment` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="aab04-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="aab04-141">See also</span></span>

- [<span data-ttu-id="aab04-142">MAPI を使用して Outlook 2007 アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="aab04-142">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

