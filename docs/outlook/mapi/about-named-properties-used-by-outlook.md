---
title: Outlook で使用される名前付きプロパティについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '最終更新日: 2012 年 6 月 25 日'
ms.openlocfilehash: 328ff423025689795669d661f529270886123a7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322240"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="fba68-103">Outlook で使用される名前付きプロパティについて</span><span class="sxs-lookup"><span data-stu-id="fba68-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="fba68-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fba68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fba68-p101">MAPI は、特定のプロパティに名前を割り当て、これらの名前を一意識別子にマッピングし、この名前から識別子へのマッピングをセッション間で永続化するための機能を提供します。名前付きプロパティは、プロパティ セットの名前とグローバル一意識別子 (GUID) によって識別されます。名前には、数値または文字列を使用することができます。Microsoft Outlook 2013 または Microsoft Outlook 2010 のプロパティ セットの多くは、**PSETID_Appointment** などの、Outlook 2013 または Outlook 2010 で定義された名前空間です。</span><span class="sxs-lookup"><span data-stu-id="fba68-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="fba68-p102">名前付きプロパティは、[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 関数や [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) 関数を使って操作されます。名前とプロパティ セット GUID は [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 関数に回されて、現在の MAPI セッションに有効なプロパティ識別子を取得します。プロパティ識別子はコンピューター端末によって異なることがあるため、名前付きのプロパティに一貫してアクセスする唯一の方法は、そのプロパティの名前とプロパティ セット GUID を知ることです。識別子の範囲は常に 0x8000 から 0xFFFE の間です。</span><span class="sxs-lookup"><span data-stu-id="fba68-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="fba68-p103">[IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトはすべて、名前付きプロパティをサポートすることができます。具体的には、MAPI サービス プロバイダーまたは MAPI クライアントは [IMAPIProp::GetProps](imapiprop-getprops.md) を実装して、名前付きプロパティの値を取得する必要があります。Outlook 2013 または Outlook 2010 で使用される名前付きプロパティの設定はサポートされていません。これは、他の MAPI プロバイダーまたはクライアントと共有されるデータが破損する危険があるためです。</span><span class="sxs-lookup"><span data-stu-id="fba68-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="fba68-p104">Outlook 2013 と Outlook 2010 では、MAPI の名前付きプロパティを使用して、添付ファイルのセキュリティや会議の代替日時の提案などのさまざまな機能を実装しています。Outlook 2013 と Outlook 2010 は、この基盤となるデータ上で、Outlook 2013 と Outlook 2010 のオブジェクト モデルのアイテム プロパティとして、これらのプロパティの一部を公開しています。たとえば、オブジェクト モデル内の **ContactItem** オブジェクトである **Email1Address** プロパティは、**PSETID_Address** 名前空間にある名前付きの [PidLidEmail1EmailAddress 標準プロパティ](pidlidemail1emailaddress-canonical-property.md)に対応します。しかし、一般に、互換性とデータの整合性に対する懸念から、Outlook 2013 と Outlook 2010 で使用される MAPI プロパティの多くはオブジェクト モデルに公開されていません。</span><span class="sxs-lookup"><span data-stu-id="fba68-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="fba68-120">このリファレンスでは、以下に列挙する多数の名前付きプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fba68-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="fba68-121">**PSETID_Address** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-122">PidLidEmail1AddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="fba68-123">PidLidEmail1EmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="fba68-124">PidLidEmail1OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="fba68-125">PidLidEmail2AddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="fba68-126">PidLidEmail2DisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="fba68-127">PidLidEmail2EmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="fba68-128">PidLidEmail2OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="fba68-129">PidLidEmail2OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="fba68-130">PidLidEmail3AddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="fba68-131">PidLidEmail3DisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="fba68-132">PidLidEmail3EmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="fba68-133">PidLidEmail3OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="fba68-134">PidLidEmail3OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="fba68-135">PidLidEmail1DisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="fba68-136">PidLidEmail1OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="fba68-137">PidLidFileUnder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="fba68-138">PidLidInstantMessagingAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="fba68-139">PidLidWorkAddressCity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="fba68-140">PidLidWorkAddressCountry 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="fba68-141">PidLidWorkAddressPostalCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="fba68-142">PidLidWorkAddressPostOfficeBox 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="fba68-143">PidLidWorkAddressState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="fba68-144">PidLidWorkAddressStreet 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="fba68-145">PidLidYomiCompanyName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="fba68-146">PidLidYomiFirstName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="fba68-147">PidLidYomiLastName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="fba68-148">**PSETID_Appointment** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-149">PidLidAllAttendeesString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="fba68-150">PidLidAppointmentCounterProposal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="fba68-151">PidLidAppointmentDuration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="fba68-152">PidLidAppointmentEndWhole 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="fba68-153">PidLidAppointmentStartWhole 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="fba68-154">PidLidBusyStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="fba68-155">PidLidCcAttendeesString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="fba68-156">PidLidLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="fba68-157">PidLidRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="fba68-158">PidLidToAttendeesString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="fba68-159">**PSETID_Common** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-160">PidLidCommonEnd 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="fba68-161">PidLidCommonStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="fba68-162">PidLidCompanies 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="fba68-163">PidLidContacts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="fba68-164">PidLidCustomFlag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="fba68-165">PidLidFormPropStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="fba68-166">PidLidFormStorage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="fba68-167">PidLidHeaderItem 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="fba68-168">PidLidPageDirStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="fba68-169">PidLidPropertyDefinitionStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="fba68-170">PidLidReminderSet 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="fba68-171">PidLidReminderTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="fba68-172">PidLidFlagRequest 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="fba68-173">PidLidScriptStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="fba68-174">PidLidSmartNoAttach 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="fba68-175">PidLidToDoTitle 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="fba68-176">PidLidUseTnef 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="fba68-177">**PSETID_Meeting** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-178">PidLidMeetingType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="fba68-179">**PSETID_Task** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-180">PidLidTaskActualEffort 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="fba68-181">PidLidTaskDueDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="fba68-182">PidLidTaskEstimatedEffort 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="fba68-183">PidLidTaskFRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="fba68-184">PidLidTaskStartDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="fba68-185">PidLidTaskStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="fba68-186">**PS_INTERNET_HEADERS** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-187">PidTagInternetReturnPath 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="fba68-188">**PSETID_Log** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-189">PidLidLogDuration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="fba68-190">PidLidLogEnd 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="fba68-191">PidLidLogStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="fba68-192">PidLidLogType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="fba68-193">**PS_PUBLIC_STRINGS** 名前空間の名前付きプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fba68-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="fba68-194">PidNameKeywords 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="fba68-195">PidNameExchangeJunkEmailMoveStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fba68-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="fba68-196">関連項目</span><span class="sxs-lookup"><span data-stu-id="fba68-196">See also</span></span>



[<span data-ttu-id="fba68-197">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="fba68-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="fba68-198">Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する</span><span class="sxs-lookup"><span data-stu-id="fba68-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="fba68-199">連絡先アイテムのメール アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="fba68-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="fba68-200">メッセージと共に保存されているユーザー設定フォーム定義を削除する</span><span class="sxs-lookup"><span data-stu-id="fba68-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

